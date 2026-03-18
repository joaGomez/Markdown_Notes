Campo constante en el tiempo → $\frac{\partial}{\partial t}=0$

Hans Oersted encuentra experimentalmente la conexión entre la electricidad y el magnetismo, dando origen al electromagnetismo. Luego, a partir de publicaciones importantes en el campo, como la ley de Biot Savart, o la ley de Ampère, se propone un modelo teórico del magnetismo, y define como fuente fundamental la corriente eléctrica.
### Intensidad y densidad de corriente
En un conductor, se define la densidad de corriente como $\vec{J}=\rho \vec{v}$, por lo que la intensidad de corriente se puede expresar como:
$$
I = \int_{A} \vec{J}\cdot \hat{n}\, dS 
$$
### Ley de Ampère de la fuerza
A partir de sus experimentos, Ampère realiza las siguientes observaciones:
- Dos conductores paralelos por los que circula corriente en el mismo sentido **se atraen**.
- Dos conductores paralelos por los que circula corriente en sentidos opuestos **se repelen**.
La expresión para definir la fuerza que actúa sobre elementos con corriente se representa diferencialmente como:
$$
d\vec{F}_{12} = \frac{\mu_{0}}{4\pi} \cdot \frac{I_{2}\vec{dl_{2}}\times(I_{1}\vec{dl_{1}}\times \hat{r}_{12})}{r_{12}^{2}}
$$
Donde $\mu_{0}=4\pi\cdot 10^{-7} \text{ H/m}$ es la permeabilidad del espacio libre.
### Ley de Biot-Savart
Se define la densidad de flujo magmético como el número de líneas por unidad de área
$$
\vec{B}_{\Gamma}(\vec{r}) = \frac{\mu_{0}}{4\pi} \cdot \oint_{\Gamma'} \frac{I'dl'\times(\vec{r}-\vec{r}')}{(\vec{r}-\vec{r}')^{3}}
$$
Donde se cumple el principio de superposición, y $[B]=\frac{N}{Am}=T$ (tesla).

Para una distribución en volumen de corriente ($J$):
$$
\vec{B}(\vec{r})= \frac{\mu_{0}}{4\pi} \int_{V'} \frac{\vec{J}(\vec{r}')\times \vec{R}}{R{^{3}}}  \, dv' 
$$
Para una distribución superficial de corriente ($J_{s}$):
$$
\vec{B}(\vec{r})= \frac{\mu_{0}}{4\pi} \int_{S'} \frac{\vec{J_{s}}(\vec{r}')\times \vec{R}}{R{^{3}}}  \, ds' 
$$
#### Flujo magnético
A partir de la densida de flujo magnético $B$, se puede hallar la expresión para el flujo magnético:
$$
\phi_{m} = \int_{S}\vec{B}\cdot d\vec{S} 
$$
Las unidades que se utilizan son $Wb$ (Weber), o $Mx$ (Maxwell). Estas unidades nacen de la representación de la densidad de flujo magnético. De acuerdo a la magnitud del campo, hablaremos de Tesla o de Gauss. La relación entre estos es de $1T=10^{4}G$. 
$$
[B]=\frac{Wb}{m{^{2}}} = T \qquad [B]=\frac{Mx}{cm^{2}} = G
$$
### Fuerza sobre una carga en movimiento
Una carga en movimiento, en presencia de un campo $B$, experimenta una fuerza dada por:
$$
\vec{F}_{m} = q\vec{v}\times \vec{B}
$$
Dado que la fuerza es perpendicular a la velocidad → El trabajo es nulo: $W=\int \vec{F}_{m}\cdot d\vec{r}$

Para un elemento diferencial de corriente, inmerso en una región donde existe una densidad de flujo magnético, el diferencial de fuerza que experimenta será:
$$
d\vec{F}=\vec{v}~dq\times \vec{B}= \frac{d\vec{l}}{dt}\times \vec{B}=Id\vec{l}\times \vec{B} \to \vec{F}=I \int_{C} d\vec{l}\times \vec{B} 
$$
### Fuerza de Lorentz
Si una carga puntual se mueve en una región donde existen un campo eléctrico y uno magnético, la carga experimenta una fuerza dada por:
$$
\vec{F}=\vec{F}_{e}+\vec{F}_{m} = q(\vec{E}+\vec{v}\times \vec{B})
$$
### Ley de Gauss para el magnetismo
Dado que las líneas de campo magnético son cerradas, el flujo magnético es nulo.
$$
\phi_{m} = \oint_{S} \vec{B}\cdot d\vec{S} = \int_{V} \nabla\cdot \vec{B}  \, dV = 0 
$$
Como consecuencia → No existe el monopolo magnético.
$$
\nabla\cdot \vec{B}=0 \qquad \text{Segunda ecuación de Maxwell}
$$
### Ley de Ampère
$$
\begin{split}
& \oint_{C} \vec{B}\cdot d\vec{l} = \mu_{0}I_{enc} \qquad & \text{Forma integral} \\
& \nabla \times \vec{B} = \mu_{0}\vec{J} & \text{Forma diferencial}
\end{split}
$$
### Vector potencial magnético
La divergencia de un campo vectorial es nula. Por lo tanto, dado que la divergencia de la densidad de flujo magnético es nula, se puede expresar a $\vec{B}$ como el rotor de un campo vetorial.
$$
\nabla\cdot \vec{B}=0 \Rightarrow \vec{B}=\nabla \times \vec{A}
$$
Donde $\vec{A}$ es el campo vectorial, y será conocido como el potencial magnético ($[A]=\frac{Wb}{m}$).

