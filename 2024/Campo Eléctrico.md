Los objetos pueden estar cargados positivamente o negativamente. Para entender un poco como interactúan estas cargas, si tenemos dos cargas de un mismo signo se repelen, y dos cargas de distinto signo se atraen.
Un aspecto importante de la electricidad es que la carga eléctrica se conserva, es decir, si froto un objeto contra otro, no se crea carga en este proceso. El estado de electrificación se debe a una transferencia de carga de uno de los objetos hacia el otro. Uno adquiere la parte de carga negativa y el otro adquiere la misma cantidad de carga pero positiva.
Dentro del sistema internacional de unidades (S.I), la unidad de medida de la carga eléctrica es el **Coulomb (C)**, y se define la carga fundamental *e* por: $$e=1,6 \ . \ 10^{-19} \ C$$
Y a partir de esta definición de la unidad, sabemos que $q_{e}=-e$ , es la carga del electrón y la del protón $q_{p}=+e$. Además, se concluyó que la carga eléctrica de cualquier objeto está cuantizada, siendo siempre múltiplo entero de *e*.
### Inducción
- Los **conductores** eléctricos son aquellos materiales en los cuales algunos de los electrones son libres, y pueden moverse a través del material.
- Los **aislantes** eléctricos son aquellos materiales en los cuales todos los electrones están unidos y no pueden moverse libremente a través del material.
- Hay un tercer grupo, denominado **semiconductores**, cuyas propiedades eléctricas se ubican entre los aislantes y los conductores.

La carga por inducción sucede cuando, por ejemplo, tengo una esfera conductora de carga neutra, y le acerco una varilla cargada cargada (No es necesario el contacto). Al acercarle la varilla, las cargas opuestas a las de la varillan se 'acercaran' a la superficie de la esfera, mientras que las cargas de mismo signo se alejaran, ya que se repelen. Si mantengo la varilla cerca de la esfera y momentaneamente conecto la esfera a tierra, ocasionando que mucha de la carga 'alejada' se marche por ese canal a tierra. Si luego quito la conexión con tierra y alejo la varilla, la esfera quedara cargada, opuesta a la carga de la varilla, pero cargada en fin, y ese proceso se llama carga por inducción.
## Fuerza de Coulomb
Por la ley de Coulomb, podemos conocer la magnitud de una fuerza eléctrica entre dos cargas puntuales, dada por la sig ec.:
$$F_{e}=k_{e}\ \frac{|q_{1}| \ |q_{2}|}{r^{2}}$$
Donde $k_{e}$ es la constante de Coulomb y se puede expresar como: $$k_{e}=\frac{1}{4\pi \epsilon_{0}}$$→ $k_{e}=8,9876 \ . \ 10{^{9}\ N\ . \ \frac{m^{2}}{C^{2}}}$ y $\epsilon_{0}=8.854 \ . \ 10{^{-12}}\ {\frac{C^{2}}{N\ . \ m^{2}}}$
## Partícula en un campo eléctrico
Si se coloca una carga arbitraria *q* en un campo eléctrico $\vec{E}$, ésta experimenta una fuerza eléctrica dada por: 
$$\vec{F_{e}}=q\vec{E}$$
###### Obs.
Si la carga es positiva, la fuerza tiene la misma dirección que el campo eléctrico. Mientras que si la carga es negativa, la fuerza y el campo tienen direcciones opuestas.

De esta expresión, puedo obtener el campo eléctrico en un punto a distancia $r$ de una carga $q$.
$$\vec{E}=k_{e}\ \frac{q}{r^{2}}\ \hat{r}$$
###### Obs.
A la hora de calcular un campo eléctrico, vale la superposición, por lo que el campo eléctrico total, o resultante, lo puedo pensar como la sumatoria de todos los campos eléctricos.
## Líneas de campo eléctrico
Las líneas de campo sirven para relacionar el campo eléctrico con una región del espacio.
- El vector $\vec{E}$ del campo eléctrico es tangente a la línea del campo eléctrico en cada punto. La dirección de la línea es igual al vector del campo eléctrico.
![[Pasted image 20230804184722.png | 200]]
###### Obs (Partículas cargadas en un campo uniforme)
$$\sum\limits \vec{F}=q\vec{E}=m\vec{a} \to \vec{a}=\frac{q\vec{E}}{m}$$
## Campo eléctrico de una distribución de carga continua
- **Densidad de carga volumétrica**: $\rho\equiv \frac{Q}{l}$
- **Densidad de carga superficial**: $\sigma\equiv \frac{Q}{A}$
- **Densidad de carga volumétrica**: $\rho\equiv \frac{Q}{V}$
 ###### Obs
 Si la carga no esta distribuida uniformemente: $$dq = \rho \ dV ,\quad dq = \sigma \ dA ,\quad dq = \lambda \ dl$$
 Además, como la carga no esta uniformemente distribuida → $d\vec{E}=k_{e}\ \frac{dq}{r^{2}}\ \hat{r}$, entonces el campo eléctrico quedará expresado de la siguiente forma:
 $$\vec{E}=\int d\vec{E}=\int k_{e}\ \frac{dq}{r^{2}}\ \hat{r}$$
