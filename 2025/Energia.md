### Potencial y trabajo
El trabajo realizado para traer una carga $q$ desde $\infty$ hasta el punto $P$, donde existe un campo $E$ creado por una distribución de cargas estática $\rho$ está dado por:
$$
W^{ext} = \int_{inf}^{P} \vec{F}_{ext}\cdot d\vec{l} = -\int_{\infty}^{P} \vec{F}_{e}\cdot d\vec{l} = -q \int_{\infty}^{P} \vec{E}\cdot d\vec{l} = q\cdot V(P)
$$
Por el principio de conservación de la energía $\Delta U+W_{e}=0$, entonces:
$$
U(r) = q\cdot V(r)
$$
#### Energía electroestática de un conjunto discreto de cargas
$$
U_{e} = \frac{1}{2} \sum_{i=1}^{N} q_{i}V(\vec{r}_{i})
$$
#### Energía electroestática de una distribución continua de carga
$$
U_{e} = \frac{1}{2} \int_{V'} \rho(\vec{r}')V(\vec{r}')  \, dv' 
$$
#### Relación entre la energía electroestática y el campo
En todo el espacio se cumple que:
$$
U_{e} = \frac{1}{2} \int \vec{D}\cdot \vec{E} \, dv = \int w_{e} \, dv  
$$
Donde $w_{e}$ es la densidad de energía electroestática por unidad de volumen $\left[ \frac{J}{m^{3}} \right]$

Utilizando la relación constitutiva (medio L.I.H) $D=\varepsilon E:$
$$
w_{e}=\frac{1}{2}\varepsilon|E|^{2} \longrightarrow U_{e} = \frac{\varepsilon}{2}\int |E|^{2} \, dv 
$$
Es equivalente expresar la densidad de energía por unidad de volumen como $\frac{dU_{e}}{dv} = \frac{1}{2}\varepsilon|E|^{2}$
#### Dieléctricos
Para los dieléctricos, el vector $\vec{D}$ se expresa mediante la relación $\vec{D} = \varepsilon_{0}\vec{E}+\vec{P}$, por lo tanto, la energía electroestática será:
$$
U_{e} = \frac{1}{2} \left( \int \varepsilon_{0}|\vec{E}|^{2} \, dv + \int \vec{P}\cdot \vec{E} \, dv  \right)
$$
Donde la primer integral es la energía requerida para ‘armar’ el campo en el vacío, y la segunda es la energía requerida para polarizar el dieléctrico.
#### Energía electroestática en un capacitor
$$
U_{e} = \frac{1}{2} Q \Delta V = \frac{1}{2} C\Delta V^{2}
$$
#### Principio de los trabajos virtuales
- N conductores cargados en equilibrio estable.
- Teorema de Earnshaw: Los conductores cargados no pueden estar en equilibrio estable si están sometidos únicamente a fuerzas eléctricas.
- Hay fuerzas mecánicas que contrarrestan las eléctricas.
- Se retira por un tiempo infinitesimal la ligadura mecánica que mantiene sujeto a uno de los conductores.
- Dicho conductor experimenta un desplazamiento infinitesimal (virtual) debido a la fuerza eléctrica que actúa sobre él y esta fuerza eléctrica realiza un trabajo $dW$.
- Al mismo tiempo de producirse el desplazamiento infinitesimal la energía electrostática almacenada en el conjunto de conductores sufre una variación $dU_{e}$.
- Se debe cumplir el principio de conservación de la energía.

Hay dos casos posibles:
##### A carga constante (sistema aislado)
Como el sistema está aislado, el trabajo mecánico se realiza a expensas de la $U_{e}$
$$
dU_{e} + dW = 0 \longrightarrow

\text{Donde } 
\begin{cases}
dW = \vec{F}_{e}\cdot d\vec{l} \\
dU_{e} = \nabla U_{e}\cdot d\vec{l}
\end{cases}
\quad
\longrightarrow 
\quad
\vec{F}_{e}=-\nabla U_{e}\bigg{|}_{Q=cte}
$$
![[Ejemplo - Fuerza entre placas de un cap Q=cte]]
##### A potencial constante
Al desplazar un conductor, varía la carga $Q_{j}$ sobre los conductores. Si la carga $Q_{j}$ pasa a ser $Q_{j} + dQ_{j}$, el generador debe trasladar $dQ_{j}$ desde el potencial $0$ hasta $V_{j}$, realizando trabajo $dW_{g}$. Por lo tanto, de acuerdo al principio de conservación de la energía:
$$
dW_{g} = dU_{e} + dW \Rightarrow \vec{F}_{e} = \nabla U_{e}\bigg{|}_{V=cte}
$$
#### Fuerza sobre un dipolo
$$
U_{e_{dipolo}} = q(\underbrace{V(P_{1})-V(P_{2})}_{dV=\nabla V\cdot\Delta \vec{r}}) \simeq q\Delta \vec{r}\cdot \nabla V = \vec{p}\cdot \nabla V = -\vec{p}\cdot \vec{E}_{ext}
$$
Como $\vec{F}=-\nabla U_{e}$, tenemos que:
$$
\vec{F}_{dipolo} = \nabla(\vec{p}\cdot \vec{E}_{ext})
$$
Siendo $p$ cte.
![[Pasted image 20250815161852.png#center|300]]
