Una interrupción es un evento que suspende la ejecución normal del programa forzando al procesador a realizar otra «tarea» de mayor prioridad que una vez finalizada retorna al programa suspendido.

- Dicho evento es generado por el hardware y se lo conoce como Interrupt Request (IRQ). Este pedido es asincrónico al programa actualmente en ejecución.
- La tarea es conocida como Interrupt Service Routine (ISR).

**Secuencia**
![[Pasted image 20260324134217.png#center|266]]

La interrupción será aceptada al finalizar la instrucción actual de assembler (no de C). La latencia (tiempo de respuesta) del software es el tiempo que tarda desde que ocurre el evento hasta que el mismo es atendido. 

![[Pasted image 20260324134315.png#center|408]]
### Máscaras
Las interrupciones del procesador pueden ser inhibidas o habilitadas por software. La terminología frecuentemente usada es enmascarar (inhibir) una interrupción.

Hay dos tipos de máscaras:
1. Máscara global: Una llave general que corresponde a un bit del procesador (Global Interrupt Enable).
2. Máscara individual: Una llave o enable para cada periferico del microcontrolador.

![[Pasted image 20260324143442.png#center]]

Además, dentro de las interrupciones, existen las enmascarables (se pueden deshabilitar por software), y las no enmascarables (no se pueden deshabilitar por software).
### Vectores de interrupción
Son vectores donde cada elemento es un puntero a una función para cada interrrupción.

![[Pasted image 20260324143744.png#center]]
### Secuencia de la interrupción
Configuración inicial (SW):
1. Se habilita la interrupción particular (Periférico).
2. Se desenmascaran las interrupciones Globales.

Entrada a la rutina de interrupción (HW):
1. Se genera el pedido de interrupción, encendiéndose el flag correspondiente (xxxIF).
2. Se finaliza la ejecución de la instrucción en curso.
3. Se guarda en el stack el contexto de trabajo (dirección de retorno y demás registros) en forma automática.
4. Se transfiere el control a la ISR, mediante el vector de interrupción.

**Códigos bloqueante:** La CPU interroga constantemente al periférico para ver si hay algún evento que atender.
**Polling:** La CPU interroga al periférico intercalando ahora otras tareas.

Gran parte de los eventos generados por el hardware son lentos en relación a la velocidad del procesador para este caso la mejor estrategia es utilizar una interrupción periódica (PISR).

![[Pasted image 20260324144829.png#center]]
#### Interrupciones dedicadas
Cuando el evento es de corta duración en relación al tiempo de la CPU una interrupción periódica no es posible. En estos casos deberemos utilizar una interrupción dedicada a ese evento.

**Recomendaciones:**
- Siempre que sea posible usar interrupciones periódicas para capturar eventos externos.
- Hay que analizar cuidadosamente cuales son los eventos que se asignaran a interrupciones dedicadas.
- Las interrupciones dedicadas son breves.

![[Pasted image 20260324145015.png#center|479]]
### NVIC: Nested vector interrupt controller
Éste es un controlador de interrupciones integrado en los microcontroladores basados en ARM Cortex-M. Su función es gestionar todas las interrupciones del sistema.

![[Pasted image 20260324191058.png#center]]

**Ejemplo: Interrupción por botón SW2**
```c
#include "MK64F12.h"
void init_pins(void);
void init_nvic(void);

int main(void) {
    init_pins();
    init_nvic();

    while(1) {
        // el programa principal no hace nada
        // todo ocurre por interrupciones
    }
}

void init_pins(void) {

    /* ------------------- LED ROJO (PTB22) ------------------- */
    SIM->SCGC5 |= SIM_SCGC5_PORTB_MASK;   // habilita reloj al PORTB
    PORTB->PCR[22] = PORT_PCR_MUX(1);     // función GPIO
    PTB->PDDR |= (1 << 22);               // pin como salida
    PTB->PCOR = (1 << 22);                // LED OFF

    /* ------------------- SW2 (PTC6) ------------------------- */
    SIM->SCGC5 |= SIM_SCGC5_PORTC_MASK;   // habilita reloj al PORTC
    PORTC->PCR[6] = PORT_PCR_MUX(1)       // GPIO
                  | PORT_PCR_PE_MASK      // enable pull
                  | PORT_PCR_PS_MASK      // pull-up
                  | PORT_PCR_IRQC(0b1010); // interrupción por falling edge

    PTC->PDDR &= ~(1 << 6);               // pin como entrada
}

void init_nvic(void) {
    NVIC_EnableIRQ(PORTC_IRQn);        // habilita interrupciones del PORTC
    NVIC_SetPriority(PORTC_IRQn, 3);   // prioridad cualquiera
}

/* ---------------- INTERRUPT HANDLER ---------------- */
void PORTC_IRQHandler(void) {

    // limpia el flag de interrupción del pin C6
    PORTC->ISFR = (1 << 6);

    // toggle del LED rojo
    PTB->PTOR = (1 << 22);
}
```
El NVIC es útil ya que sin el, deberías realizar polling todo el tiempo, sin control de prioridades, sin poder interrumpirse ente sí, y sería difícil expandir el firmware.

El orden del vector de interrupciones por defecto en la freedom es:
```c
__attribute__ ((used, section(".isr_vector")))

void (* const g_pfnVectors[])(void) = {

// Core Level - CM4

&_vStackTop, // The initial stack pointer

ResetISR, // The reset handler

NMI_Handler, // The NMI handler

HardFault_Handler, // The hard fault handler

MemManage_Handler, // The MPU fault handler

BusFault_Handler, // The bus fault handler

UsageFault_Handler, // The usage fault handler

0, // Reserved

0, // Reserved

0, // Reserved

0, // Reserved

SVC_Handler, // SVCall handler

DebugMon_Handler, // Debug monitor handler

0, // Reserved

PendSV_Handler, // The PendSV handler

SysTick_Handler, // The SysTick handler

  

// Chip Level - MK64F12

DMA0_IRQHandler, // 16 : DMA Channel 0 Transfer Complete

DMA1_IRQHandler, // 17 : DMA Channel 1 Transfer Complete

DMA2_IRQHandler, // 18 : DMA Channel 2 Transfer Complete

DMA3_IRQHandler, // 19 : DMA Channel 3 Transfer Complete

DMA4_IRQHandler, // 20 : DMA Channel 4 Transfer Complete

DMA5_IRQHandler, // 21 : DMA Channel 5 Transfer Complete

DMA6_IRQHandler, // 22 : DMA Channel 6 Transfer Complete

DMA7_IRQHandler, // 23 : DMA Channel 7 Transfer Complete

DMA8_IRQHandler, // 24 : DMA Channel 8 Transfer Complete

DMA9_IRQHandler, // 25 : DMA Channel 9 Transfer Complete

DMA10_IRQHandler, // 26 : DMA Channel 10 Transfer Complete

DMA11_IRQHandler, // 27 : DMA Channel 11 Transfer Complete

DMA12_IRQHandler, // 28 : DMA Channel 12 Transfer Complete

DMA13_IRQHandler, // 29 : DMA Channel 13 Transfer Complete

DMA14_IRQHandler, // 30 : DMA Channel 14 Transfer Complete

DMA15_IRQHandler, // 31 : DMA Channel 15 Transfer Complete

DMA_Error_IRQHandler, // 32 : DMA Error Interrupt

MCM_IRQHandler, // 33 : Normal Interrupt

FTFE_IRQHandler, // 34 : FTFE Command complete interrupt

Read_Collision_IRQHandler, // 35 : Read Collision Interrupt

LVD_LVW_IRQHandler, // 36 : Low Voltage Detect, Low Voltage Warning

LLWU_IRQHandler, // 37 : Low Leakage Wakeup Unit

WDOG_EWM_IRQHandler, // 38 : WDOG Interrupt

RNG_IRQHandler, // 39 : RNG Interrupt

I2C0_IRQHandler, // 40 : I2C0 interrupt

I2C1_IRQHandler, // 41 : I2C1 interrupt

SPI0_IRQHandler, // 42 : SPI0 Interrupt

SPI1_IRQHandler, // 43 : SPI1 Interrupt

I2S0_Tx_IRQHandler, // 44 : I2S0 transmit interrupt

I2S0_Rx_IRQHandler, // 45 : I2S0 receive interrupt

UART0_LON_IRQHandler, // 46 : UART0 LON interrupt

UART0_RX_TX_IRQHandler, // 47 : UART0 Receive/Transmit interrupt

UART0_ERR_IRQHandler, // 48 : UART0 Error interrupt

UART1_RX_TX_IRQHandler, // 49 : UART1 Receive/Transmit interrupt

UART1_ERR_IRQHandler, // 50 : UART1 Error interrupt

UART2_RX_TX_IRQHandler, // 51 : UART2 Receive/Transmit interrupt

UART2_ERR_IRQHandler, // 52 : UART2 Error interrupt

UART3_RX_TX_IRQHandler, // 53 : UART3 Receive/Transmit interrupt

UART3_ERR_IRQHandler, // 54 : UART3 Error interrupt

ADC0_IRQHandler, // 55 : ADC0 interrupt

CMP0_IRQHandler, // 56 : CMP0 interrupt

CMP1_IRQHandler, // 57 : CMP1 interrupt

FTM0_IRQHandler, // 58 : FTM0 fault, overflow and channels interrupt

FTM1_IRQHandler, // 59 : FTM1 fault, overflow and channels interrupt

FTM2_IRQHandler, // 60 : FTM2 fault, overflow and channels interrupt

CMT_IRQHandler, // 61 : CMT interrupt

RTC_IRQHandler, // 62 : RTC interrupt

RTC_Seconds_IRQHandler, // 63 : RTC seconds interrupt

PIT0_IRQHandler, // 64 : PIT timer channel 0 interrupt

PIT1_IRQHandler, // 65 : PIT timer channel 1 interrupt

PIT2_IRQHandler, // 66 : PIT timer channel 2 interrupt

PIT3_IRQHandler, // 67 : PIT timer channel 3 interrupt

PDB0_IRQHandler, // 68 : PDB0 Interrupt

USB0_IRQHandler, // 69 : USB0 interrupt

USBDCD_IRQHandler, // 70 : USBDCD Interrupt

Reserved71_IRQHandler, // 71 : Reserved interrupt

DAC0_IRQHandler, // 72 : DAC0 interrupt

MCG_IRQHandler, // 73 : MCG Interrupt

LPTMR0_IRQHandler, // 74 : LPTimer interrupt

PORTA_IRQHandler, // 75 : Port A interrupt

PORTB_IRQHandler, // 76 : Port B interrupt

PORTC_IRQHandler, // 77 : Port C interrupt

PORTD_IRQHandler, // 78 : Port D interrupt

PORTE_IRQHandler, // 79 : Port E interrupt

SWI_IRQHandler, // 80 : Software interrupt

SPI2_IRQHandler, // 81 : SPI2 Interrupt

UART4_RX_TX_IRQHandler, // 82 : UART4 Receive/Transmit interrupt

UART4_ERR_IRQHandler, // 83 : UART4 Error interrupt

UART5_RX_TX_IRQHandler, // 84 : UART5 Receive/Transmit interrupt

UART5_ERR_IRQHandler, // 85 : UART5 Error interrupt

CMP2_IRQHandler, // 86 : CMP2 interrupt

FTM3_IRQHandler, // 87 : FTM3 fault, overflow and channels interrupt

DAC1_IRQHandler, // 88 : DAC1 interrupt

ADC1_IRQHandler, // 89 : ADC1 interrupt

I2C2_IRQHandler, // 90 : I2C2 interrupt

CAN0_ORed_Message_buffer_IRQHandler, // 91 : CAN0 OR'd message buffers interrupt

CAN0_Bus_Off_IRQHandler, // 92 : CAN0 bus off interrupt

CAN0_Error_IRQHandler, // 93 : CAN0 error interrupt

CAN0_Tx_Warning_IRQHandler, // 94 : CAN0 Tx warning interrupt

CAN0_Rx_Warning_IRQHandler, // 95 : CAN0 Rx warning interrupt

CAN0_Wake_Up_IRQHandler, // 96 : CAN0 wake up interrupt

SDHC_IRQHandler, // 97 : SDHC interrupt

ENET_1588_Timer_IRQHandler, // 98 : Ethernet MAC IEEE 1588 Timer Interrupt

ENET_Transmit_IRQHandler, // 99 : Ethernet MAC Transmit Interrupt

ENET_Receive_IRQHandler, // 100: Ethernet MAC Receive Interrupt

ENET_Error_IRQHandler, // 101: Ethernet MAC Error and miscelaneous Interrupt

}; /* End of g_pfnVectors */
```
### Interrupciones periódicas
Para este tipo de interrupciones se utiliza Systick. El Systick Timer es un contador descendente de 24 bits, interno a la CPU Cortex-M, está integrado al NVIC y puede ser usado para generar una excepción (#15). En muchos sistemas operativos el timer es usado para administrar las tareas. Por ejemplo para permitir que múltiples tareas sean ejecutadas en diferentes momentos y evitar así que ninguna tarea bloquee al sistema.
```c
typedef struct {
__IOM uint32_t CTRL; /*!< Offset: 0x000 (R/W) SysTick Control and Status Register */
__IOM uint32_t LOAD; /*!< Offset: 0x004 (R/W) SysTick Reload Value Register */
__IOM uint32_t VAL; /*!< Offset: 0x008 (R/W) SysTick Current Value Register */
__IM uint32_t CALIB; /*!< Offset: 0x00C (R/ ) SysTick Calibration Register */
} SysTick_Type;
```
**Observación:** Si se desea generar una interrupción periódica de N pulsos de clock, el valor de recarga debe ser N-1, y el valor inicial debe ser N. No es necesario borrar ningún flag al entrar a la interrupción del Systick dado que se trata de una excepción del propio core.

**Ejemplo:**
```c
void SysTick_Init (void) { 
	SysTick->CTRL = 0x00; 
	SysTick->LOAD = 12500000L - 1; // 125ms @ 100MHz 
	SysTick->VAL = 0x00; 
	SysTick->CTRL = SysTick_CTRL_CLKSOURCE_Msk 
					| SysTick_CTRL_TICKINT_Msk 
					| SysTick_CTRL_ENABLE_Msk; 
	} 
	
	__ISR__ SysTick_Handler (void) { 
		// Your code Here 
	} 
```