## Ley de Gauss
Es el producto del campo eléctrico por el área perpendicular al mismo sobre una superficie dada, y se lo denomina **flujo de campo eléctrico**, dado por:
$$\phi_{E}=\int_{superficie}\vec{E}.d\vec{A}$$
Además, $[\phi]=N \frac{m^{2}}{C}$
#### Def
**Superficie Gaussiana**: *Superficie cerrada, suave, orientable y sin orificios.*
###### Obs
Esta clase de superficies dividen el espacio en dos; el interior y el exterior. El **flujo del campo eléctrico** será proporcional a la diferencia entre la cantidad de líneas de campo salientes y entrantes a la superficie Gaussiana.
![[Pasted image 20230809181849.png|250]]
→ Por la **ley de Gauss**:
$$\phi_{E}=\oint_{S}\vec{E}.d\vec{A}=\frac{Q_{int}}{\epsilon_{0}}$$
y si hubiera más de una carga encerrada:
$$\phi_{E}=\oint_{S}\vec{E}.d\vec{A}=\frac{\sum\limits_{i=1}^{N}q_{i}^{int}}{\epsilon_{0}}$$
###### Obs
Si la carga neta es positiva (*negativa*) → el flujo neto a través de la superficie Gaussiana también es positiva (*negativa*)
###### Obs
Para tener flujo de campo eléctrico no nulo es necesaria una fuente o sumidero de campo en el interior, esto es, carga neta no nula.
##### Prop
Es posible valerse de la simetría de una distribución de carga para, a través de la ley de Gauss, determinar el módulo del campo eléctrico. Si se tiene una distribución de carga con cierta simetría, el procedimiento consistirá en:
- Elegir una superficie Gaussiana con la simetría de la distribución que la encierre al menos parcialmente.
- Si cumple con lo anterior, será posible establecer fácilmente la dirección y sentido del campo sobre la superficie Gaussiana y, además, su módulo será cte.
- Valiéndonos de la ley de Gauss podremos determinar el módulo del campo eléctrico.
### Conductores en equilibrio electroestático
Las cargas en exceso dentro de un conductor se depositan en su superficie
![[Pasted image 20230809194600.png]]
Luego, el campo eléctrico en su interior es $E=0$
###### Obs
La superficie de cualquier conductor con carga en equilibrio electroestático es una superficie **equipotencial**: Cada punto de la superficie de un conductor cargado en equilibrio está en el mismo potencial eléctrico. Además, ya que el campo eléctrico es igual a *cero* en el interior del conductor, el potencial eléctrico es **cte** en cualquier punto en el interior del conductor y en la superficie es equivalente a su valor. Por lo que, al ser *cte* el potencial eléctrico dentro de la superficie, **No** requiere ningún trabajo mover una carga desde el interior hasta la superficie del conductor cargado. 
###### Obs
En el caso de someter al conductor a un campo eléctrico externo, las cargas se redistribuirán en su superficie para anular el campo en su interior.
###### Obs, ¿Cómo serán las líneas de campo eléctrico en la superficie del conductor?
Éstas serán normales a la superficie.
###### Obs
![[Demostración puntas cargadas]]
## Potencial Eléctrico y diferencia de potencial
Para un desplazamiento infinitesimal $d\vec{s}$ de una carga puntual *q* inmersa en un campo eléctrico, el trabajo realizado por un campo eléctrico sobre la misma es $W_{int}=\vec{F}_{e} \centerdot d\vec{s} = q\vec{E} \centerdot d\vec{s}$. Además, el trabajo interno hecho en un sistema es igual al negativo de la variación de la energía potencial del sistema: $W_{int}=-\Delta U_{g}=-\Delta U_{e}$. Por tanto, como la carga *q* se desplaza , la energía potencial del sistema carga-campo cambia en una cantidad $dU_{e}=-W_{int}=-q.\vec{E}\centerdot d\vec{s}$
Para un desplazamiento finito de la carga desde un punto *A* a un punto *B*, la variación de la energía potencial del sistema es:
$$\Delta U_{E}=-q\int_{A}^{B}\vec{E}\centerdot d\vec{s}$$

