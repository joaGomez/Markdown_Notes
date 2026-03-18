Pasamos de trabajar con opamps a utilizar circuitos amplificadores. El objetivo de esto es modelizar nuestro circuito amplificador hecho con transistores y componentes pasivos como resistencias, capacitores, etc.

Dado que los parámetros del circuito amplificador son desconocidos, no podemos utilizar los recursos como tierra virtual. Sino, la técnica para desarrollar estos circuitos es modelizarlos con un diagrama de bloques realimentado. De esta forma, se busca compatibilizar los componentes presentes en el circuito con los bloques del sistema.

Hay 4 escenarios posibles para modelizar un diagrama de bloques, ya que la entrada y la salida pueden estar caraterizadas por tensión o corriente:

![[Pasted image 20250813105249.png#center|400]]

Se define el parámetro estabilizador como la relación entre la salida sobre la entrada.
$$
P_{E} = \frac{1}{\beta} \cdot \frac{A\cdot \beta}{1+A\cdot \beta}
$$
A partir de los parámetros de entrada/salida, se elige un modelo de cuadripolo para modelizar el bloque $\beta$. Este procedimiento se realiza para conseguir aislar la fuente controlada que aparece con el factor $\beta$, y tener un modelo que se asemeja más al del diagrma de bloques.
### Parámetros de entrada y salida
#### Entrada
Para determinar el parámetro de entrada, debo ver que parámetro (corriente/tensión) comparten entre el generador, el realimentador y el amplificador.
- Si se comparte corriente (Los 3 bloques están en serie) → Se suma tensión.
- Sise comparte tensión (Los 3 bloques se conectan con un nodo común) → Se suma corriente.
#### Salida
Para determinar el parámetro de salida, debo ver que parámtro comparten entre la carga, el realimentador y el amplificador.
- Comparten tensión → Muestrea tensión.
- Comparten corriente → Muestrea corriente.
### Modelo de cuadripolo
Para saleccionar que modelo utilizar, se puede realizar de varias maneras. Una es ver los parámetros de entrada y salida. El bloque $\beta$ conecta el parámetro que se muestrea a la salida, y lo suma en la entrada, por lo que podemos definir el bloque $\beta$ de la siguiente forma:
$$
\beta = \frac{\text{Magnitud que se suma}}{\text{Magnitud que se muestra}}\bigg{|}_{\text{Magnitud común a la entrada nula}} \qquad \qquad \text{Método práctico}
$$
Otra forma de plantear el modelo de cuadripolo es estableciendo el sistema de ecuaciones. Para ello, utilizo las variables independientes, las magnitudes comunes a la entrada y a la salida. Por ejemplo, si en la entrada se comparte $i_{1}$, y a la salida $v_{2}:$
$$
\begin{cases}
v_{1} = C_{11}\cdot i_{1} + C_{12}\cdot v_{2} \\
i_{2} = C_{21}\cdot i_{1} + C_{22}\cdot v_{2}
\end{cases}
$$
Donde $i_{1}$ y $v_{2}$ son las variables independientes, y $v_{1}$ e $i_{2}$ las variables dependientes.

**Observaciones:**
- Las ctes $C_{11}, C_{12}, C_{21} \text{ y } C_{22}$ son las ctes que cumplan el modelo de cuadripolo para el sistema de ecuaciones planteado.
- Siempre se cumplirá que $\beta=C_{12}$
- Siempre será despreciable $C_{21}$, ya que es el que aporta la fuente  controlada por la tensión a la entrada del realimentador, y en relación a $A\cdot v_{e}$ es despreciable.
### Parámetros del circuito
#### Bloque amplificador
Una vez resuelto el cuadripolo del bloque $\beta$, se determina el valor de las resistencias $R_{A}$ y $R_{B}$, las cuales aparecen también por el modelo del cuadripolo. La expresión para las resistencias salen del modelo del cuadripolo, y su valor se toma con el bloque realimentador en las condiciones del cuadripolo. Por ejemplo:

![[Pasted image 20250813122307.png#center|200]]
Los valores de las resistencias serán:
$$
R_{A} = \frac{v_{1}}{i_{1}}\bigg{|}_{v_{2}=0} = R_{f} \qquad R_{B} = \frac{v_{2}}{i_{2}}\bigg{|}_{v_{1}=0} = R_{f}
$$
Con estos valores, sustituyendo el realimentador por su cuadripolo, se puede calcular el factor $A:$
$$
A = \frac{v_{o}}{i_{e}}\bigg{|}_{\beta=0}
$$
#### Impedancia de entrada y salida

|       | Entrada                          | Salida                           |
| ----- | -------------------------------- | -------------------------------- |
| Malla | $Z_{i}= Z_{ia}(1+A\beta)$        | $Z_{o}= \frac{Z_{oa}}{1+A\beta}$ |
| Nodo  | $Z_{i}= \frac{Z_{ia}}{1+A\beta}$ | $Z_{o}= Z_{oa}(1+A\beta)$        |

Con esos resultados, para hallar la verdadera impedancia de entrada y salida del circuito:
![[Pasted image 20250813130228.png#center|600]]
**Observaciones:**
- Impedancia de salida:
	- Si es malla común, la impedancia de salida se ve en serie a la carga.
	- Si es nodo común, la impedancia de salida se ve en paralelo a la carga
- Impedancia de entrada:
	- Si es malla común, la impedancia de entrada se ve en serie al generador.
	- Si es nodo común, la impedancia de 
### Método de recorrida de lazo
Este es un método práctico para el cálculo del parámetro $|T|$ de un circuito realimentado.

El procedimiento para la aplicación del método será:
1) Pasivar el generador de entrada.
2) Cortar el lazo de realimentación.
3) Conectar en la entrada negativa (restador) una fuente de prueba $v_{p}$.
4) Al cortar el lazo, el nodo del bloque realimentador que queda al aire, se conecta en paralelo la impedancia que veria del amplificador (a lazo cerrado). 
5) En el nodo donde se conecto la impedancia, medimos la tensión ($v_{x}$).
6) El parámetro $T$ estará dado por la relación: $T = \left|\frac{v_{x}}{v_{p}}\right|$.
![[Ejemplo - Recorrida de Lazo]]
#### Ratio de retorno
En lugar de cortar el lazo entre la suma y el realimentador, se corta entre la suma y el amplificador. De esta manera, al hacer la relación entre la señal de retorno y la de entrada, tenemos el parámetro R:
$$
R = - \frac{S_{R}}{S_{P}}
$$
Donde $S_{P}$ es el generador de prueba que se conecta a la entrada del amplificador.

**Obs:** La resolución del método es semejante al de recorrida de lazo. Al cortar el lazo, se debe colocar la impedancia del amplificador vista por el sumador.

Este planteamiento conduce a la siguiente pregunta, ¿se puede realizar el corte en cualquier lugar del lazo?
Para poder cortar en cualquier otro lugar del lazo, se debe tener en cuenta no sólo la impedancia vista donde se corto el lazo, sino que se debe agregar la ganancia cuando $v_{p}$ se pasiva, y se usa $v_{i}$, de la siguiente manera:

![[Pasted image 20250911085118.png#center]]

De esta forma, la relación será:
$$
\frac{S_{o}}{S_{i}} = S_{i} G_{0} + \left( S_{i}RG_{\infty}-RG_{\infty} \frac{S_{o}}{G_{\infty}} \right) = G_{\infty} \frac{R}{1+R} + G_{0} \frac{1}{1+R}
$$
Donde $G_{0}= \frac{S_{o}}{S_{i}}\bigg{|}_{R=0}$ es la **ganancia ideal**, y $G_{\infty}= \frac{S_{o}}{S_{i}}\bigg{|}_{R\to \infty}$ es la **ganancia de lazo**.