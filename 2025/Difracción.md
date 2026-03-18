La difracción es el fenómeno por el que una onda electromagnética cambia de dirección al encontrarse con un obstáculo. Este fenómeno produce que la onda electromagnética tienda a curvarse alrededor de los bordes de un obstáculo y penetre en una región inaccesible para la óptica geométrica.

Los efectos de la difracción son generalmente perceptibles sólo cuando la longitud de onda es similar al tamaño del objeto en el que se difractan.
### Principio de Huygens
Según el Principio de Huygens, se puede describir la propagación de una onda en un medio cualquiera suponiendo que cada punto del frente de ondas se comporta como una fuente secundaria emisora de ondas esféricas (emisor secundario) y la interferencia de las mismos genera el siguiente frente de onda.

Todos los emisores secundarios emiten en fase, ya que todos los puntos de un frente de onda plano están en fase. Así, la interferencia entre los emisores secundarios anularía totalmente la propagación en todas las direcciones, excepto la perpendicular al frente de onda.
![[Pasted image 20251115183401.png]]
### Factor de oblicuidad
Augustin Fresnel (1818) agrega el “factor de oblicuidad” al modelo de Huygens, el emisor secundario emite según:
$$
K(\theta) = \frac{1}{2} (1+\cos \theta)
$$
#### Elipses de Fresnel
Las zonas de Fresnel describen cómo se distribuye la energía de una onda electromagnética en el espacio entre un transmisor y un receptor. No toda la energía viaja en línea recta: una parte se expande alrededor del eje del enlace y puede interferir constructivamente o destructivamente dependiendo de los obstáculos cercanos.

Cada zona corresponde a superficies elipsoidales que rodean la línea de vista directa (LOS). La primera zona de Fresnel es la más importante, porque contiene la mayor parte de la potencia útil del enlace.

Si cortamos las elipses de Fresnel con un plano perpendicular a la pantalla, obtenemos una serie de circunferencias concéntricas. Las zonas entre estas circunferencias se denominan Zonas de Fresnel.
![[Pasted image 20251115183620.png]]

Los haces dentro del primer círculo difieren en fase entre si, a lo sumo en 180°. Su composición produce una resultante de fase -90 ° con respecto del haz de referencia (Tx-Rx). 

Los haces dentro del segundo círculo también difieren en fase entre si a lo sumo en 180 °. Su composición produce una resultante de fase -270 ° respecto del haz de referencia o sea opuesta a la resultante de la primera zona.

Las regiones pares contienen aportes que se interfieren constructivamente entre sí, al igual que las impares. Las regiones pares contribuyen con ondas en contrafase con respecto de las regiones impares → interferencia destructiva.

**Obs:** Si obstruimos las zonas pares, llegará al receptor una onda más intensa que si dejamos el camino completamente despejado.

A partir de la definición de elipse de Fresnel:
$$
F_{n} = \sqrt{ \frac{n\lambda d_{1}d_{2}}{d_{1}+d_{2}} }
$$
![[Pasted image 20251115191613.png#center|300]]
### Filo de cuchillo
El “filo de cuchillo” es el modelo más simple para una obstrucción aguda, que en un plano que puede considerarse infinito.
$$
v = h\sqrt{ \frac{2}{\lambda} \frac{d_{1}+d_{2}}{d_{1}d_{2}} } = h\sqrt{ \frac{2}{\lambda} \left( \frac{1}{d_{1}} + \frac{1}{d_{2}} \right) }
$$
Donde $h$ es la altura desde la línea TR hasta la línea del obstáculo. Además, se puede demostrar que $v=\sqrt{ 2 } \frac{h}{F_{1}}$

**Convención del signo de $h$**
![[Pasted image 20251115192016.png#center|450]]
**Obs:** A menor frecuencia→ La onda puede ‘bordear’ conmayor facilidad el obstáculo. Visto de otra forma, a mayor frecuencia → El obstáculo afecta más.
![[Pasted image 20251115192405.png#center|350]]
#### Relación de despeje
$$
RD = \frac{h}{F_{1}}
$$
#### Difracción por un filo de cuchillo
El criterio a cumplir para los radioenlaces es → $-0.6 \leq \frac{h}{F_{1}} \leq 0.5$. Aunque, para mayor seguridad, se debe considerar que el 80% de $F_{1}$ debe estar despejado. 
A su vez, se considera difracción cuando → $0.5 \leq \frac{h}{F_{1}}<\infty$

**Obs:** Se considera visibilidad directa si no hay obstáculos dentro de la primera zona de Fresnel.