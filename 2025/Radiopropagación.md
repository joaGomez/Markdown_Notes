**Ganancia de una antena:** Mide qué tan bien una antena concentra la energía radiada en una determinada dirección del espacio.

**Antena isotrópica:** Es una antena con ganancia unitaria, y que irradia la misma potencia en todas las direcciones del espacio.

### Área efectica
Esta área no es el área geométrica, sino que es una medida de cuánta potencia de una onda electromagnética incidente puede captar realmente la antena.

Para una antena sin pérdidas, la potencia recibida será:
$$
P_{r} = |S|\cdot A_{e}
$$
Además, se puede determinar el área efectiva máxima para una antena, la cual va a depender de la longitud de onda que se busca captar:
$$
A_{e_{max}} = \frac{\lambda^{2}}{4\pi}\cdot g_{max}
$$
Donde $g_{max}$ es la ganancia máxima de la antena.
### Pérdida por propagación
$$
L(dB) = 10\cdot \log\left( \frac{P_{t}}{P_{r}} \right)
$$
Donde $P_{t}$ es la potencia de salida del transmisor, y $P_{r}$ es la potencia de entrada al receptor.
#### Pérdida por espacio libre
$$
L_{bf}= \frac{P_{t}}{P_{r}} = \left( \frac{4\pi R}{\lambda} \right)^{2}
$$
La potencia no se disipa, sino que se distribuye a lo largo del frente de onda. A mayor distancia de la fuente, la potencia recibida es mucho menor ya que aumenta la superficie del frente de onda.
$$
L_{bf}[dB] = 32.5 + 20\cdot \log_{10}(f[MHz])+20\cdot \log_{10}(R[Km])
$$
El modelo de propagación por espacio libre, para la línea de vista (LOS), será aplicable a ambientes en el que no se encuentre ningún objeto que produzca en la señal: Absorción, Difracción, Reflexión, Dispersión.
$$
P_{r} = P_{t}\cdot \frac{g_{t}g_{r}\lambda^{2}}{(4\pi R)^{2}L}
$$
### Balance de potencia
$$
P_{r}[dBm] = P_{t}[dBm] + G_{t}[dB] + G_{r}[dB] - L_{t}[dB]
$$
![[Pasted image 20251115164324.png]]

Se esquematiza el sistema a partir del siguiente diagrama, donde $G$ son las ganancias de las antenas, y $L_{T}$ las pérdidas totales del sistema.
### Difracción por un filo de cuchillo
La difracción por un filo de cuchillo es un modelo clásico que describe cómo una onda electromagnética se **dobla** al encontrarse con un obstáculo con un borde agudo, como un filo de cuchillo.

