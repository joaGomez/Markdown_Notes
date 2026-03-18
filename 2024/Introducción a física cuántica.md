### Radiación de cuerpo negro
Un objeto a cualquier temperatura emite ondas electromagnéticas (*Luz, UV, Infrarrojo*) en la forma de **radiación térmica** desde la superficie. Las características de esta radiación dependen de la temperatura y de las propiedades del objeto.

**Obs:** La radiación consiste en una distribución de longitudes de onda continuas desde todas las partes del espectro electromagnético.

**Def:** Un **cuerpo negro** es un sistema ideal que absorbe toda la radiación incidente. Y la radiación emitida por un cuerpo negro se conoce como *radiación de cuerpo negro*.

![[Pasted image 20240312110600.png#center|150]]		
*Esta figura muestra cómo varía la intensidad de la radiación de un cuerpo negro en relación con la temperatura y la longitud de onda*

Mediante experimentación, se hacen dos descubrimientos significativos:
- **La potencia total de la radiación emitida aumenta con la temperatura:** $\mathcal{P}=\sigma A eT{^{4}}$, donde $\mathcal{P}$ es la potencia (en watts) radiada en todas las longitudes de onda desde la superficie de un objeto, $\sigma = 5.67*10^{-8} \frac{W}{m^{2}.K^{4}}$ es la cte de Stefan-Boltzmann, $A$ es el área de la superficie del objeto en metros cuadrados, $e$ es la emisividad de la superficie y $T$ es la temperatura de la superficie en grados Kelvin. 
**Obs:** La emisividad de un cuerpo negro es $e=1$.
- **Ley de desplazamiento de Wien:** El pico de la distribución de la longitud de onda se desplaza hacia las longitudes de onda más cortas conforme aumenta la temperatura, mediante la expresión: $\lambda_{max} \ T=2.898*10^{-3} m.K$, donde $\lambda_{max}$ es la longitud de onda en la que el máximo de la curva y $T$ es la temperatura absoluta de la superficie del objeto que emite la radiación.
**Obs:** La longitud de onda en el pico es *inversamente proporcional* a la temperatura aboluta; es decir, conforme la temperatura aumenta , el pico se "desplaza" hacia longitudes de onda más cortas.

**Obs:**
- A temperatura ambiente $\to$ No parece resplandecer porque el pico está en la región infrarroja del espectro electromagnético.
- A una temperatura más elevada $\to$ Resplandece con un color rojo debido a que el pico está en la cercanía infrarroja, con alguna radiación en el extremo rojo del espectro visible.
- A temperaturas mucho mayores $\to$ Resplandece blanco porque el pico está en el intervalo visible, todos los colores son emitidos.

#### Ley de Rayleigh-Jeans
Resulta útil definir $I(\lambda, T)d\lambda$ como la intensidad o la potencia por unidad de área emitida en el intervalo de longitud de onda $d\lambda$. También se puede definir $I(\lambda, T)$ como la radiancia espectral.
$$I(\lambda, T)= \frac{2\pi ck T}{\lambda^{4}}$$
Donde $k$ es la *constante de Boltzmann* = $1.38* 10^{-23}\ \frac{J}{ K}$.

**Obs:** El cuerpo negro se representa como un orificio que conduce a una cavidad que contiene muchos modos de oscilación del campo electromagnético causados por cargas aceleradas en las paredes de la cavidad, lo que da como resultado la emisión de ondas electromagnéticas en todas las longitudes de onda.

##### Características del espectro de emisión
$$[I(\lambda, T)]= \frac{J}{m{^{2}}}    \qquad [I(f, T)]= \frac{J}{m{^{2}}s\ Hz}$$
El espectro de emisión depende de $T$, las propiedades de la superficie del radiador, y tiene muy poca dependencia del material.

1. Espectro continuo.
2. Fuertemente dependiente de la $T$: $I(\lambda, T), I(f, T)$ → Emiten de forma selectiva. $I(\lambda, T)d\lambda$ definida en el intervalo comprendido entre $\lambda$ y $\lambda + d\lambda$, donde $d\lambda$ es el ancho de banda.
3. Muy poco dependiente de las propiedades intrínsecas del radiador.

> Observaciones
> $[I(\lambda, T)d\lambda]= \frac{J}{m{^{2}}s}    \qquad [I(f, T)df]= \frac{J}{m{^{2}}s}$
> $\lambda = \frac{c}{f} \Rightarrow d\lambda = \frac{c}{f{^{2}}} df \Rightarrow \frac{|d\lambda}{df}|= \frac{c}{f^{2}}$
> $|I(\lambda, T)d\lambda|= |I(f, T)df|$
> $I(f,T)=I(\lambda, T) \frac{|d\lambda}{df}|=I(\lambda, T) \frac{c}{f^{2}}$

La radiación térmica emitida por un radiador llega a otro cuerpo mediante:
- Absorción ($a_{\lambda}(\lambda, T)$)
- Reflexión
- Transmisión
![[Pasted image 20240312132537.png#center|300]]
> El coeficiente entre la radiancia espectral de un cuerpo y el coeficiente de absorción del mismo cuerpo a la temperatura de equilibrio termodinámico y en intervalo $\lambda$ y $\lambda + d\lambda$, es independiente de la geometría y detalles de composición interna del cuerpo y es una función de $\lambda$.
> $$\frac{[I]_{1}}{[a_{\lambda}]_{1}}=\frac{[I]_{2}}{[a_{\lambda}]_{2}}=\frac{[I]_{3}}{[a_{\lambda}]_{3}}=\ ...\ = \frac{[I]_{m}}{[a_{\lambda}]_{m}}=I(\lambda, T)$$
> Donde si el cuerpo es ideal $\to a_{\lambda}=1 \quad \forall \lambda$.

#### Ley de Stefan-Boltzmann
Se define la radiancia como el área encerrada bajo la curva de la intensidad en función de la longitud de onda.
$$e_{total}=\int_{0}^ {\infty}I(\lambda, T)d\lambda=\sigma T^{4} \qquad [e_{total}]= \frac{J}{m^{2}s}$$
#### Ley de desplazamiento de Wien
Se define la función de Wien como la radiancia espectral, por lo que Wien para buscar el máximo la deriva y la iguala a 0, y obtenemos: $\lambda_{max} \ T=2.898*10^{-3} m.K$.

#### Hipótesis de Planck
- Wien → UV.
- Rayleigh-Jeans → Infrarrojo.
- $\lim_{\lambda\to0} I(\lambda, T) = \infty$ (Este fue un problema ya que ni Wien ni Rayleigh-Jeans podían explicarlo, "Catástrofe del ultravioleta").
- Si $e^{\frac{h c}{\lambda k T}}-1 \simeq \frac{h c}{\lambda k T}$ → Puedo usar R-J

Planck formuló dos hipótesis respecto de la naturaleza de los osciladores en la sparedes de la cavidad:
- La energía de un oscilador sólo puede tener ciertos valores discretos $E_{n}=nh f$, donde $n$ es un entero positivo conocido como **número cuántico**, $f$ es la frecuencia de la oscilación, y $h$ es la constante de Planck. Como la energía sólo puede tomar valores discretos, se dice que la energía está *cuantizada*. Cada uno de los valores discretos de energía corresponde a un *estado cuántico* diferente representado por su valor $n$ correspondiente.
- Los osciladores emiten o absorben energía cuando realizan una transición de un estado cuántico a otro. Esta diferencia de energía se denomina cuanto de energía.
	- Emisión: $2 \to 1: \Delta E=h f$
	- Absorción: $1 \to 2: \Delta E=h f$

###### Diagrama de nivel de energía

![[Pasted image 20240312140059.png#center|200]]
**Obs:** La energía promedio de una onda es la diferencia de energía promedio entre los niveles del oscilador, *ponderados de acuerdo con la probabilidad de la onda que se está emitiendo*.

**Obs:** La probabilidad de que un estado esté ocupado es proporcional al factor $e^{\frac{E}{k_{B}T}}$, donde $E$ es la energía del estado.
##### Función de Planck
$$I(\lambda, T)= \frac{2\pi h c^{2}}{\lambda^{5}(e^{\frac{h c}{\lambda kT}}-1)} \qquad h = 6.626*10^{-34} J.s$$
De donde si utilizamos que $f=\frac{c}{\lambda}=v$, entonces la función de planck nos queda tal que:
$$u(v, T) dv= \frac{8\pi h v^{3}}{c^{3}(e^{\frac{h v}{ kT}}-1)} dv$$
Y $u(v,T)dv$ es ña **densidad de energía** emitida con frecuencia $\in [v, v+dv]$. Además, recordemos que se cumple $|u(v,t)dv|=|u(\lambda,t)d\lambda|$.

> **Obs:**
> ![[Pasted image 20240312140828.png#center]]
### Efecto fotoeléctrico
A fines del siglo XIX, algunos experimentos demostraron que una luz incidente sobre ciertas superficies metálicas provoca la emisión de electrones de esas superficies. Este fenómeno se conoce como **efecto fotoeléctrico**, y los electrones emitidos se conocen como **fotoelectrones**.

Una observación que hizo Hertz mediante un experimento llamado *resonador de Hertz* fue que las superficies metálicas emiten cargas cuando se exponen a la radiación ultravioleta, que en otras palabras, esta radiación en forma de luz es capaz de arrancar partículas cargadas ($e^{-}$).

En 1905, unos años más tarde, Einstein nos invita a dejar de lado el concepto de onda electromagnética y nos lleva a entender que la radiación UV está conformada por paquetes de energía que liberan unas partículas llamadas fotones, que tienen $masa = 0$. A su vez, estos fotones salen con una energía de la magnitud de $E=h f$.
#### Resultados experimentales más importantes
1. Se define $f_{\mu}$ como la **frecuencia umbral**, la cual es propia de cada material (metal). Donde si la frecuencia propia de la radiación UV es mayor a esta ($f \geq f_{\mu}$) → Habrá efecto fotoeléctrico, es decir, la radiación ppodrá arrancar los $e{^{-}}$ del metal. Por el contrario, si $f < f_{\mu}$ → No habrá efecto fotoeléctrico ya que la radiación no será capaz de arrancar $e{^{-}}$.
**Obs:** Este efecto es *independiente* de la intensidad de la radiación, por lo que si varío la intensidad no veré manifestarse el efecto.
2. Se define $K_{e}$ como la energía cinética que tienen los $e{^{-}}$ al ser arrancados/emitidos. $K_{e}\in [0, K_{max}]$, donde $K_{max}$ va a ser diferente dependiendo del material con el que estemos trabajando, ya que está ligado a la frecuencia umbral ($f_{\mu}$), y como tiene relación directa con el efecto fotoeléctrico → También será independiente de la intensidad de la radiación.
	Si llamamos $w$ a la energía ligada al material, entonces estamos de acuerdo que podemos decir lo siguiente:
	- Si $h f \geq w:$ Hay efecto fotoeléctrico → El fotón es absorbido y el electrón es arrancado.
	- Si $h f < w:$ No hay efecto fotoeléctrico → El fotón **NO** es absorbido y no hay electrón arrancado.
	Mediante estas definiciones, podemos asociar lo siguiente:
	La energía del $e{^{-}}$ fuera del material se define como $K_{e}=h f - w$. Por lo tanto, podemos ver que $w$ va a variar, depende del material, y de la profundidad → Ahora entendemos como $K_{e}$ está en el intervalo $[0, K_{max}]$.
	**Obs:**
	- Si $hf = w$ → $K_{e}=0$, esto quiere decir que hemos podido arrancar el electrón, pero la energía cinética con la que sale es $0$.
	- Por otro lado, tenemos el valor mínimo que puede tomar $w$, esto es en la superficie del material, $w > w_{min}=\phi$. Además, $h f_{\mu}=\phi \to f_{\mu}= \frac{\phi}{h}$, y este es el caso de máxima energía cinética con la que sale arrancado el electrón: $K_{max}=h f - \phi$. A su vez, sigue valiendo que si $f\geq f_{\mu}$ hay E.F, y si $f<f_{\mu}$ no hay E.F.
	- Como dijimos antes, $w$ puede variar con la profundidad, aumentando así su valor, ya que la energía que *liga* el $e{^{-}}$ al material será mayor → $K_{e}<K_{max}$ a pesar de no haber variado la frecuencia ($f$). Esto quiere decir que la misma frecuencia que puede hacer que un $e{^{-}}$ de la superficie salga con energía cinética máxima, puede hacer que otro $e{^{-}}$, en mayor profundidad salga pero con menor energía cinética, hasta podría ser $0$, o incluso no ser capaz de arrancar el $e{^{-}}$.
3. No se pudo determinar el intervalo de tiempo entre la llegada de la radiación electromagnética al material y el posterior arranque de los electrones. Si se pudo ver experimentalmente que a mayor $I \Rightarrow \Delta t$ más chico, y a menor $I \Rightarrow \Delta t$ más grande.

**Obs:** La intensidad es proporcional al cuadrado de la amplitud del campo eléctrico.

Aunque mediante el concepto de fotón y paquetes de energía planteado por Einstein, podemos definir la intensidad de otra forma:
$$I=nh f$$
Siendo $n$ el numero de fotones sobre $m{^{2}\cdot}s$ y $h f$ la energía por cada fotón.

**Obs:** Inversamente a la frecuencia → Para que haya E.F: $\lambda < \lambda_{u}$.
#### Rayos X
Surge el descubrimiento de estos como la radiación producida por el choque de los rayos provenientes del cátodo en ánodo. Según Maxwell, los electrones chocaban contra la pantalla (ánodo), lo cual los frenaba → Perdían energía cinética.

##### Tubo de Coolidge
En este experimento, los rayos X debían ser no monocromáticos, ni colimados.

> **Observaciones del experimento**
> 1. Espectro de emisión continuo
> 2. $\lambda_{min} \sim \frac{1}{V}$
> 3. El espectro de emisión es independiente (los $e^{-}$) del material blanco.

Surge la **ley de Duane-Hunt**, donde descubren que $\lambda_{min}= \frac{h c}{eV}$.

**Obs:** Tras la colisión de un electrón con un átomo (estructura cristalina) → Se crea un fotón.

Cuando hay aceleración (o desaceleración) lineal/tangencial, no hay pérdida significativa de energía por radiación. Pero cuando la aceleración es normal (movimiento curvilíneo) → Hay suficiente pérdida de energía por radiación, lo que genera un fotón con energía $E= h f$, y el electrón queda con una energía cinética menor ($K_{e}^{'}<K_{e}$).

**Obs:** Si en la colisión electrón-átomo, el electrón pierde toda su energía cinética en un solo choque:
$$K_{e}^{'}
\begin{cases} 
V_{e}=K_{e} \\ 
K_{e}=h f_{max} \\ 
f_{max}= \frac{c}{\lambda_{min}} \\
\end{cases} \Rightarrow \lambda_{min}= \frac{h c}{eV}$$
**Obs:** La pérdida de energía es discreta → Si hay N choques → Hay N fotones con energía $h f$.
#### Efecto Compton
Este efecto ocurre en condiciones opuestas al tubo de Coolidge, donde para este caso, los rayos X deben ser monocromáticos y colimados.

![[Demo]]

> **Obs:**
> - $E=h f$ → Efecto fotoeléctrico.
> - $p= \frac{E}{C}= \frac{h}{\lambda}$ → Efecto Compton.

Para este efecto se tiene el siguiente escenario:

![[Pasted image 20240327143301.png#center|300]]

Donde un rayo incide con longitud de onda $\lambda_{0}$ y tras colisionar con un cristal de grafito, sale un fotón con ángulo $\theta \in [0,\pi]$.

Definimos el **desplazamiento de Compton** tal que $\Delta \lambda =\lambda^{'}-\lambda_{0}$, es independiente de $\lambda_{0}$ y aumenta con $\theta$.

![[Pasted image 20240327143345.png#center|400]]

Para un caso particular como lo es cuando fotón incidente colisiona con un electrón libre y en reposo. De esta colisión, surge un fotón dispersado con datos:  ($\theta, E^{'}= h f^{'}, p^{'}= \frac{h}{\lambda^{'}}$), y un electrón con velocidad $\vec{u}$. Donde vale la conservación de la energía y conservación del movimiento lineal.

Planteando esto último, obtengo que para que suceda el efecto Compton se debe cumplir que:
$$K_{e}= h f_{0}-h f^{'} → f_{0}>f^{'} → \lambda^{'}>\lambda_{0}$$
$$\Delta \lambda =\lambda^{'}-\lambda_{0}= \frac{h}{mc} (1-cos(\theta))= \lambda_{c}(1-cos(\theta))$$
Donde $\lambda_{c}=0.0243~ \mathring{A}$.

###### Casos límites
Si $\theta=\pi \Rightarrow \lambda^{'}= \lambda_{0} +2\lambda_{c}$ (Máximo)
Si $\theta=0 \Rightarrow \lambda^{'}= \lambda_{0}$ (Mínimo)

Por lo que podemos ver que para $\theta \in [0,\pi] → \Delta \lambda \in [0,2\lambda_{c}]$

Si $M >> m$, podemos considerar que es un núcleo o electrones ligados. En este caso:
$$\lambda_{c}= \frac{h}{Mc} \to 0 \Rightarrow \lambda^{'}\simeq \lambda_{0} ~\forall~ \theta$$
El efecto Compton **no es perceptible en el rango de longitudes de onda de la luz y el UV**. Pero si que lo es en el rango de los rayos X y rayos $\gamma$.
#### Producción de pares
Cuando tenemos un choque entre partículas → Se producen partículas.

Definimos un par de partículas como dos partículas, una partícula y su anti partículas. Algunas famosas son los pares: electrón-positrón, protón-antiprotón. Estas partículas cargadas tienen la misma masa y $|q|$, pero con distinto signo de la carga.

En la producción de pares hay interacción fotón con la materia y la conidición umbral. Además, hay conservación de la energía y del movimiento.

**Obs:** En la condición umbral, el par partícula-anti partícula + la partícula con la que interactua el fotón (esto vale si no es un núcleo), saldrán con la energía cinética mínima → Las tres partículas tendrán la misma energía cinética → Tendrán la misma cantidad de movimiento. Siempre y cuando no sea un nucleo el que interactúe con el fotón, ya que al tener masa distinta, no serán iguales, ni la energía, ni la cantidad de movimiento. Si es un núcleo es más conveniente trabajar con sistema de centro de momentos. Mientras que si es un electrón es más fácil trabajar con el sistema de laboratorio.
#### Aniquilación de pares
Interacción partícula-anti partícula → Se producen por lo menos dos fotones.
#### Dualidad onda-partícula
Se comienza a interpretar a la radiación electromagnética (LUZ/UV/RX) con un **concepto dual**, ya que se percibe como *onda (difracción)*, y como *fotón (E.F/E.C/P.P)*.

Para ambos modelos vale que: $\lambda = \frac{c}{f},~E= p~c$.

**Obs:** Si los efectos que produce la radiación electromagnética en su interacción con la materia están:
- Distribuidos → **Modelo de onda**.
- Localizados → **Modelos de fotón**.

Según Broglie, la materia(*partícula*, $m\neq 0$) también se podía estudiar con un concepto dual, y surge el **principio de complementariedad** por Bohr.
$$\lambda_{DB}= \frac{h}{p} \qquad E= h \cdot f_{DB}$$
> **Obs:**
> $p=m\cdot u \qquad 0<u<0.1c → E=K= \frac{p{^{2}}}{2m}$
> $p=\gamma\cdot m\cdot u \qquad 0.1c<u<c → \begin{cases}E^{2}=p^{2}c^{2}+E_{0}^{2} \\ K{^{2}}+2KE_{0}=p^{2}c^{2} \end{cases}$

**Obs:** $\lambda_{DB}$ no está vinculado a la forma o al tamaño de la materia, sino a su comportamiento.
#### Difracción de rayos X
![[Pasted image 20240331104027.png#center|300]]
Por la **condición de Bragg**, las longitudes de onda de los RX dispersados sólo pueden tomar valores discretos:
$$2dsen(\theta)=n\lambda \qquad n=1,2,3,...$$
##### Teoría de Fourier
Mediante la suma de ondas armónicas, con distinta amplitud y distinta frecuencia, a través de la superposición logramos formar un **paquete de ondas**, y se lográ identificar además de las propiedades de onda, se concibe como partícula, ya que la localización del paquete de ondas corresponde a la posición de la partícula.

A su vez, surge la definición de **rapidez de grupo**, es decir, la rapidez del paquete de ondas, y está expresada de la siguiente forma:
$$v_{g}= \frac{d\omega}{dk}=\frac{dE}{dp}=u$$
Estas igualdades surgen de las definiciones de: $\hbar\omega=hf=E=\frac{p^{2}}{2m}, ~\hbar k=\frac{h}{\lambda}=p$
### Principio de incertidumbre
La teoría cuántica dice que básicamente es imposible medir, simultáneas, la posición y la cantidad de movimiento de una partícula con una precisión infinita. Por el **principio de Heisenberg**, la incertidumbre $\Delta x$ de la posición de una partícula, y la incertidumbre $\Delta p_{x}$ de su cantidad de movimiento en la componente $x$, el producto de ambas incertidumbres no puede ser menor de $\frac{\hbar}{2}$:
$$\Delta x\Delta p_{x}\geq \frac{\hbar}{2}$$
**Obs:** Físicamente, es imposible medir de manera simultánea la posición exacta, y la cantidad de movimiento exacta de una partícula. Además, estas incertidumbres no se presentan debido a imperfecciones en los instrumentos de medición, sino que surgen debido a la estructura cuántica de la materia (*dualidad*).

$$Relaciones~de~incertidumbre \qquad 
\begin{split}
\Delta x\Delta p_{x}\geq \frac{\hbar}{2} \\
\Delta y\Delta p_{y}\geq \frac{\hbar}{2} \\
\Delta z\Delta p_{z}\geq \frac{\hbar}{2}
\end{split}$$
**Obs:** Podemos notar que como las incertidumbres de distintas componentes no tienen relación que las vincule, por lo que no hay restricciones debido a estas.

**Obs:** Es importante notar que si $\Delta p_{x}= 0 \Rightarrow \Delta x \to \infty$. Por lo dicho antes, no hay ninguna restricción con que simultáneamenrte $\Delta p_{x}=0 \land \Delta y=0$.

**Obs:** El principio de incertidumbre no afecta las interpretaciones clásicas de los objetos macroscópicos.

**Def:** Una consecuencia de la teoría de Fourier es $\Delta\lambda \neq 0 \Rightarrow \Delta p_{x} \neq 0 \Rightarrow \Delta x \not \to \infty$.

Otra forma de escribir el prinicipio de incertidumbre es mediante la relación de incertidumbres de energía y de tiempo. Ya que la energía se puede escribir como $E=hf$, entonces la relación de incertidumbre que nos queda es la siguiente:
$$\Delta E\Delta t \geq \frac{\hbar}{2}$$
**Obs:** $k = \frac{2\pi}{\lambda}$ y $\omega= 2\pi f$.