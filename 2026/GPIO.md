### Diagrama en bloques
![[Pasted image 20260322125645.png#center]]

GPIO se define como general purpose input or output. La idea es tener puertos capaces de comportarse como input, output, o ambos.

En la freedom, GPIO contiene 5 puertos de 32 bits cada uno, desde el puerto A, hasta el puerto E.

```c
/** GPIO - Register Layout Typedef */

typedef struct {

__IO uint32_t PDOR; /**< Port Data Output Register, offset: 0x0 */

__O uint32_t PSOR; /**< Port Set Output Register, offset: 0x4 */

__O uint32_t PCOR; /**< Port Clear Output Register, offset: 0x8 */

__O uint32_t PTOR; /**< Port Toggle Output Register, offset: 0xC */

__I uint32_t PDIR; /**< Port Data Input Register, offset: 0x10 */

__IO uint32_t PDDR; /**< Port Data Direction Register, offset: 0x14 */

} GPIO_Type;
```
#### Acceso periférico PORT
![[Pasted image 20260323111731.png#center]]

Cada pin de cada puerto es configurable mediante un registro de 32 bits llamado Pin Control Register (PCR).

**¿Qué permite configurar el PCR?**
- Generación de interrupciones desde el pin
- Filtrado digital (de-glitch)
- Pullup/down
- Impedancia de salida y slew rate (EMC)
- Open drain
- Mux que permite seleccionar GPIO, ADC, y otros módulos

![[Pasted image 20260323112009.png#center]]
##### ISF: Interrupt status flag
- 0: No se detecta la interrupción configurada.
- 1: Se detecta la configuración configurada.

Si el pin está configurado para generar una solicitud DMA, el indicador correspondiente se borrará automáticamente al finalizar la transferencia DMA solicitada. De lo contrario, el indicador permanecerá activado hasta que se escriba un 1 lógico en él. Si el pin está configurado para una interrupción sensible al nivel y permanece activado, el indicador se vuelve a activar inmediatamente después de borrarse.

El bit ISF de cada PCR tiene una copia en este registro. Dado que el registro es de 32 bits contiene 32 flags, agrupa todos los flags de un mismo puerto. Por lo tanto, este registro nos permite acceder a todos los flags de una sola vez.
##### IC: Interrupt configuration
El pin de configuración de interrupciones es válido para todas los modos de elección del pin por mux.
##### LK: Lock register
- 0: El campo \[15:0\] del PCR no está bloqueado.
- 0: El campo \[15:0\] del PCR está bloqueado, y no puede ser actualizado hasta el próximo reset del sistema.
##### MUX (Pin mux control)
Define la conexión al pin. No todos los pines soportan todas las configuraciones del mux. Las configuraciones sin implementar del mux quedan reservadas y los pines pueden ser configurados en otras opciones del mux.
##### Control de slew rate
Hay dos aspectos que deben ser tenidos en cuenta para reducir las emisiones electromagnéticas : la pendiente decrecimiento y el overshoot . Si el valor del overshoot excede a VDD en la caida de un diodo el circuito de proteccion se enciende aumentando asi la corriente y por lo tanto la EMC. Es por eso que se debe analizar bien en que pines es necesario tener un alto SR.

Excesivo overshoot y un subsecuente ringing son indicadores de capacitores de desacople insuficientes y trazas en el PCB muy largas.
##### Open drain, Pull enable y Pull select
Se activa (1) o desactiva (0) para salida digital en cualquiera de los modos del mux. Se activa cuando el pin se configura como output digital. En cambio, se activa PULL ENABLE cuando el pin se configura como input digital.

El pin para PULL SELECT se activa (1) cuando el PULL ENABLE está seteado.
##### Global pin control HIgh/Low registers
![[Pasted image 20260323115639.png#center]]

Permite modificar en forma simultánea varios PCR del puerto X (n= 0:15 LOW / n= 16:31 HIGH) 

Los registros **PORTx_GPCLR** y **PORTx_GPCHR** permiten configurar múltiples PCR de forma en conjunto sin usar *read-modify-write*.  
  
- **GPCLR** → configura pines **0–15**  
- **GPCHR** → configura pines **16–31**  
  
*Ambos funcionan igual*


- **GPWE**: máscara de pines a modificar  
- **GPWD**: valor a escribir en PCR\[n] de esos pines  
**Sintaxis**
```c
PORTx->GPCLR = (MASK << 16) | VALUE;

PORTx->GPCHR = (MASK << 16) | VALUE;
```
**Ejemplo: Configurar PTD20–PTD23 como GPIO (MUX = 1)**
```c
PORTD->GPCHR = (0x00F0 << 16) | (1 << 8);
```
- `0x00F0` → afecta pines 20–23 (bits 4–7 del GPWE alto)
- `(1<<8)` → MUX = 1

**Ejemplo: Habilitar Pull-Up en PTC0–PTC7**
```c
PORTC->GPCLR = (0x00FF << 16) | ((1 << 1) | (1 << 0));
```
`PE=1 (bit1), PS=1 (bit0)`
##### Digital filter
El filtrado de las entradas digitales permite rechazar pulsos no deseados presentes en líneas digitales que normalmente están en 0 o 1. Estas interferencias pueden provenir de fuentes de RF y/o conmutadores electromecánicos, etc.

Para habilitar el filtro digital, se utiliza el regristro PORTx_DFER.

Para establecer un tipo de filtro a usar, está el digital clock register (PORTx_DFCR).

**Ejemplo: Filtro digital para SW2**

```c
#include "MK64F12.h"

void init_sw2_with_filter(void) {
    // 1) Habilitar clock para PORTC
    SIM->SCGC5 |= SIM_SCGC5_PORTC_MASK;

    // 2) Configurar PTC6 como GPIO (MUX = 1)
    PORTC->PCR[6] = PORT_PCR_MUX(1);

    // 3) Configurar PTC6 como entrada
    PTC->PDDR &= ~(1 << 6);

    // 4) CONFIGURAR FILTRO DIGITAL ----------------------

    // 4.1 Seleccionar la fuente de clock del filtro
    // 0 = bus clock (rápido, corta rebotes de pocos microsegundos)
    // 1 = LPO 1 kHz (cada tick es 1 ms, útil para rebotes de botones)
    PORTC->DFCR = 1;  // Usar LPO clock (~1 kHz)

    // 4.2 Configurar ancho del filtro en DFWR
    // Valor N: la entrada debe permanecer estable durante N+1 ciclos del clock elegido.
    // Con LPO (1 kHz), DFWR = 5 → entrada estable 6 ms.
    PORTC->DFWR = 5;

    // 4.3 Habilitar el filtro digital en PTC6
    PORTC->DFER |= (1 << 6);
}

// Lectura del botón con filtro digital
int sw2_leer(void) {
    // SW2 es activo en LOW
    return (PTC->PDIR & (1 << 6)) == 0;
}

int main(void) {
    init_sw2_with_filter();

    // Ejemplo básico: leer el botón y encender un LED
    SIM->SCGC5 |= SIM_SCGC5_PORTB_MASK;
    PORTB->PCR[18] = PORT_PCR_MUX(1);   // LED rojo
    PTB->PDDR |= (1 << 18);

    while (1) {
        if (sw2_leer()) {
            PTB->PSOR = (1 << 18);   // LED ON
        } else {
            PTB->PCOR = (1 << 18);   // LED OFF
        }
    }
}
```
##### Clock gating
- Los procesadores modernos poseen mecanismos para reducir el consumo del chip apagando todos los recursos que no son usados. Esto se logra apagando el clock de dichos módulos (clock gating).
- Para configurar que módulos reciben clock se deben habilitar los bits correspondientes en los registros SCGCx (System Clock Gating Control Register x).
- Después del reset estos bits están apagados para ahorrar energía.
- Los SCGCx. se encuentran dentro del modulo SIM (System Integration Module).
- Antes de usar un modulo se debe habilitar el clock de lo contrario se genera un error. De igual forma antes de apagar un clock se deberá deshabilitar el modulo.
- El registro SCGC5 del modulo SIM contiene los bits necesarios para habilitar el clock de la lógica de PORT.
```c
//Enable clocking for port B 
SIM->SCGC5 |= SIM_SCGC5PORTB_MASK; 
```
### GPIO: Ejemplos
```c
PTB->PDDR = (1<<21)|(1<<22); // Defino pin 21 y 22 del GPIO B como Salidas

PTB->PDOR = (PTB->PDOR & ~(1<<pin)) | (data << pin); // Change pin value

PTB->PSOR = (1<<21)|(1<<22); // Set pin 21 and 22

PTB->PCOR = (1<<21)|(1<<22); // Clear pin 21 and 22

PTB->PTOR = (1<<21)|(1<<22); // Toggle pin 21 and 22

if (PTA->PDIR & (1<<4)) // Test pin 4 
	Do_something(); // if pin 4 == 1
```
Se pueden crear definiciones propias cuando sea necesario:

![[Pasted image 20260323122521.png#center]]
### PCR: Ejemplos
```c
/Configure Individual Pins (pin 22) PORTB->PCR[22]=0x0; //Clear all bits then set pin22 properties 
PORTB->PCR[22] |=PORT_PCR_MUX(PORT_mGPIO); //Set MUX to GPIO mode on pin22 
PORTB->PCR[22] |=PORT_PCR_DSE(1); //Drive strength: enabled 
PORTB->PCR[22] |=PORT_PCR_IRQC(PORT_eDisabled); //Disable interrupts 

// Configure Multiple Pins at once using Global Registers 
// First define which Pins will be modified 
temp =PORT_GPCHR_GPWE((1<<(21-16))|(1<<(22-16))); 
// Then set pin properties 
temp|=PORT_GPCHR_GPWD(PORT_PCR_MUX(PORT_mGPIO)); //Set MUX to GPIO pin22 & pin21 
temp|=PORT_GPCHR_GPWD(PORT_PCR_DSE(1)); //Drive strenght pins 21&22: enabled 
PORTB->GPCHR=temp; //Done 
```
