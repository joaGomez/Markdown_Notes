Se concibe como ruido toda señal no deseada presente en la banda útil del sistema. Esta señal se considera aleatoria, por lo que no se puede determinar su valor instantáneo ni su fase.

En general, se determine el ruido mediante alguna distribución probabilística útil para el caso.
#### Tipos de ruido
- No correlacionado:
	- Ruido externo → Es generado en fuentes externas a los circuitos (Ruido atmosférico, cósmico, o de equipos electrónicos).
	- Ruido interno → Es generado en los dispoitivos pasivos y activos de un circuito (Ruido térmico, ruido 1/f, ruido de disparo, ruido burst/popcorn) .
- Correlacionado → Resultado directo de la señal (distorsión armónica, distorsión por intermodulación).
#### Posibles soluciones
Ante el ruido externo, se pueden colocar blindajes que aisalan los circuitos de estos factores, como los cables STP, o FTP.

Para ruido interno, es importante diseñar bajo condiciones de bajo ruido, como no utilizar resistencias muy grandes.

Ante la distorsión, como se debe a diversos factores, una posible solución es blindaje, para que la señal de entrada sea lo más limpia posible. Además, se debe diseñar a partir de una correcta definición de los límites de trabajo del circuito.

Para evitar la distorsión de la señal, el filtro debe ser de amplitud constante y fase lineal.
#### Distorsión armónica
Ante la distorsión armónica, se modela la señal de entrada como una serie, tal que:
$$
\psi_{salida}(t) = V_{0}+V_{1}\cos(\omega_{0}t+\varphi_{1}) + V_{2}\cos(2\omega_{0}t+\varphi_{2}) + \dots + V_{n}\cos(n\omega_{0}t+\varphi_{n})
$$
Donde se cumple que la distorsión armónica total será:
$$
\text{THD}(\%) = \frac{\sqrt{\sum_{n=2}^{\infty}V_{n}^{2}}}{V_{1}} \cdot 100
$$
Esta representación corresponde a un única tono de entrada. Si se ingresa con una señal de entrada de mayor cantidad de tonos, aunque todas las señales de entrada sean de la misma frecuencia, la salida tendrá cmponentes de distintas frecuencias,las cuales pueden llegar a estar ubicadas en la banda de interés, y afectar la distorsión del circuito.

