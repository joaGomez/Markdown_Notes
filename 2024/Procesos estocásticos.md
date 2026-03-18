Un proceso estocástico es una familia de variables aleatorias $\{ X(t) \}_{t\in \mathbb{T}}$, donde $\mathbb{T}$ es el conjunto de índices o espacio de parámetros del proceso.

- Proceso discreto: $p(x_{1},t_{1},...,x_{n},t_{n})=P(X(t_{1})=x_{1},...,X(t_{n})=x_{n})$
- Proceso continuo: $f(x_{1},t_{1},...,x_{n}, t_{n})$. En general no es sencilla esta forma de describir los procesos, por lo que se utilizan simplifaciones, como los procesos estacionarios, procesos de Markov, etc.

> Observación: **Ec. de Chapman-Kolmogorov**
> ![[Pasted image 20240521201026.png|400]]

**Def:** Un proceso estocástico es **estacionario** si:
- Continuo: $$f(x_{1},t_{1}+\Delta t,...,x_{n}, t_{n}+\Delta t)=f(x_{1},t_{1},...,x_{n}, t_{n})$$
- Discreto: $$p(x_{1},t_{1}+\Delta t,...,x_{n},t_{n}+\Delta t)=p(x_{1},t_{1},...,x_{n},t_{n})$$
En resumen, $\{X(t)\}_t$ es estacionario si **es igual** a $\{X(t+\Delta t)\}_t$.

**Obs:** Se dice que un proceso estocástico es estacionario en sentido amplio si su *esperanza* y *varianza* son constantes.
##### Incrementos independientes
Un proceso estocástico tiene incrementos independientes si para $t_{1},t_{2},t_{3},t_{4}\in\mathbb{T}$ se cumple que:
$$[t_{1},t_{2})\cap[t_{3},t_{4})=\emptyset \Rightarrow (X(t_{2})-X(t_{1}))~\text{y}~(X(t_{4})-X(t_{3}))~\text{son v.a independientes}$$
Se dice que un proceso estocástico tiene incrementos estacionarios si las variables aleatorias
$(X(t_{2})-X(t_{1}))~\text{y}~(X(t_{2}+\Delta t)-X(t_{1}+\Delta t))$ tienen la misma distribución de probabilidades.
##### Procesos de Markov
Se dice que un proceso estocástico es un proceso de Markov si para todo conjunto de valores $t_{1}\leq t_{2} \leq ...\leq t_{n},~t_{i}\in\mathbb{T}$, y para todo $x_{1}, x_{2},...,x_{n}\in\mathbb{E}$ se cumple:
- Continuo: $$f(x_{n},t_{n}|x_{n-1},t_{n-1},...,x_{1},t_{1})=f(x_{n},t_{n}|x_{n-1},t_{n-1})$$
- Discreto: $$p(x_{n},t_{n}|x_{n-1},t_{n-1},...,x_{1},t_{1})=p(x_{n},t_{n}|x_{n-1},t_{n-1})$$
**El proceso depende del estado más reciente y no de toda la historia.**

> Observación: **Ec. de Chapman-Kolmogorov**
> ![[Pasted image 20240521201729.png|400]]
##### Proceso de conteo
Considero un proceso estocástico $\{T(k)\}_{k\in \mathbb{N}_{0}}$ tal que $T_{0}=0$ y $k\leq m \Rightarrow T_{k}\leq T_{m}$. Este tipo de proceso puede utilizarse para modelar los instantes de ocurrencia de ciertos eventos. Puede tener un espacio de estadios discreto o continuo. En general, se le asocia un proceso de conteo $\{ N(t) \}_{t\geq 0}$ definido como $N(t)=\text{máx}\{ k:T_{k}\leq t \}$. Por lo tanto, $N(t)$ cuenta la cantidad de eventos hasta el instante $t$, y cuenta con las siguientes proposiciones/características:
1. $N(0)=0$.
2. $N(t)\in\mathbb{N}_{0}$.
3. $s\leq t \Rightarrow N(s)\leq N(t)$.
4. $N(t)-N(s)$ es la cantidad de eventos en el intervalo $(s,t]$.
##### Proceso de Poisson
Un proceso de conteo puede considerarse un proceso de Poisson con tasa $\lambda>0$ si satisface las siguientes condiciones:
1. Tiene incrementos independientes.
2. Los incrementos son estacionarios.
3. La probabilidad de que exactamente un evento ocurrra en un intervalo de longitud $\Delta t$ es $\lambda \Delta t+ o(\Delta t)$.
4. La probabilidad de que más de un evento ocurra en un intervalo de longitud $\Delta t$ es $o(\Delta t)$.

