Los capacitores dentro del transistor generan un polo. Por lo tanto, $h_{fe}$ va a comenzar a dependar de la frecuencia.

**Obs:** $f_{t}$ es la frecuencia de transición, cuando la ganancia es 1, o sea 0 dB.

**Obs:** Cada elemento reactivo (independiente) en el circuito introducirá siempre un polo y un cero.
#### Respuesta en frecuencia de amplificadores
Tanto la ganancia de tensión, de corriente, de potencia, y la eficiencia, van a depender de la frecuencia.
#### Modelo de alta frecuencia BJT con capacidades parásitas
![[Pasted image 20241030165322.png#center]]

![[Pasted image 20241030165404.png#center]]
En las hojas de datos se suele especificar $f_{t}$, $C_{ib}$, $C_{ob}$.
![[Pasted image 20241030165627.png#center]]
## Método de las constantes de tiempo
- **Método de cortocircuito:** Este método permite conocer la contribución relativa de cada capacitor al polo. También, permite estimar el mayor de los polos. Se utilizará este método para el polo de bajas frecuencias.
	1. Pasivar el generador de entrada.
	2. Hacer superposición con los capacitores.
	3. Determinar la resistencia $R_{i}$ vista desde los bornes de cada capacitor $C_{i}$.
	4. Calcular la frecuencia de -3 dB mediante: $f_{p}\simeq \sum\limits \frac{1}{2\pi R_{i}C_{i}}$
- **Método de circuito abierto:** Se utiliza para estimar el menor de los polos. Es útil para altas frecuencias.
	1. A diferencia del anterior método, el resto de los capacitores se consideran circuitos abiertos.
	2. La frecuencia de -3 dB se calcula como: $f_{p}\simeq \frac{1}{2\pi \sum\limits R_{i}C_{i}}$
----

| Polo         |                                 $f_{L}$                                  |                        $f_{H}$                         |
| :----------- | :----------------------------------------------------------------------: | :----------------------------------------------------: |
| Método       |                              Cortocircuito                               |                    Circuito abierto                    |
| Ecuación     |             $\frac{1}{2\pi}\sum\limits \frac{1}{R_{i}C_{i}}$             |        $\frac{1}{2\pi \sum\limits R_{i}C_{i}}$         |
| Dominante    |         $\frac{1}{2\pi}(\frac{1}{\tau_1}+\frac{1}{\tau_2}+...)$          |        $\frac{1}{2\pi(\tau_{1}+\tau_{2}+...)}$         |
| No dominante | $\frac{1}{2\pi}\sqrt{\frac{1}{\tau^{2}_{1}}+\frac{1}{\tau^{2}_{2}}+...}$ | $\frac{1}{2\pi\sqrt{(\tau^{2}_{1}+\tau^{2}_{2}+...)}}$ |
Donde $\tau_{i} = R_{i}C_{i}$.
#### Equivalencias para xFET
![[Pasted image 20241030183200.png#center]]
#### Fórmulas
![[Pasted image 20241030183228.png#center]]
#### Acoples multietapas
Cuantos menos capacitores mejor:
![[Pasted image 20241030183329.png#center]]
#### Resumen
- Los capacitores externos limitan la respuesta en baja frecuencia. Para determinar su influencia en el circuito se utiliza el método de las constantes de tiempo.
- La respuesta en frecuencia de los Source y Emisor comunes está drasticamente limitada por el efecto Miller.
- Drain y Colector comunes pueden tener polos complejos conjugados. En estos casos no hay un aumento de las capacidades, sino por el contrario una reducción, por eso tienen grandes anchos de banda.
- Base común y gate común NO sufren efecto Miller! Por lo tanto el Cascode es un muy buen circuito para obtener grandes ganancias y gran ancho de banda.