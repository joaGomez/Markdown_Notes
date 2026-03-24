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

