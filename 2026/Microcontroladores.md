![[Pasted image 20260302192432.png#center|652]]

Los MCU actuales poseen además periféricos integrados, que son módulos de hardware configurable mediante registros. 

Dicho módulo funciona en paralelo con el CPU, liberando a este de ciertas tareas (que se resuelven por hardware), permitiendo un entorno de multitarea real.

Esto permite también diseñar sistemas de baja complejidad de hardware (alta integración). La desventaja es que estos periféricos son menos versátiles que lo alcanzable por un programa ejecutado por la CPU.

![[Pasted image 20260302192543.png#center|262]]

Los MCUs suelen clasificarse, distinguirse y finalmente elegirse por:
- CPU: 8, 16, 32 (bits).
- Memoria: # de RAM / FLASH.
- Encapsulado: # y tipo de pines.
- Periféricos: Cuales, cuantos, prestaciones.
- Aplicación: Bajo costo, alta performance, low power.

### Conexionado
El conexionado común para (casi) todos los MCUs es:

   ![[Pasted image 20260302192837.png#center|450]]

#### Alimentación
Los pines de alimentación del MCU proveen energía a la circuitería interna. 

Hay MCUs que se alimentan a 5V, 3.3V, 2.7V, 1.8V, etc. En general, la tendencia es que los fabricantes bajan la tensión de alimentación de los microcontroladores, para reducir el consumo de corriente. 

Los MCUs con muchos pines (ej, > 32 pines), tienen varias patas de VDD y GND, porque el PCB puede proveer una impedancia menor que las conexiones internas del IC.
#### Clock
Los MCUs actuales tienen la posibilidad de ser clockeados desde diferentes osciladores. En general, hay tres opciones: 
- Oscilador a cristal (amplificador interno, cristal externo). Alta precisión/estabilidad de temperatura y aging. 
- Oscilador RC interno. Bajo costo, moderada precisión ~±2%, baja estabilidad de temperatura. Se puede trimmear (calibrar). 
- Oscilador externo. En general, mayor rango de frecuencias que el oscilador de cristal.

Muchas veces, la fuente de clock del MCU puede ser variada dinámicamente (o sea, el programa que corre en el MCU puede cambiar la fuente del clock), lo que permite ajustar el balance velocidad-consumo de acuerdo con los requerimientos de procesamiento/ahorro de energía. 

Muchos MCUs tienen un PLL interno, que permite obtener frecuencias más altas al oscilador y variar la velocidad del reloj en manera gradual y flexible.
#### Reset
El reset es muy importante porque le asegura al programador que el MCU comience en una condición predefinida: 
- El programa arranca desde el inicio, y no de cualquier lado. 
- El estado de todos los periféricos es conocido. 

La condición para el reseteo es, en general, un pulso de cierta duración mínima en el pin nRESET (por lo general con lógica negada y con un pullup interno).
#### Programación / Debug
Para modificar el programa que ejecuta el MCU es necesario modificar su memoria flash interna. En general hay tres opciones: 
- Programador externo: Herramienta de desarrollo que se comunica mediante pines dedicados, la cual suele ser altamente dependiente del fabricante del procesador. 
- Programador in-circuit: El programador se encuentra en la misma placa con el MCU. Muy utilizado en kits de evaluación. 
- Bootloader: El MCU se autoprograma, recibiendo el nuevo programa por otro medio (USB, WiFi, Bluetooth, etc.).

A su vez, es deseable durante la etapa de desarrollo del software (y su hardware asociado) poder “mirar” lo que está haciendo el micro. Esto es posible mediante una herramienta de desarrollo tome control del procesador, y permitir debuggear la aplicación: poner breakpoints, ejecutar paso a paso, leer valor de variables y registros, etc.).
#### Entradas y salidas
Los pines de Entrada y Salida (E/S o I/O en inglés) son la interfaz con el mundo exterior: el programa al ejecutarse puede leer las entradas y modificar las salidas. Los MCUs tienen pines de entrada y salida digitales (GPIO) altamente configurables. También suelen tener pines de entrada y salida analógicos (A/D y D/A).

Dada la cantidad de periféricos (que no siempre necesitamos usar simultáneamente) y el costo que representa un pin físico, los MCUs suelen tener sus señales multiplexadas a los pines. Es decir, un mismo pin podría ser I/O digital, entrada de conversor A/D o salida de conversor D/A, pero no simultáneamente.
#### Periféricos
Los MCUs poseen integrados varios tipos de periféricos que realizan diversas funciones específicas. Estos puede poseer hardware tanto digital como analógico. Entre ellos pueden encontrarse:
- Timers: permiten generar formas de onda en los pines de salida o medir tiempo de y entre eventos en los pines de entrada. 
- Conversores A/D y D/A: proporcionan capacidad de interfaz con el mundo analógico, sin necesidad de ICs externos. 
- Interfaces de comunicación serial: UART, SPI, I2C, USB, CAN, etc.
##### Avanzados
- Direct Memory Access (DMA): permite leer, escribir o copiar zonas de la memoria sin la CPU. 
- Watchdog Timer o Computer Operating Properly (COP): genera un RESET si la aplicación no lo “refresca” periódicamente. 
- Low Voltage Detect (LVD) o BrownOut Detect (BOD): mantiene al micro reseteado si la tensión de alimentación baja del umbral que asegura el funcionamiento de todos los componentes del micro.
##### Dedicados
- Fuentes: permiten generar tensiones reguladas para uso interno, o muy estables para referencia de los conversores A/D y D/A. 
- Amplificadores Diferenciales: permiten medir tensiones diferenciales, con mayor precisión y ganancia variable. 
- CRC Engine: permite cálculo de CRC y algoritmos complejos de redundancia.
##### Interconexionado
Es posible interconectar los periféricos para encadenar eventos y sincronizarlos, sin intervención de la CPU y de manera más eficiente. Por ejemplo:
- Realizar una conversión A/D disparada por un Timer. 
- Anular la salida de un generador de señales si la salida de un comparador se activa. 
- Al comenzar el período de un PWM, se dispara un timer monoestable, que al finalizar dispara una conversión A/D, que al finalizar dicho resultado es encolado en un buffer por el DMA.
#### Consumo
Los fabricantes de micros quieren aumentar la performance y disminuir el consumo. Como los microcontroladores se fabrican en un proceso CMOS, el consumo se divide en 2: potencia estática y potencia dinámica. En general, domina la potencia dinámica.
##### Potencia dinámica
se debe la carga y descarga de la capacidad de gate de los MOSFETs. La capacidad Cload representa la capacidad total cargada y descargada en un ciclo de clock, e incluye la capacidad de lo que está conectado a cada pin del micro. 

En cada ciclo, el capacitor $C_{load}$ se carga a $V_{DD}$. Entonces, la fuente entrega $Q=C_{load}\cdot V_{DD}$. Como esto ocurre $f_{clk}$ veces por segundo, la corriente dinámica es $I_{d}=C_{load}\cdot V_{DD}\cdot f_{clk}$.
$$
P_{d} = C_{load}\cdot V_{DD}{^2}\cdot f_{clk}
$$
Para disminuir la potencia dinámica, se puede: 
- Reducir la velocidad ($f_{clk}$): Disminuir la velocidad de clock cuando no se requiere procesamiento rápido. 
- Reducir la tensión (relación cuadrática!). Esto en general NO lo hace el programa, sino que se elige una tensión de operación cuando se diseña el sistema. 
- Reducir $C_{load}$.
![[Pasted image 20260303095451.png#center|252]]
#### Modo sleep
Los MCUs modernos tienen la capacidad de entrar en modo de bajo consumo. Esto es muy útil en equipos portátiles alimentados a batería. Es buena práctica entrar en modo sleep cuando el programa no tiene nada que hacer. 

En general, un micro tiene 2 o 3 modos de bajo consumo. Casi siempre, el modo de menor consumo también es el que tiene un tiempo de wakeup más elevado.

