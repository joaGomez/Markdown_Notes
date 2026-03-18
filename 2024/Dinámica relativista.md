La teoría de la relatividad surgió de la necesidad, detrás de muchas contradicciones de la vieja teoría. La fuerza de la nueva teoría está en la consistencia y sencillez con la que resuelve todas esas dificultades.

### Principio Galileano de la relatividad
Un marco inercial de referencia es aquel en el que se observa que un objeto no tiene aceleración cuando **NO** actúan fuerzas sobre él. Además cualquier sistema que se mueva con velocidad cte respecto a un marco inercial, también debe estar en un marco inercial.

> No hay marco inercial absoluto de referencia → Los resultados de un experimento realizado en un vehículo que se mueve con velocidad uniforme serán idénticos a los resultados del mismo experimento realizado en un vehículo inmóvil. **Las leyes de la mecánica deben ser las mismas en todos los marcos inerciales de referencia**.

Las ecuaciones de transformación galileana de la velocidad son consistentes con la noción antigua de tiempo y espacio, pero que conduce a serias contradicciones cuando es aplicada a ondas electromagnéticas.

Para resolver esta contradicción, debe concluir que:
- Las leyes de la electricidad y el magnetismo no son las mismas en todos los marcos inerciales.
- La ecuación de transformación galileana de la velocidad es incorrecta.

> Si suponemos lo primero, debe existir un marco de referencia preferencial en el que la rapidez de la luz tenga el valor $c$ y la rapidez medida sea mayor o menor que este valor en cualquier marco de referencia → **ERROR**
> Si suponemos lo segundo, estamos forzando a abandonar las nociones de tiempo absoluto y longitud absoluta que forman la base de las ecuaciones de transformación galileanas del espacio-tiempo → **CORRECTO**

### Experimento de Michelson-Morley
Los resultados del experimento de M-M no sólo contradijeron la hipótesis del éter, sino que también demostraron que era imposible medir la velocidad absoluta de la tierra respecto al marco éter.

Mediante este experimento, se entendió que la luz es una onda electromagnética que no requiere de ningún medio para propagarse.

### Prinicipio de la relatividad de Einstein
Einstein basó su teoría especial de la relatividad en dos postulados:
- El principio de la relatividad: Las leyes físicas deben ser las mismas en todosd los marcos inerciales de referencia.
- La invariabilidad de la rapidez de la luz: La rapidez de la luz en el vacío tiene el mismo valor, $c=3.00 * 10^{8} \frac{m}{s}$, en todos los marcos inerciales, cualquiera que sea la velocidad del observador o la velocidad de la fuente que emita la luz.

> Desde el punto de vista experimental, el principio de la relatividad de Einstein significa que cualquier clase de experimento realizado en un laboratorio en reposo debe dar el mismo resultado cuando se realice en un laboratorio que se mueve con una velocidad cte respecto al primero. **No existe marco inercial de referencia que sea preferenciado y es imposible detectar movimiento absoluto**.

### Consecuencias de la teoría especial de la relatividad
##### Simultaneidad y relatividad del tiempo
Dos eventos que son simultáneos en un marco de referencia en general no son simultáneos en un segundo marco que se mueve respecto al primero.

##### Dilatación del tiempo
$$\Delta t= \frac{\Delta t_{p}}{\sqrt{1-\frac{v^{2}}{c^{2}}}}=\gamma \Delta t_{p}$$
Notar que $\gamma > 1$. El intervalo $\Delta t$ medido por un observador que se mueve respecto a un reloj es más largo que el intervalo $\Delta t_{p}$ medido por un observador en reposo al mismo reloj. El intervalo $\Delta t_{p}$ se denomina **intervalo de tiempo característico**, y es el intervalo entre dos eventos medidos por un observador que ve que los evento se presentan en el mismo punto en el espacio.

##### Contracción de longitud
La distancia medida entre dos puntos en el espacio también depende del marco de referencia del observador. La **longitud característica** $L_{p}$ de un objeto es la longitud medida por alguien en reposo respecto del objeto. `La longitud de un objeto medida por alguien en un marco de referencia que se mueve respecto al objeto siempre es menor que la longitud característica`, y la definimos de la siguiente manera:
$$L= \frac{L_{p}}{\gamma}=L_{p}\sqrt{1 - \frac{v^{2}}{c^{2}}}$$
**Obs:** La contracción de longitud tiene lugar sólo a lo largo de la dirección de movimiento.