Si cumple estas condiciones: $N(t)\sim \text{Poisson}(\lambda t) \Rightarrow P(N(t)=k)=\frac{(\lambda t)^{k}}{k!}e^{-\lambda t}~\text{con}~k=0,1,...$

**Obs:** Sea ${T(k)}_{k\in \mathbb{N}_{0}}$ el proceso estocástico que modela los instantes de ocurrencia de eventos asociados al proceso de Poisson ${N(t)}_{t\in\mathbb{R}_{\geq 0}}$. También, se puede demostrar que, para todo $k\in\mathbb{N}_{0}$, $(T(k+1)-T(k))$ son variables aleatorias i.i.d con distribución exponencial, de parámetro $\lambda$. Es decir, los tiempos entre eventos son variables exponenciales independientes.
##### Cadenas de Markov
Las cadenas de Markov son procesos de Markov en los cuales el espacio de estados es discreto: $E = \{s_{1}, s_{2}, s_{3}, ... \}$. Nosotros nos concentraremos en cadenas cuyo espacio de parámetro o conjunto de índices es también discreto: $\mathbb{T} = \mathbb{N}_{0}$ . Una cadena de Markov $\{X(n)\}n\in\mathbb{N}_{0}$ queda completamente descripta por:
1. Distribución de probabilidades del estado inicial: $p_{j}(0)=P(X(0)=s_{j})$ con $\sum\limits_{j}p_{j}(0)=1$.
2. Probabilidades de transición entre cada par de estados en cada instante de tiempo: $p_{ij}(n)=P(X(n+1)=s_{j}|X(n)=s_{i})$ con $\sum\limits_{j}p_{ij}(n)=1~\forall ~i$.
	Por la ec. de Chapman-Kolmogorov: $p_{j}(n+1)=\sum\limits_{i}p_{ij}(n)p_{i}(n)$.
	> Observación: ![[Pasted image 20240521205053.png|500]]
###### Tipos de estados en cadenas homogéneas
Si $P(X(n + m) = s_{j} | X(n) = s_{i} )> 0$ para algún $m$, entonces se dice que el estado $s_{j}$ es accesible desde el estado $s_{i}$. Si todos los estados de una cadena de Markov son accesibles de todos los otros estados, se dice que la cadena de Markov es irreducible. Un estado $s_{i}$ es absorbente si $p_{ii} = 1$. Un estado $s_{j}$ es periódico con período $T_{0}$ si $P(X(n) = s_{j} | X(0) = s_{j}) = 0$ salvo para $n = k$.
###### Diagrama de estados de Markov
Se trata de un grafo dirigido y con aristas etiquetadas. Cada nodo del grafo se corresponde a un estado posible de la cadena de Markov. La etiqueta de cada arista dirigida indica la probabilidad de transición de un estado hacia otro.
![[Pasted image 20240521211324.png#center|500]]
**Teorema:** Una cadena de Markov finita irreducible tiene una distribución estacionaria de probabilidades → $\exists ~\vec{\pi}= \lim_{n\to \infty}\vec{p}(n)$, y ese límite es independiente de la distribución de probabilidades del estado original $\vec{p}(0)$.

**Teorema:** Si $\exists k$ / todos los elementos $\mathbb{P}_{ij}^{k}>0$, la cadena de Markov es regular → Existe una distribución de probablidades estacionaria.

> Observación:
> ![[Pasted image 20240521211714.png|600]]