Además, si trabajamos el rotor de $\vec{B}:$
$$
\begin{split}
\nabla \times \vec{B}= \mu_{0}\vec{J} \to \nabla \times \nabla \times \vec{A} = \mu_{0}\vec{J} \\

\nabla \times \nabla \times \vec{A}=\nabla(\nabla\cdot \vec{A})-\nabla^{2}\vec{A} = \mu_{0}\vec{J}
\end{split}
$$
Dado que $\nabla\cdot \vec{A}$ no está definida, se le asigna arbitrariamente 0, por lo tanto, de la expresión anterior queda:
$$
\nabla^{2}\vec{A}= - \mu_{0}\vec{J}
$$
La expresión resultante es similar a la ecuación de Poisson, y su solución será:
$$
\vec{A}(\vec{r}) = \frac{\mu_{0}}{4\pi} \int_{V'} \frac{\vec{J}(\vec{r}')}{R} \, dv' 
$$
- Par una distribución superficial de corriente:
$$
\vec{A}(\vec{r}) = \frac{\mu_{0}}{4\pi} \int_{S'} \frac{\vec{J_{s}}(\vec{r}')}{R} \, ds' 
$$
- Para una línea de corriente:
$$
\vec{A}(\vec{r}) = \frac{\mu_{0}I}{4\pi} \int_{L} \frac{d\vec{l}}{R} 
$$
### Desarrollo multipolar
Para el desarrollo de una teoria multipolar, el término multipolar en la expresión de $\vec{A}_{4}(\vec{r})$ se anula, ya que no  existe el monopolo magnético. 

En particular, para el caso del dipolo magnético:
$$
\vec{A}_{dip}(\vec{r}) = \frac{\mu_{0}}{4\pi}\cdot \frac{\vec{m}\times\hat{r}}{r^{2}}
$$
El momento magnético de la espira será:
$$
\vec{m}=I\vec{S}
$$
Para una espira plana de cualquier forma: $\vec{m} = IA\hat{n}=I\vec{S}$
#### Para puntos lejanos al dipolo
Se cumplirá que:
$$
\begin{split}

\vec{A}(\vec{r}) = \frac{\mu_{0}}{4\pi}\cdot \frac{m\cdot sen~ \theta}{r^{2}}\hat{\phi} \\ 