La *diferencia de potencial* $\Delta V=V_{B}-V_{A}$ entre los puntos *A* y *B* de un campo eléctrico se define como  el cambio en energía ppotencial en el sistema al mover una carga *q* entre los puntos, dividido entre la carga:
$$\Delta V \equiv \frac{\Delta U_{E}}{q} = -\int_{A}^{B}\vec{E}\centerdot d\vec{s}$$
##### Obs
Para poder calcular la diferencia de potencial, es necesario establecer un punto 0, un punto  inicial, ya que no se puede establecer y decir con certeza el potencial eléctrico en un punto del espacio, pero si podemos decir la variación del mismo. Por lo que si establecemos un punto de *"potencial = 0"*, podemos calcular el potencial en un punto ya que la diferencia con 0 es igual al valor en ese punto.
Y por lo general establecemos el **cero de potencial** en el infinito, tal que: $V_{\infty}=0$.
#### Prop
Consideremos la situación en la que un agente externo mueve la carga en el campo, desde un punto   *A*, hasta un punto *B*, sin modificar la energía cinética de ésta. El trabajo que realizará el agente externo será:
$$W=q\Delta V$$

> *El campo eléctrico es una medida de la relación del cambio del potencial eléctrico en función de la posición*

- $1eV = (1,60218 \centerdot 10^{-19}C)(1V)$ 
### Diferencias de potencial en un campo eléctrico uniforme
Si el campo es uniforme, las cuentas que vimos antes se simplifican un poco ya que ahora el campo es **cte** en todo punto en el que estamos tranbajando.
$$V_{B}-V_{A}=\Delta V=-\int_{A}^{B}\vec{E}\centerdot d\vec{s} = - E\int_{A}^{B}ds=-E.d$$

> Cuando una carga positiva se mueve del punto *A* al punto *B*, la energía potencial eléctrica del sistema carga-campo disminuye.

### Potencial eléctrico y energía potencial debido a cargas puntuales
Si tomo el **cero de potencial** en el infinito, el potencial eléctrico de una *carga* en un punto *P*, a una distancia *r*, será:
$$V=k_{e}\frac{q}{r}$$
Y para un sistema de cragas puntuales:
$$V=k_{e}\sum\limits_{i}\frac{q_{i}}{r_{i}}$$
Y la energía potencial la calcularemos mediante el trabajo que 'cuesta' mover todas las cargas puntuales con referencia a las demás del sistema.
$$U_{E}=k_{e}\sum\limits_{j}\sum\limits_{i\neq j}\frac{q_{j}q_{i}}{r_{i}}$$
#### Obtención del valor del campo eléctrico a partir del potencial eléctrico
A partir de la expreción de potencial eléctrico, el incremento de la diferencia de potencial $dV$ entre dos puntos separados por una distancia *ds* puede expresarse como:
$$dV=-\vec{E}\centerdot d\vec{s}$$
##### Obs
> En notación vectorial: $\vec{E}=-\nabla V= - (\hat{i}\frac{\partial}{\partial x}+\hat{j}\frac{\partial}{\partial y}+\hat{k}\frac{\partial}{\partial z})V$   
### Potencial eléctrico debido a distribuciones continuas de carga
Si conozco la distribución de carga, considero el potencial debido a un elemento de carga $dq$ pequeño y trato a este elemento como una carga puntual. Por lo que el incremento en la diferencia de potencial me queda como:
$$dV=k_{e}\frac{dq}{r} \to V=k_{e}\int \frac{dq}{r}$$
#### Energía electrostática almacenada
$$\mu_{E}=\frac{1}{2}\epsilon_{0}E^{2} \Longrightarrow U=\frac{1}{2}\epsilon_{0}\int_{V}E^{2} dV$$