En la práctica se utilizan las siguientes expresiones:
$$
L_{D}(v) = 
\begin{cases}
6.9 + 20\cdot \log(\sqrt{ (v-0.1)^{2}+1 } + v-0.1)\,dB \qquad v>-0.7 \\
0\, dB \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad \qquad ~ ~ ~  v<-0.7
\end{cases}
$$
### Ecuación de radar
La expresión para la potencia recibida en el receptor será:
$$
P_{r} = \frac{P_{t}g^{2}\lambda^{2}(A_{blanco}\cdot \Gamma_{b}\cdot g_{blanco})}{(4\pi)^{3}R^{4}}
$$
Donde $\sigma = A_{blanco}\cdot \Gamma\cdot g_{blanco}$ es la sección eficaz del blanco.
### Radioenlace VHF-UHF
Banda: 150 MHz - 3000 MHz
#### Modelo de reflexión en tierra plana
$$
\Delta R = R_{1}+R_{2}-R_{0} = \frac{2h_{t}h_{r}}{R} \qquad \text{Diferencia de camino físico}
$$
Si $\vec{E}_d$ es el campo eléctrico por espacio libre, en la antena receptora el campo estará dado por:
$$\vec{E}_d = \vec{E}_0 e^{-j\beta R_0} e^{j\omega t} \qquad |\vec{E}_0| = \frac{\sqrt{30\,P_t}}{R_0}$$
La onda reflejada está dada por:
$$\vec{E}_r = \Gamma\, \vec{E}_0 e^{-j\beta (R_1 + R_2)} e^{j\omega t}
$$El campo resultante:
$$\vec{E} = \vec{E}_d + \vec{E}_r
= \vec{E}_0 e^{-j\beta R_0} e^{j\omega t}
\left( 1 + \Gamma e^{-j\beta (R_1 + R_2 - R_0)} \right)$$
La diferencia de camino óptico es:
$$\Delta = \beta (R_1 + R_2 - R_0)
= \frac{2\pi}{\lambda}(R_1 + R_2 - R_0)
\approx \frac{2\pi}{\lambda} \cdot \frac{2h_t h_r}{R}
= \frac{4\pi h_t h_r}{\lambda R}
$$
Finalmente:
$$\vec{E} = \vec{E}_0 e^{-j\beta R_0} e^{j\omega t}
\left( 1 + \Gamma e^{-j\Delta} \right)
$$
**Zona de interferencia o visibilidad**
Sea la onda:
$$
\vec{E} = \vec{E}_0 + \vec{E}_0\, \Gamma e^{-j\Delta}
\qquad \text{(Onda directa + Onda reflejada)}
$$
Sabiendo que el coeficiente es complejo: $\Gamma = |\Gamma|\, e^{-j\phi}$, el campo queda tal que:
$$
\vec{E} = \vec{E}_0 + \vec{E}_0 |\Gamma| e^{-j(\Delta + \phi)}
\qquad , \qquad \alpha = \phi + \Delta
$$
De esta manera, el módulo del campo será:
$$
|\vec{E}| = |\vec{E}_0| \left| 1 + |\Gamma| e^{-j\alpha} \right|
= |\vec{E}_0|\, |F_i|
$$
Se define el factor de interferencia como:
$$
|F_i| = \sqrt{1 + |\Gamma|^2 + 2|\Gamma| \cos\!\left( \frac{4\pi h_t h_r}{\lambda R} + \phi \right)}
$$
Este factor contará con máximos y mínimos, tal que:
$$
\begin{align}
\text{Máximos} \qquad \alpha=2\pi m',\quad  m'=1,2,3,\dots \\
\text{Mínimos} \qquad \alpha=(2m'+1)\pi, \quad m'=1,2,3,\dots
\end{align}
$$
![[Pasted image 20251115174411.png#center|300]]
El campo resultante de la interferencia entre el campo directo y el reflejado, suponiendo incidencia rasante será:
$$
|\vec{E}| = 2|E_{0}|\left|sen\left( \frac{\Delta}{2} \right)\right| 
$$
Si $\Delta \leq 0.1$ (enlaces tierra-tierra):
$$
|\vec{E}| = \frac{4\pi h_{t}h_{r}\sqrt{ 30P_{t}g_{t} }}{\lambda R^{2}}
$$
La potencia recibida resulta:
$$
P_{r} = (Pg_{t})g_{r} \frac{(h_{t}h_{r})^{2}}{R^{4}} \quad P_{r(L_{bf})} =\frac{Pg_{t}g_{r}\lambda^{2}}{16\pi^{2}R^{2}}
$$
Para los distintos escenarios, se puede utilizar la siguiente tabla:
$$
P_{r} = P_{t} \frac{g_{t}g_{r}\lambda^{2}}{(4\pi)^{2}R^{n}L}
$$![[Pasted image 20251115175355.png#center|400]]
### Radio horizonte
Es la distancia máxima en la línea de visión hacia el horizonte.
![[Pasted image 20251115175636.png#center|300]]
Si dos torres tienen la altura suficiente, se puede ganar mayor línea de visión. El cálculo que relaciona la altura y distancias de las torres será:
$$
Rh = Rh_{1}+Rh_{2} = \sqrt{ 2ka } (\sqrt{ h_{1} } + \sqrt{ h_{2} })
$$
![[Pasted image 20251115180208.png#center|300]]
### Fenómenos que afectam la propagación de ondas electromagnéticas
- Reflexión: Cambio abrupto de la dirección de propagación en la interfase entre dos medios. Se presenta cuando la onda incide sobre objetos de tamaños mayores que la longitud de onda.
- Scattering o Dispersión: Ocurre cuando el medio por el cual viaja la onda consiste de objetos pequeños comparados con longitud de onda y el número de obstáculos por unidad de volumen es grande.
- Refracción: Cambio en la dirección de propagación debido al cambio del índice de refracción. 
- Difracción: Ocurre cuando la ruta entre Tx y Rx está obstruida por superficies de forma irregular (puntas) o la superficie terrestre, la onda bordea el obstáculo para alcanzar la zona de sombra.
![[Pasted image 20251115180439.png#center|120]]
### Atenuación por gases e hidrometeoros
**Para $f<3GHz$ → La atmósfera apenas atenúa**.
**Para $f>3GHz$ → Hay atenuación por lluvia, niebla y gases**.
