**Obs:** Al haber dopaje, va a haber diferencia de concentraciones y por lo tanto va a existir un movimiento de cargas (portadores).

**Recuerdo:** Una partícula cargada que está sometida a un campo eléctrico, va a estar sometida a una fuerza, del orden de la carga por el campo.
#### Corrientes de drift (arrastre)
Es el movimiento de una partícula cargada, en respuesta de un campo eléctrico aplicado. Estas partículas pueden ser tanto electrones como lagunas.

Acciones de portadores: Drift, Difusión, recombinación-generación. Siempre ocurren las tres en simultáneo, aunque hay una que tiene preponderancia.

La velocidad de drift va a estar limitada por las colisiones, ya que al tratarse de un red cristalina, es un sistema caótico y la velocidad máxima de los portadores va a estar limitada ($v_{dSAt})$.

**Obs:** La corriente eléctrica es la carga por unidad de tiempo que cruza una sección transversal de un determinado material, por lo tanto se puede demostrar que en un cristal tipo P la corriente de huecos en presencia de un campo eléctrico externo será:
$$I=\iint \vec{J}\cdot d\vec{s}=J\cdot A=q \cdot p \cdot v_{d} \cdot A$$
Donde $p$ es la concentración de huecos por unidad de volumen.

La velocidad de los portadores se va a comportar de la siguiente forma cuando está en presencia de un campo eléctrico:
$$\begin{split}
& v_{d}= \frac{\mu_{0}E}{^{\beta}\sqrt{1+(\frac{\mu_{0}E}{v_{sat}})^{\beta}}} =
\begin{cases}
\mu_{0}E,\quad E\to 0 \\ \\
v_{sat}, \quad E\to \infty
\end{cases} \\
& \beta = \begin{cases}1, \quad huecos \\ 2, \quad electrones \end{cases} \\
&[\mu]= \frac{cm^{2}}{V\cdot s}
\end{split}$$
La movilidad va a depender del tipo de portador (es distinta para electrones y para lagunas), varía con el dopaje del cristal, y también de la temperatura. La movilidad siempre es positiva.
$$\mu = \mu_{min}+ \frac{\mu_{0}}{1+(\frac{N}{N_{ref}})^{\alpha}}$$
**Obs:** A mayor concentración de impurezas ionizadas, aumenta el scattering → Disminuye la movilidad.

A mayor temperatura, más scattering → Debido al movimiento de la red → $\mu \alpha T^\frac{-3}{2}$. 

##### Corrientes de $e^{-}$ y $h^{+}$ 
$$\begin{split}

\vec{v}_{dp} = \mu_{p}\vec{E} \qquad \vec{J}_{p} = q\ p \ \vec{v}_{dp}= q\ p \ \mu_{p} \vec{E} \\
\vec{v}_{dn} = -\mu_{n}\vec{E} \qquad \vec{J}_{N} = -q\ n \ \vec{v}_{dn}= q\ n \ \mu_{n} \vec{E}

\end{split}$$
Tanto la corriente de drift de electrones como de lagunas tienen la misma dirección:
$$\vec{J} = \vec{J}_{p} + \vec{J}_{N} = q \vec{E}\cdot (p\ \mu_{p}+ n\ \mu_{n})$$
#### Conductividad
Como $\vec{J} = q \vec{E}\cdot (p\ \mu_{p}+ n\ \mu_{n}) \Rightarrow \sigma = q \ (p\ \mu_{p}+ n\ \mu_{n})$ (Ley de Ohm)
$$\sigma = \begin{cases}
q\ \mu_{n}N_{D}, \qquad tipo~N\\
q\ \mu_{p}N_{A}, \qquad tipo~P\\ 
\end{cases}$$

**Obs:** Elevando lo suficientemente la temperatura, todos los sc se vuelven intrínsecos.

La resistividad de un semiconductor está dada por:
$$\rho = \frac{1}{\sigma}= \frac{1}{q(\mu_{n}n+\mu_{p}p)} \equiv
\begin{cases} 
\frac{1}{q\mu_{n}N_{D}}, tipo-N \\ \\
\frac{1}{q\mu_{p}N_{A}}, tipo-P
\end{cases}$$
**Obs:** Un paralelepípedo semiconductor de área A ($A=\omega t$) y largo L tendrá una resistencia dada por $R=\rho \frac{l}{A} = \frac{l}{Aq\mu N}$
#### Efecto Hall
El campo de inducción magnética B incide perpendicularmente sobre el cristal y genera una fuerza de Lorentz sobre cada portador de carga. Por lo tanto, habrá una acumulación de portadores de carga en las caras opuestas. Dejando en la cara opuesta, impurezas donoras ionizadas (**fijas en la red cristalina**). Esa ionización de cargas va a dar origen a un campo eléctrico transversal y por ende a una nueva fuerza (pero esta vez de origen eléctrico) que seguirá aumentando hasta que ambas fuerzas estén en equilibrio ($\vec{f}_{B}+\vec{f}_{E}=0$).

