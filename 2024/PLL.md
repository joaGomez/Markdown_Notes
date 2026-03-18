La función de un PLL (*Phase Locked Loop*) es la de enganchar la frecuencia del $VCO$ a la frecuencia de la señal de entrada.
### Diagrama de bloques
![[Pasted image 20241010113800.png#center]]
La función del comparador de fase es la de entregar una tensión proporcional a la diferencia de fase($\Delta \phi$) entre la señal del $VCO$ y la señal de entrada.
$$\Delta \phi = \phi_{in} - \phi_{VCO} = \frac{\Delta t}{T}2\pi \Longrightarrow V_{0}= K_{\phi}\Delta \phi \quad \text{Salida del comparador de fase}$$
#### Implementación (Comparador de fase)
- Multiplicador:
![[Pasted image 20241010114309.png#center]]
$$\begin{cases}
V_{0}= \frac{BA}{2}cos(\phi) \\
K_{\phi} = \frac{dV_{0}}{d\phi} = - \frac{BA}{2}sen(\phi) → K_{\phi= \frac{\pi}{2}} = - \frac{BA}{2} \quad \text{Máxima ganancia del detector} \\
\end{cases}$$
- XOR:
![[Pasted image 20241010114650.png#center]]
- Edge detector (Phase Frequency Detector):
![[Pasted image 20241010114739.png#center]]
- Edge detector + Charge pump:
![[Pasted image 20241010114955.png#center]]
#### VCO
La función del $VCO$ es generar una frecuencia proporcional a la tensión de entrada.
![[Pasted image 20241010115141.png#center]]
#### Transferencia
Dado el siguiente diagrama de bloques:
![[Pasted image 20241010115330.png]]
La función de transferencia será:
$$H(s) = \frac{\phi_{VCO}}{\phi_{in}} = \frac{\frac{K_{\phi}F(s)K_{VCO}}{s}}{1+\frac{K_{\phi}F(s)K_{VCO}}{s}}$$
También, se puede hallar en función de $V_0:$
![[Pasted image 20241010122046.png]]
### Rangos de captura y de enganche
![[Pasted image 20241010122143.png#center|400]]
#### Transferencia
![[Pasted image 20241010122332.png#center|500]]
En ausencia del filtro $F(s):$
![[Pasted image 20241010122416.png#center|500]]