##### Efecto Doppler relativista
Otra consecuencia es el desplazamiento en la frecuencia observada por la luz que emiten átomos en movimiento. Si una fuente de luz y un observador se aproximan entre sí con rapidez relativa $v$, la frecuencia $f_{obs}$ medida por el observador es:
$$f_{obs}=\frac{\sqrt{1+ \frac{v}{c}}}{\sqrt{1 - \frac{v}{c}}}. f_fuente$$
Donde $f_{fuente}$ es la frecuencia de la fuente medida en su marco en reposo. Cuando la fuente y el observador se aproximan entre ellos → $f_{obs} > f_{fuente}$. Tomando valores negativos para $v$, obtengo la expresión cuando la fuente y el observador se alejan entre sí.

#### Ecuaciones de transformación de Lorentz
Supongo dos eventos que se presentan en los puntos $P$ y $Q$, y son reportados por dos observadores, uno en reposo en un marco $S$, y otro en un marco $S'$ que se mueve a la derecha con una rapidez $v$. El observador en $S$ reporta el evento con coord. $(x, y, z, t)$, mientras que el observador en $S'$ reporta el mismo evento con coord. $(x',y',z',t')$.
Para el intervalo de velocidades $0 < v < c$, las ecuaciones de transformación de Lorentz son válidas y son descriptas de la forma:
$$x'=\gamma (x-v\ t) \quad y'=y \quad z'=z \quad t'=\gamma(t - \frac{v}{c^{2}}x)$$
Si deseo transformar coord. del marco $S'$ a coord. del marco $S$, simplemente sustituyo $v$ con $-v$ :
$$x=\gamma (x'+v\ t) \quad y'=y \quad z'=z \quad t=\gamma(t' + \frac{v}{c^{2}}x)$$
Es posible expresar las diferencias entre las cuatro variables tal que:
$$S\to S'\begin{cases}
\Delta x'= x_{2}'-x_{1}'=\gamma (\Delta x-v\ \Delta t) \\
\Delta t'= t_{2}'-t_{1}'=\gamma (\Delta t - \frac{v}{c^{2}}\ \Delta x) \\
\end{cases}$$
$$S'\to S\begin{cases}
\Delta x= x_{2}-x_{1}=\gamma (\Delta x'+v\ \Delta t') \\
\Delta t= t_{2}-t_{1}=\gamma (\Delta t' + \frac{v}{c^{2}}\ \Delta x') \\
\end{cases}$$

### Ecuaciones de transformación de velocidad de Lorentz
Sea $S'$ el marco que se mueve con una rapdez $v$ respecto a $S$. Supongo un objeto que tiene una componente de velocidad $u_{x}'$ preciso en el marco $S'$, donde $u_{x}'= \frac{dx'}{du'}$, por lo que expresado en función de la velocidad vista desde un observador en $S$ será:
$$u_{x}'=\frac{u_{x}-v}{1-\frac{u_{x}.v}{c^{2}}}$$
Si el objeto tiene componentes de velocidad a lo largo de los ejes $y$ y $z$, las componentes medidas por un observador en $S'$ son:
$$u_{y}'=\frac{u_{y}}{\gamma (1-\frac{u_{x}v}{c^{2}})} \qquad u_{z}'=\frac{u_{z}}{\gamma (1-\frac{u_{x}v}{c^{2}})}$$
**Obs:** $u_{y}'$ y $u_{z}'$ no contienen el parámetro $v$ en el numerador porque la velocidad relativa es a lo largo del eje $x$. En otro extremo, cuando $u_{x}=c \to u_{x}'=c$. Lo cual es consstente con el segundo postulado de Einstein.

Para obtener $u_{x}$ en términos de $u_{x}'$, sólo debo sustituir $v$ con $-v$.
$$u_{x}=\frac{u_{x}'+v}{1+\frac{u_{x}'.v}{c^{2}}}$$

### Movimiento lineal relativista
Para cualquier partícula, la ecuación relativista correcta para una cantidad de movimiento lineal que satisface estas condiciones es:
$$\vec{p}=\frac{m\vec{u}}{\sqrt{1- \frac{u^{2}}{c^{2}}}}=\gamma m\vec{u}$$
Donde $\vec{u}$ es la velocidad de la partícula y $m$ es su masa.

