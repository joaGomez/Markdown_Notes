Juntura metal-óxido-semiconductor.

En el óxido no hay cargas atrapadas. La corriente no puede circular por el óxido.

##### En equilibrio
Se asume condición de Flat-band: $\phi_{M}=\phi_{s}$. Por lo tanto las energías de Fermi del metal y del SC estarán alineadas.

![[Pasted image 20240516193743.png#center|250]]

Al conectar una fuente deja de estar en equilibrio. Si conecto en directa (para el SC de tipo p), la energía de Fermi del SC disminuirá.

![[Pasted image 20240516194019.png#center|400]]

Al aplicar una tensión negativa en el gate, el campo eléctrico empujará los huecos hacia el óxido. habrá una acumulación de huecos en el silicio cerca del óxido.

Si fuese de tipo n funcionaría de la siguiente forma:

![[Pasted image 20240516194358.png#center|400]]

Si aplicamos una tensión positiva (pequeña) en el gate, el campo eléctrico empujará los huecos hacia abajo, los cuales dejarán iones con carga negativa. En este caso, ocurre un vaciamiento de cargas móviles en el silicio cerca del óxido (zona desierta). 

![[Pasted image 20240516201406.png#center|400]]

Si aumento la tensión positiva en el gate (por encima de la tensión umbral $V_{TH}$), me aparecen electrones libres en una zona. Por lo que en esa zona, la energía de Fermi intrínseca será menor a la energía de Fermi. Ocurre una inversión del canal en el silicio cerca del óxido. Se puede considerar como que en esa región el silicio se volvió de tipo n. La zona desierta llegó a su máximo valor y no se modifica si se sigue aumentando $V_{G}$.

![[Pasted image 20240516203133.png#center|400]]

**Obs:** Se pueden generar pares electrón-hueco, por agitación térmica u otro medio. Hay recombinación, pero no es suficiente. Por lo que me quedan electrones libres que serán desplazados por el campo eléctrico, y habrá un canal tipo n en el que fluye corriente. Para un SC de tipo n, habrá un canal de tipo p. **Aparece el MOSFET!!!**

#### Potenciales en la estructura
![[Pasted image 20240516203337.png#center|400]]
#### Regiones de operación
Las regiones de operación dependerán de la relación entre $\phi_{s}$ y $\phi_{F}$.

![[Pasted image 20240516203548.png#center|300]]

![[Pasted image 20240516203621.png#center|400]]
Dependiendo de la relación entre $V_{G}$ y $V_{TH}$ se obtienen distintas regiones de operación:

![[Pasted image 20240516204630.png#center|300]]
#### Electroestática

![[Pasted image 20240516204730.png#center|500]]
#### Relación entre $V_{G}$ y el potencial de superficie
La tensión del gate se puede expresar como: $V_{G}=V_{SC}+V_{ox}$. En el semiconductor se puede consderar que la ca´da de tensión se da en la superficie, por lo tanto $V_{SC}=\phi_{s}$. La caída de tensión en el óxido se puede obtener a través de su campo eléctrico, dando como resultado: $V_{ox}= \frac{t_{ox}}{\varepsilon_{ox}}\sqrt{2\varepsilon_{s}qN_{D}\phi_{s}}=\gamma \sqrt{\phi_{s}}$. De esta expresión, podemos deducir la siguiente igualdad:
$$V_{G}=\phi_{s}+\gamma \sqrt{\phi_{s}}$$
Y si utilizamos la condición de inversión, obtenemos la tensión de Threshold (tensión que debe superar $V_{G}$ para entrar en inversión fuerte).
$$V_{TH}=V_{TH0}=2\phi_{F}+\gamma \sqrt{2\phi_{F}}$$
#### Capacidad
- En acumulación: Es como un capacitor de placas planas paralelas. ![[Pasted image 20240517090254.png#center|400]]
- En vaciamiento: Dos capacidades en serie. ![[Pasted image 20240517090348.png#center|400]]
- En inversión: Desestimo la capacidad que apareció antes en serie, ya que la zona desierta no aumenta más a pesar de cuanto aumente la tensión $V_{G}$. Por lo que volvemos a tener un capacitor de placas planas paralelas. ![[Pasted image 20240517090606.png#center|400]]
- En alta y baja frecuencia: Como el proceso de generación de pares electrón-hueco es lento, si varío muy rápido la tensión $V_{G}$ no voy a alcanzar a ver como cambia la capacidad, ya que no le di tiempo a crearse el canal. En cambio, a baja frecuencia, tengo en cuenta qur toma un tiempo en crearse el canal, por lo que aumento la tensión del gate lentamente y de esa forma puedo ver como progresivamente la capacidad va a ir aumentando. En cambio, a alta frecuencia no veré cambios en la capacidad hasta que se cree el canal. Una vez este está creado, sí, crece la capacidad muy rápidamente debido a que mi tensión del gate ya es muy grande. ![[Pasted image 20240517091031.png#center|400]]