![[Pasted image 20260312170418.png#center]]
#### Clasificación por colores
| Color       | Dependencia de f  |
| ----------- | ----------------- |
| Violeta     | $f^{2}$           |
| Azul        | $f$               |
| Blanco      | 1                 |
| Rosa        | $\frac{1}{f}$     |
| Rojo/Marrón | $\frac{1}{f^{2}}$ |
#### Ruido térmico
Este es causado por la agitación térmica en los portadores del conductor. Además, está presente en todos los elementos pasivos resistivos.

Su espectro de densidad de potencia puede expresarse como:
$$
S(\omega) = \frac{h\omega}{\pi\left( e^\frac{{h\omega}}{2\pi kT} -1\right)} \underset{\text{espectro plano para }f<1 \text{THz}}{=} 2kT
$$
Se puede representar la potencia de ruido sobre una resistencia de $1 \Omega$ como:
$$
P = \int S(\omega) \, df 
$$
De esta forma, se obtiene que:
$$
\bar{v}_{n} = \sqrt{ 4kTR\Delta f } \qquad \wedge \qquad \bar{i}_{n} = \sqrt{ 4kT\Delta f } 
$$
Con estas expresiones se modela por Thèvenin, o Norton, modelando al ruido como fuente, y colocando una resistencia ideal:
![[Pasted image 20260312173158.png#center]]
![[Pasted image 20260312173214.png#center|334]]
#### Ruido de disparo
Este ruido se genera cuando una corriente cruza una barrera de potencial tal como una juntura PN:
$$
i_{ind}^{2} = \int_{0}^{\Delta B}(2qI_{D}+4qI_{I})   \, df 
$$
SIendo $I_{D}$ la corriente en directa, e $I_{I}$ la corriente en inversa.

**Obs:** Esa expresión es general. Cuando la juntura se polariza, sólo se tiene en cuenta la corriente correspondiente a esa polarización.

Para modelarlo como una fuente de tensión de ruido, se debe considerar la resistencia de la juntura:
$$
r_{j} = \frac{kT}{qI_{D}} \quad \to \quad \bar{v}_{n}^{2} = \int r_{j}^{2}S_{i}(\omega)  \, df  = \frac{2k^{2}T^{2}}{qI_{D}}\Delta f
$$
#### Ruido de Flicker
También es conocido como ruido $\frac{1}{f}$. Es generado en los dispositivos activos, y se asocia a la corriente continua (polarizaciones).
$$
S_{V}(\omega) = \frac{K_{e}^{2}}{f} \quad \to \quad \bar{v}_{n}^{2} = K_{e}^{2}\ln\left( \frac{f_{max}}{f_{min}} \right) 
$$
Donde $K_{e}$ depende del dispositivo.

**Obs:** A bajas frecuencias, el ruido de Flicker es dominante.
#### Ruido Burst o de PopCorn
Se genera a causa de las imperfecciones en los materiales semiconductores, y genera ruido en frecuencias menores a 100Hz. Es del tipo $\frac{1}{f^{2}}$, sólo aplicable en VLF.
#### Múltiples fuentes de ruido
Si consideramos varias fuentes de ruido aplicadas a un circuito, podemos reemplazar cada una como una fuente de tensión y hallar la tensión de ruido a la salida de cada fuente:

![[Pasted image 20260313105728.png#center]]

Si las señales son independientes, y al menos una posee media nula:
$$
S_{3}(\omega) = S_{1}(\omega) + S_{2}(\omega)
$$
Además, se cumple que:
$$
\bar{v}_{n}^{2} = \bar{v}_{n_{1}}^{2} + \bar{v}_{n_{2}}^{2} + \dots + \bar{v}_{nj}^{2}
$$
Para fuentes independientes pero con media no nula:
$$
S_{3}(\omega) = S_{1}(\omega) + S_{2}(\omega) + V_{1}\cdot V_{2}\cdot \delta(\omega)
$$
Si las fuentes no son independientes, se debe evaluar la correlación entre ambas para obtener el valor de los 2 últimos términos:
$$
S_{3}(\omega) = S_{1}(\omega) + S_{2}(\omega) + \mathcal{F}\left\{  \int v_{1}(\tau)v_{2}(t+\tau) \, d\tau   \right\} + \mathcal{F}\left\{  \int v_{2}(\tau)v_{1}(t+\tau) \, d\tau   \right\}
$$
#### Densidad de potencia máxima
Si tomamos impedancias, la máxima transferencia de potencia se produce cuando $Z_{L}=Z_{s}^{*}$. En este caso, la tensión de ruido se dividirá en mitades entre la resistencia generadora y la carga.
$$
S_{max} (\omega) = \frac{kT}{2} \quad \to \quad P_{n_{max}} = kT\Delta f
$$
#### Ancho de banda equivalente
Se considera que el ruido ha pasado a través de un circuito con transferencia $H(\omega)$, dando como espectro a la salida $S_{o}(\omega) = S_{i}(\omega)|H(\omega)|^{2}$.

![[Pasted image 20260313111737.png#center]]

El valor pico estará dado por el máximo de la transferencia. Por lo tanto, el ancho de banda equivalente será dado por:
$$
B_{eq} = \frac{\int_{0}^{\infty} |H(\omega)|^{2} \, df}{|H(0)|^{2}}
$$

![[Pasted image 20260310191858.png#center]]
### Ruido en transistores
Se puede considerar el modelo equivalente del transistor y considerar el ruido en todas sus fuentes:

![[Pasted image 20260310192043.png#center]]

Los valores de las fuentes de ruido resultan:
$$
e_{nf}^2 = 4kT B R_f, \qquad  
e_{nb}^2 = 4kT B R_b
$$
$$
i_{ne}^2 = 2 q B I_e, \qquad  
i_{nc}^2 = 2 q B I_c = 2 q B \alpha I_e
$$
Considerando en las expresiones anteriores las ganancias de corriente en base y emisor común:
$$
\alpha = \frac{\alpha_0}{\sqrt{1 + \left( \frac{f}{f_c} \right)^{2}}} \qquad \beta_0 = \frac{\alpha_0}{1 - \alpha_0}
$$
El resultado es una tensión de ruido a la salida que presenta una expresión como la siguiente:
$$
\begin{align*}

& \overline{v_n^2}  
= 2 k T B (r_e + r_b + 2 R_s)  
+ \frac{2 k T B (r_e + r_b + 2 R_s)^2}{r_e \, \beta_0}  
\left[ 1 + \left( \frac{f}{f_c} \right)^2 \right] (1 + \beta_0)
\\
& \overline{I_{n}^{2}} = \frac{2kTB}{r_{e}\beta_{0}} \left[ 1+\left( \frac{f}{f_{c}} \right)^{2} (1+\beta_{0})\right]
\end{align*}
$$
Es usual expresar el equivalente del transistor como una fuente de tensión de ruido y una de corriente de ruido. 

![[Pasted image 20260313114945.png#center]]
#### Ruido en operacionales
Se representa por las fuentes de tensión y corriente de ruido en las entradas de un amplificador ideal.

![[Pasted image 20260313182155.png#center]]

Considerano un amplificador sn ruido con ganancia $A_{v}:$
$$
E_{n_{0}}^{2} = (E_{n}^{2}+E_{t}^{2})|A_{v}|^{2} \bigg{|} \frac{Z_{in}}{Z_{in}+R_{s}}\bigg{|}^{2} + I_{n}^{2}|A_{v}|^{2}|Z_{in}||R_{s}|^{2}
$$
El ruido referenciado a la entrada será:
$$
E_{ni}^{2} = E_{t}^{2} + E_{n}^{2} + I_{n}^{2}R_{s}^{2}
$$
Si se encuentran correlacionados:
$$
E_{ni}^{2} = E_{t}^{2} + E_{n}^{2} + I_{n}^{2}R_{s}^{2}+2CE_{n}I_{n}R_{s}
$$
Donde $C$ es el coeficiente de correlación.
$$
\text{FIgura de ruido: } \qquad \text{NF} = 10\log\left( \frac{E_{ni}^{2}}{E_{t}^{2}} \right) = 10 \log\left( \frac{E_{t}^{2}+E_{n}^{2}+I_{n}^{2}R_{s}^{2}}{E_{t}^{2}} \right) 
$$
$$
\text{Valor óptimo: } \qquad F_{opt} = 1 + \frac{E_{n}I_{n}}{2kT\Delta f}
$$
##### Representación usual
![[Pasted image 20260313183008.png#center]]
#### Factor de ruido
Éste representa la relación entre la relación señal a ruido a la salida, y la misma relación a la entrada del amplificador.
$$
F = \frac{\frac{S}{N}\bigg{|}_{i}}{\frac{S}{N}\bigg{|}_{o}} = 1 + \frac{N_{ao}}{N_{io}}
$$
Para muchos amplificadores en cascada conectados, se puede determinar el factor de ruido total mediante la fórmula de Fris:
$$
F_{total} = F_{1} + \frac{F_{2}-1}{G_{1}} + \frac{F_{3}-1}{G_{1}\cdot G_{2}} + \dots + \frac{F_{n}-1}{G_{1}\cdot \, \dots \, \cdot G_{n-1}} 
$$
#### Temperatura equivalente de ruido
Si el ruido es únicamente térmico, la densidad de potencia es función de la temperatura, y se considera la temperatura responsable de esa potencia como la temperatura de ruido.
$$
S_{na} = \frac{kT_{eq}}{2}, \text{ considerando } F= \frac{S_{nio}+S_{nao}}{S_{nio}} =1 + \frac{T_{eq}}{T_{o}} \to T_{eq}=(F-1)\cdot T_{o}
$$
Aplicando la fórmula de Friis:
$$
T_{eq_{total}} = T_{eq_{1}} + \frac{T_{eq_{2}}}{G_{1}} + \dots + \frac{T_{eq_{n}}}{G_{1}\cdot \, \dots \, G_{n-1}}
$$