B_{dip} (\vec{r}) \simeq \frac{\mu_{0}}{4\pi}\left[ \frac{3(\vec{m}\cdot \hat{r})\cdot \hat{r}}{r^{3}} - \frac{\vec{m}}{r^{3}} \right]
\end{split}
$$
![[Ej_Emag_Espira]]
### Materiales magnetizables
En las substancias magnéticas existe un momento dipolar magnético total del átomo no nulo:
$$
m_{atóico} = 10^{-23} \frac{A\cdot m^{2}}{\text{átomo}}
$$
Para el caso de los materiales magnetizables, se cumple que:
$$
\vec{B}=\vec{B}_{ap}+\vec{B}_{m}
$$
### Vector magnetización
Se define el vector magnetización como:
$$
\vec{M} = N\cdot<\vec{m}> = \frac{d\vec{m}}{dv'}
$$
Siendo $N$ el número de dipolos por unidad de volumen, y $<m>$ el momento dipolar promedio de los dipolos.
$$
\begin{split}

d\vec{A}_{m} & = \frac{\mu_{0}}{4\pi} \vec{M} \times \frac{\vec{R}}{R^{3}}dv' \\ \vec{A}_{m} (\vec{r}) = \frac{\mu_{0}}{4\pi} \int_{V'} \frac{\vec{M}(\vec{r}')\times \vec{R}}{R^{3}} \, dv' &= 
\frac{\mu_{0}}{4\pi} \int_{V'} \frac{\nabla'\times \vec{M}}{R} \, dv' + \frac{\mu_{0}}{4\pi} \oint_{S'} \frac{\vec{M}\times \hat{n}}{R} \, ds'
\end{split}
$$
Comparando con la expresión de $\vec{A}(\vec{r})$, se pueden representar las siguientes identidades para un material magnetizado:
$$
\begin{split}
& \vec{J}_{m} = \nabla \times \vec{M} \qquad & \text{Densidad de corriente volumétrica equivalente} \\
& \vec{J}_{ms} = \vec{M}\times \hat{n} \qquad & \text{Densidad de corriente superficial equivalente}
\end{split}
$$
![[Pasted image 20250826095542.png#center]]
**Observaciones:**
- **Magnetización uniforme** → $\vec{j}_{m}=0$
- **Magnetización no uniforme** → $\vec{j}_{m} \neq 0$
### Ley de Ampère para medios magnéticos
$$
\begin{split}
\nabla \times \vec{B}=\mu_{0}(\vec{J}+\vec{J}_{m}) = \mu_{0}\vec{J}+\mu_{0}\nabla \times \vec{M} \\ 
\nabla \times(\vec{B}-\mu_{0}\vec{M}) = \mu_{0}\vec{J} \to \nabla \times\underbrace{\left( \frac{\vec{B}}{\mu_{0}} -\vec{M}\right)}_{\vec{H}} = \vec{J}
\end{split}
$$
Se define $H$ como la intensidad del campo magnético, y sólo depende de las $J$ libres ($[H]=\frac{A}{m}$).
$$
\vec{H}=\frac{\vec{B}}{\mu_{0}}-\vec{M} \qquad \nabla \times \vec{H}=\vec{J} \qquad \nabla\cdot \vec{H}=-\nabla\cdot \vec{M}
$$
En situaciones de alta simetría, se cumple que $\nabla\cdot \vec{M}=0$, y se puede calcular $\vec{H}$ en función de las $J$ libres: $\oint_{c}\vec{H}\cdot d\vec{l} = \int_{s} \vec{J}\cdot d\vec{s} = I_{enc}$
### Permeabilidad magnética
La magnetización tiene que ser función del campo aplicado → Se consigue la siguiente relación constitutiva:
$$
\vec{M} = \mathcal{X}_{m}\vec{H}
$$
Donde $\mathcal{X}_{m}$ es la susceptibilidad magnética del material.

- Si $\mathcal{X}_{m}$ es un escalar → ($M\parallel H$) → Medio isótropo.
- Si $\mathcal{X}_{m}$ no es función de la posición → Medio homogéneo.

De la expresión para $\vec{H}$ se puede llegar a la siguiente relación constitutiva:
$$
\vec{H}= \frac{\vec{B}}{\mu_{0}} -\vec{M} \to \vec{B}=\mu_{0}(\vec{H}+\vec{M})= \mu_{0}(1+\mathcal{X}_{m})\vec{H}=\mu \vec{H}
$$
Donde se utilizó $\vec{M} = \mathcal{X}_{m}\vec{H}$. Además, se cumple que: $\mu_{r}= \frac{\mu}{\mu_{0}}=1+\mathcal{X}_{m}$
### Condiciones de contorno
$$
\begin{split}
B_{2n}=B_{1n} \to \hat{n}\cdot(\vec{B}_{2}-\vec{B}_{1})= 0 \quad \text{La intensidad de flujo magnético es continua}\\

\mu_{2}\cdot H_{2n} =\mu_{1}\cdot H_{1n} \quad \text{La intensidad del campo magnético es discontinua}

\end{split}
$$
A partir de $\vec{B}=\mu_{0}(\vec{H}+\vec{M})$ y $B_{2n} = B_{1n}$, entonces:
$$
(\vec{H}_{2n}-\vec{H}_{1n}) = - (\vec{M}_{2n}-\vec{M}_{1n})
$$
### Densidad de corriente superficial
$$
I = \int_{S} \vec{J}\cdot d\vec{S} = J_{s}\cdot\Delta l \to \vec{J}_{s} = H_{2t} -H_{1t} = \hat{n}\times (\vec{H}_{2}-\vec{H}_{1})
$$
### Apantallamiento magnético
Un material de alta permeabilidad magnética, reduce significativamente la penetración del campo magnético a su interior.

![[Pasted image 20250826121308.png#center|450]]
### Clasificación de sustancias magnéticas
- **Momentos magnéticos permanentes** → Paramagnéticos y ferromagnéticos.
- **Sin momentos magnéticos permanentes** → Diamagnéticos.

![[Pasted image 20250826121114.png#center]]

Los materiales superconductores (tipo I) son diamagnéticos perfectos → $\mathcal{X}_{m}=-1$ → $\vec{B}_{m}=-\vec{B}_{0} \to \vec{B}_{t}=0$
![[Pasted image 20250826121518.png#center]]
### Imán permanente
Los materiales que permanecen magnetizados en ausencia del campo magnético exterior se denominan imanes permanentes.
- **Remanencia ($M_{0}$)** → Índice de la habilidad del material como imán permanente.
- **Coercitividad ($H_{c}$)** → Índice de la habilidad del imán para soportar factores desmagnetizantes.

*Es deseable que sean elevadas*.
### Flujo magnético
El flujo magnético producido por la corriente $I_{1}$ sobre el circuito $C_{2}$ está dado por:
$$
\phi_{12} = \int_{S_{2}} \vec{B}_{1}\cdot d\vec{s}_{2}
$$
Si el circuito $C_{2}$ tiene $N_{2}$ espiras y el circuito $C_{1}$ tiene $N_{1}$, el flujo está dado por:
$$
\Lambda_{12} = N_{1}\phi_{12}=N_{1} \int_{S_{2}} \vec{B}_{1}\cdot d\vec{s}_{2}
$$
Se define la **inductancia mutua** como:
$$
M_{12} = \frac{N_{2}\Lambda_{12}}{I_{1}}
$$
### Autoinductancia
La autoinductancia puede definirse como el flujo sobre un circuito producido por la propia corriente → Es un caso particular de la inductancia mutua.
$$
L = M_{11} = \frac{\Lambda}{I} = \frac{N^{2}\phi}{I} 
$$
![[Ejemplo - autoinductancia de un solenoide]]
### Energía almacenada en un campo magnético
La energía magnética almacenada en el campo magnético en un volumen $V$, está dada por:
$$
U_{m} = \frac{1}{2} \int_{V} \vec{B}\cdot \vec{H}  \, dv = \frac{1}{2} \int_{V} \mu H^{2} \, dv 
$$
La densidad de energía magnética es:
$$
w = \frac{U_{m}}{V} = \frac{1}{2} \mu H^{2}
$$
### Energía almacenada en una inductancia
La energía magnética almacenada en una inductancia está dada por:
$$
U_{m} = \frac{1}{2} LI^{2}
$$
De esta expresión, podemos reescribir la autoinductancia como:
$$
L = \frac{2U_{m}}{I^{2}} = \frac{\int_{V} \vec{B}\cdot \vec{H}  \, dv }{I^{2}}
$$
![[EJEMPLO - autoinductancia de un cable coaxil]]
### Principio de trabajos virtuales
• $N$ espiras conductoras por las que circulan CC ($I_{j}$) en equilibrio estable. 
• Hay fuerzas mecánicas que contrarrestan las magnéticas. 
• Se retira por un tiempo infinitesimal la ligadura mecánica que mantiene sujeto a una de las espiras. 
• Dicha espira experimenta un desplazamiento infinitesimal (virtual) debido a la fuerza magnética que actúa sobre ella y esa fuerza magnética realiza un trabajo mecánico $dW$. 
• Al mismo tiempo de producirse el desplazamiento infinitesimal la energía magnetostática almacenada en el conjunto de espiras sufre una variación $dU_{m}$. 
• Se debe cumplir el principio de conservación de la energía.

De estas, se pueden separar en dos casos:
1) Espiras con flujo constante:
Como el sistema está aislado → El trabajo mecánico se realiza a expensas de la $U_{m}$
$$
\vec{F}_{m} = - \nabla U_{m}\bigg{|}_{\phi=cte}
$$
2) Espiras con intensidad de corriente constante:
$$
\vec{F}_{m} = \nabla U_{m}\bigg{|}_{I=cte}
$$
Si en lugar de un desplazamiento virtual se produce una rotación virtual $d\varphi_{z}$ alrededor del eje z debida a la cupla $N_{m}$
3) Flujo constante:
$$
N_{mz} = - \frac{\partial U_{m}}{\partial \varphi_{z}}\bigg{|}_{\phi=cte}
$$
4) Intensidad de corriente constante:
$$
N_{mz} = \frac{\partial U_{m}}{\partial \varphi_{z}}\bigg{|}_{I=cte}
$$
### Energía magnetostática de un dipolo
$$
U_{m} = -\vec{m}\cdot \vec{B}_{ext}
$$
### Fuerza sobre un dipolo
Dado que  el dipolo tendrá flujo constante:
$$
\vec{F}_{m} = \nabla(\vec{m}\cdot \vec{B}_{ext})
$$
### Tipos de imanes
![[Pasted image 20250829092552.png#center|500]]