•Este efecto permite determinar si el cristal es P o N!
$$ (Tensión~de~Hall) \qquad \qquad v_{H}= \frac{I}{qNt}\cdot B=V\cdot \mu \frac{\omega}{l}\cdot B$$
$$(Sensibilidad~de~Hall) \qquad \qquad S_{H}^{I}= \frac{1}{qNt},\quad S_{H}^{V}=\mu \frac{\omega}{l}$$
#### Difusión
En la difusión, las partículas tienden a expandirse y redistribuirse por agitación térmica, yendo a regiones de mayor concentración a regiones con menor concentración.

Ley de Fick: $\vec{F}=-D\vec{\nabla}\eta$ (Flujo de partículas)

##### Corrientes de difusión
La densidad de corriente eléctrica debido a la difusión de portadores en cristales semiconductores estará dada por la ley de Fick, multiplicando por la carga de cada portador:
$$\begin{split}
\vec{J}_{P|diff}=-qD_{P}\vec{\nabla}p \\
\vec{J}_{N|diff}=-qD_{N}\vec{\nabla}n
\end{split}$$
Donde $p$ y $n$ son respectivamente la concentración por unidad de volumen de lagunas y electrones, para un punto arbitrario del espacio. Y $D$ es el coeficiente de difusión y se puede calcular mediante la Ecuación de Einstein.
##### Ecuación de Einstein
La densidad de corriente eléctrica debido a la difusión de portadores en cristales semiconductores está dados por las siguientes expresiones:
$$\frac{D_{N}}{\mu_{n}}= \frac{kT}{q} \qquad \frac{D_{P}}{\mu_{p}}= \frac{kT}{q}$$
**Obs:** Teniendo en cuenta la difusión como el arrastre → La corriente total de un SC será:
$$\begin{split}
\vec{J}_{P}=\vec{J}_{P|drift}+\vec{J}_{P|diff}=q\mu_{p}p\vec{E}-qD_{p}\vec{\nabla}_{p} \\
\vec{J}_{N}=\vec{J}_{N|drift}+\vec{J}_{N|diff}=q\mu_{n}n\vec{E}+qD_{N}\vec{\nabla}_{n}
\end{split}$$
#### Recombinación y generación
•La generación es el proceso mediante el cual los pares electrón-laguna son generados.

•La recombinación es el proceso mediante el cual los pares electrón-laguna son aniquilados.

