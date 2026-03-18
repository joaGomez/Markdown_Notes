![[Pasted image 20240904174130.png#center]]

ADC: Analog digital converter. Convierte señales analógicas a digitales.

Frecuencia mínima de muestreo → Principio de Nyquist. La frecuencia de muesrta debe ser por lo menos 2 veces el ancho de banda, es decir, se deben tomar más de dos muestras por período. De esta forma, cuantas más muestras se tomen en un periodo, se puede tener una mejor reconstrucción de la señal. En los osciloscopios suele aparecer como $1 GSa/s$. Esto quiere decir que toma un millón de muestras por segundo. El osciloscopio tiene un ancho de banda de 100 MHz, de forma que garantiza que se cumpla que la frecuencia del osciloscopio supera en más de dos veces el ancho de banda del generador (Principio de Nyquist).

El problema con este teorema es que no me dice cuantos períodos tienen que pasar para poder tener una buena reconstrucción. El criterio estándar hoy en día para una señal periódica, es de más de 10 puntos por período.

El osciloscopio tiene un pasabajos de 100 MHz en la entrada, de forma de evitar señales con mayor ancho de banda. 


![[Pasted image 20241014191012.png]]