La fuerza relativista $\vec{F}$ que actúa sobre una partícula cuya cantidad de movimiento lineal es $\vec{p}$ se define como:
$$\vec{F} \equiv \frac{d\vec{p}}{dt}$$
> **Obs:** Bajo condiciones relativistas, la aceleración $\vec{a}$ de una partícula disminuye bajo la acción de una fuerza cte., en cuyo caso $a \varpropto (1-\frac{u^{2}}{c^{2}})^{\frac{3}{2}}$. Por lo que cuando la rapidez de la partícula se aproxima a $c$ → La aceleración causada por cualquier fuerza finita se aproxima a cero. En consecuencia, es **imposible** acelerar una partícula desde el reposo hasta una rapidez $u \geq c$.

### Energía relativista
Suponemos que la partícula se acelera desde el reposo hasta alguna rapidez $u$. El trabajo invertido por la fuerza $F$ sobre la partícula es:
$$W=\int_{x_{1}}^{x_{2}}F\ dx = \frac{mc^{2}}{\sqrt{1- \frac{u^{2}}{c^{2}}}}-mc{^{2}}$$
Se define la energía cinético como:
$$K = \frac{mc^{2}}{\sqrt{1-\frac{u^{2}}{c^{2}}}}-mc{^{2}}=(\gamma -1)mc^{2}$$
El término cte $mc^{2}$ se denomina **energía en reposo** $E_{R}$ de la partícula:
$$E_{R}=mc^{2}$$
La suma de las energías cinética y en reposo se llama **energía total** $E$ :
$$E=K+mc^{2}=\gamma mc^{2}$$
**Obs:** $E{^{2}}=p{^{2}}c{^{2}}+(mc^{2})^{2}$

Cuando una partícula está en reposo $p=0 \to E=E_{R}=mc{^{2}}$.

#### Fotón
El fotón en particular es una partícula con masa cero ($m=0$) $\to E=pc$.

> La masa $m$ de una partícula es independiente de su movimiento, $m$ debe tener el mismo valor en todos los marcos de referencia y se denomina **masa invariante**. La energía total y la cantidad de movimiento lineal si dependen del marco de referencia en el que se miden.

#### Unidad de energía
La unidad de energía relativista es el electrón volts, y su relación con los joules es:
$$1\ eV = 1.6 \ * \ 10^{-19}J$$
$$1\ MeV=10{^{6}}\ eV \qquad 1\ GeV=10{^{9}}\ eV$$
### Masa y energía
Como $E=\gamma mc^{2}$, esto sugiere que incluso cuando una partícula está en reposo ($\gamma = 1$), todavía tiene una enorme cantidad de energía a través de su masa. Debido a esto, en situaciones relativistas, no es posible usar el principio de conservación de energía.

**Expresiones útiles:**
$$\begin{split}

 P=\frac{\partial K}{\partial t} & =\frac{\partial (E-mc^{2})}{\partial t}=\frac{\partial E}{\partial t}=\vec{F}.\vec{u} \\
& \vec{F}=\frac{\vec{F}.\vec{u}}{c^{2}}\vec{u}+\gamma \ m \ \vec{a}
\end{split}$$
### Transformación de la cantidad de movimiento
$$p_{x}=\frac{p_{x'}'+ \frac{v.E'}{c^{2}}}{\sqrt{1- \frac{v^{2}}{c^{2}}}} \qquad p_{y}=p_{y'}' \qquad p_{z}=p_{z'}' \qquad p_{x'}'=\frac{p_{x}-\frac{v.E}{c^{2}}}{\sqrt{1 - \frac{v^{2}}{c^{2}}}}$$
### Transformación de la energía
$$E=\frac{E'+ v.p_{x'}'}{\sqrt{1- \frac{v^{2}}{c^{2}}}}$$
$$E'= \frac{E-v.p_{x}}{\sqrt{1 - \frac{v^{2}}{c^{2}}}}$$

**Obs:** Para una partícula masiva en general:
$$p= \frac{1}{c} \sqrt{K^{2}+2mc^{2}K}$$

La **energía cinética umbral** es la energía mínima necesaria para que se produzca la reacción. En dicho caso, los productos de la reacción quedan en reposo en el sistema centro de masa/momentos. Pero desde el laboratorio veríamos las partículas emerger con la misma velocidad → Todos tendrán las misma energía cinética.