![[Pasted image 20240314201808.png#center]]

##### Generación y recombinación térmica
La recombinación de MINORITARIOS (electrones en cristales tipo P, o lagunas en cristales tipo N) se la considera dada por:
- $\frac{\partial p}{\partial t}|_{i-thermal(R-G)} = - \frac{\Delta p}{\tau_{p}}$ para los huecos en materiales de tipo-n
- $\frac{\partial n}{\partial t}|_{i-thermal(R-G)} = - \frac{\Delta n}{\tau_{n}}$ para los electrones en materiales de tipo-p
Donde $\tau$ es el tiempo de vida medio de dichos minoritarios.

**Ecuaciones de continuidad de la carga eléctrica:**
$$\begin{split}
\frac{\partial n}{\partial t}= \frac{1}{q} \nabla \cdot J_{N} + \frac{\partial n}{\partial t}|_{thermal(R-G)} + \frac{\partial n}{\partial t}|_{other\ processes} \\

\frac{\partial p}{\partial t}= -\frac{1}{q} \nabla \cdot J_{P} + \frac{\partial p}{\partial t}|_{thermal(R-G)} + \frac{\partial p}{\partial t}|_{other\ processes}
\end{split}$$
**Interpretación:** Si hay variación en la concentración de portadores en el tiempo, esta debe ser porque ya sea existe divergencia (derivadas espaciales) de la densidad de corriente eléctrica, o bien, hay una variación temporal de los portadores debido a la R-G térmica u otros procesos.

En el caso unidimensional, donde el único proceso extra además de la R- G  térmica  es  la  eventual  ionización  por  incidencia  de  fotones (fotogeneración), la ecuación de continuidad se reduce a:
**Minority carrier diffusion equations**
$$
\begin{split}
\frac{\partial \Delta n_{p}}{\partial t} = D_{N} \frac{\partial^{2} \Delta n_{p}}{\partial x^{2}} - \frac{\Delta n_{p}}{\tau_{n}} + G_{L} 
\\
\frac{\partial \Delta p_{n}}{\partial t} = D_{P} \frac{\partial^{2} \Delta p_{n}}{\partial x^{2}} - \frac{\Delta p_{n}}{\tau_{p}} + G_{L}
\end{split}$$
Donde $G_{L}=0$ si no hay fotogeneración.
#### Fotogeneración
La luz (fotones) que impacte en un cristal generará pares electrón-laguna. 
La intensidad de luz ($I_{0}$) decaerá exponencialmente dentro del cristal → Los fotones se irán absorbiendo a medida que penetran en el material e interaccionan con los átomos.
$$G_{L}(x,\lambda)=I_{0}e^{-\alpha x}$$
$$\frac{\partial p}{\partial t}|_{luz} = \frac{\partial n}{\partial t}|_{luz} = G_{L}(x, \lambda) = G_{L0}e^{-\alpha x}$$
#### Ecuaciones de continuidad
La carga eléctrica no se crea ni se destruye → Si la carga en un recinto varía en el tiempo, tiene que ser por la circulación de corriente (divergencia de $J$), la R-G térmica u otros procesos, como fotogeneración.
$$\begin{split}
\frac{\partial p}{\partial t}= -\frac{1}{q} \vec{\nabla} \cdot \vec{J_{P}} + \frac{\partial p}{\partial t}|_{thermal(R-G)} + \frac{\partial p}{\partial t}|_{luz}
 \\
\frac{\partial n}{\partial t}= \frac{1}{q} \vec{\nabla} \cdot \vec{J_{N}} + \frac{\partial n}{\partial t}|_{thermal(R-G)} + \frac{\partial n}{\partial t}|_{luz}

\end{split}$$
#### Difusión de minoritarios
•Asumimos bajo nivel de inyección ($Δp≪n_0$  y $Δn≪p_0$), que no hay $\vec{E}$ ni $\vec{B}$ y que la concentración de portadores no depende de la posición en el cristal.

•En el caso unidimensional, donde el único proceso extra además de la R-G térmica es la eventual ionización por incidencia de fotones (fotogeneración), la ecuación de continuidad se reduce a:

**Electrones en tipo P:** $\frac{\partial \Delta n_{p}}{\partial t} = D_{N} \frac{\partial^{2} \Delta n_{p}}{\partial x^{2}} - \frac{\Delta n_{p}}{\tau_{n}} + G_{L}$
**Lagunas de tipo N:** $\frac{\partial \Delta p_{n}}{\partial t} = D_{P} \frac{\partial^{2} \Delta p_{n}}{\partial x^{2}} - \frac{\Delta p_{n}}{\tau_{p}} + G_{L}$

Resolviendo sin pérdida de generalidad una de las dos ecuaciones y agregando la sig condición de contorno:
$$h^{+} en\ tipo \ N: \frac{\partial \Delta p_{n}}{\partial t} + \frac{\Delta p_{n}}{\tau_{p}}=+G_{L} \qquad \Delta p_{n}(t=0)=0$$
Resulta que la cantidad de lagunas aumenta de la siguiente forma:
$$\Delta p_{n}(t)=G_{L}\tau_{p}(1-e^{\frac{-t}{\tau_{p}}})$$
![[Pasted image 20240315081032.png#center]]
#### Longitud de difusión de minoritarios
Sin fotogeneración ($G_{L}=0$), en estado estacionario ($\frac{\partial \Delta p_{n}}{\partial t}=0$), y con las siguientes condiciones de contorno:
- $h{^{+}}$ en tipo N: $D_{P} \frac{\partial^{2} \Delta p_{n}}{\partial x^{2}} - \frac{\Delta p_{n}}{\tau_{p}}=0 \qquad \Delta p_{n}(x=0)=\Delta p_{n_{0}} \quad \Delta p_{n}(x\to \infty)=0$
**Obs:** La condición del infinito será utilizada para la resolución de las ecuaciones de diffusion en un diodo largo, pero no podrá ser utilizada en el caso de un diodo corto ni en la base de un transistor bipolar de juntura.

**Sol:** $\Delta p_{n}(x)=\Delta p_{n_{0}} e^{\frac{-x}{L_{P}}}$

**Longitud de difusión de $h{^{+}}$ en tipo N:** $L_{P}=\sqrt{D_{P}\tau_{P}}$
**Longitud de difusión de $e{^{-}}$ en tipo P:** $L_{N}=\sqrt{D_{N}\tau_{N}}$

![[Pasted image 20240315082917.png#center]]
##### Conclusiones
•Estudiamos la corriente de drift y vimos que la velocidad de los portadores puede limitarse dentro de un cristal, a diferencia de lo que pasa en el vacío.
•Analizamos la dependencia de la movilidad con parámetros constructivos como el dopaje y la temperatura.
•Definimos la resistividad y la conductividad de un cristal semiconductor en función de su dopaje.
•Estudiamos el efecto Hall en semiconductores, donde vimos que no es lo mismo utilizar una fuente de corriente o una de tensión para energizar el transductor.
•Definimos un nuevo mecanismo de circulación de corriente llamado difusión.
•Analizamos la R-G térmica y la fotogeneración. Resolvimos ejemplos básicos de cada caso.