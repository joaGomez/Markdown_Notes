Las variables aleatorias son funciones que transforman el espacio muestral $S$ en valores reales, es decir: $X: S \to \mathbb{R}$. Por lo tanto, la probabilidad de cada valor de $X$ está asociada a la probabilidad del espacio muestral $S$.

Para cada variable aleatoria $X$, se puede buscar cuáles son los valores que tienen asociada una probabilidad positiva. Este conjunto de valores se denomina **recorrido** y se nota $R_{X}$.

Dada una variable aleatoria discreta $X$, se denomina la función de probabilidad puntual $p_{x}$ a la función que a cada valor real le aasigna su probabilidad:
$$p_{x}: \mathbb{R}\to[0,1] / p_{x}(k)=P(X=k)$$
**Obs:** Dada una variable aleatoria discreta $X$ y su recorrido $R_{x}$, se puede deducir que los eventos asociados a valores diferentes de $X$ son mutuamente excluyentes, ya que $X$ no puede tomar dos valores distintos simultáneamente.

**Def:** Las probabilidades de todos los valores del recorrido deben sumar 1: $\sum\limits_{k\in R_{x}}p_{x}(k)=1$.
Dada una variable aleatoria discreta $X$, su **valor esperado** se nota tal que: $E(X)=\mu_{x}=\sum\limits_{k\in R_{x}}k\cdot p_{x}(k)$
#### Propiedades
- Sea una cte $c$ → $E(c)=c$.
- Sea una cte $a$ y $X$ una variable aleatoria discreta → $E(a\cdot x)=a\cdot E(x)$.
- Sean $X,Y$ dos variables aleatorias discretas → $E(X+Y)=E(X)+E(Y)$.
- $E(X^{2})=\sum\limits_{k\in R_{x}}k{^{2}}p_{x}(k)$.

Se define la **varianza** como $V(X)=E(X^{2})-E^{2}(X)$.

Se define el **desvío** tal que $\sigma(X)=\sqrt{V(X)}$.

De la definición de tanto la varianza como el desvío, nacen otras propiedades:
- Sea $c$ una cte → $V(c)=\sigma(c)=0$.
- Sea $a$ una cte y $X$ una variable aleatoria discreta → $V(a\cdot X)= a{^{2}}\cdot V(X) \Rightarrow \sigma(a\cdot X)= |a|\cdot \sigma(X)$.
- Sea $c$ una cte y $X$ una variable aleatoria discreta → $V(X+c)=V(X)\Rightarrow \sigma(X+c)=\sigma(X)$
- **Obs:** Sean $X,Y$ dos variables aleatorias discretas, por lo general vale que $V(X+Y)\neq V(X)+V(Y)$.

Sea $X$ una variable aleatoria discreta, se define la **función de distribución acumulada** tal que:
$$F_{X}:\mathbb{R} → [0,1] / F_{X}(k)=P(X\leq k)$$
Algunas propiedades de la función de distribución acumulada son:
 - Es monótona creciente → $k_{1}<k_{2}\Rightarrow F_{X}(k_{1})<F_{X}(k_{2})$.
 - $\lim_{k\to - \infty} F_{X}(k) = 0$.
 - $\lim_{k\to + \infty} F_{X}(k) = 1$.
 - Es continua a derecha → $\lim_{a\to k^{+}} F_{X}(a) = F_{X}(k)$.
 - $P(a<X\leq b)= F_{X}(b) - F_{X}(a)$.

Sea una variable aleatoria $X$ ($K$ valores posibles $x_{k}$)
$$\begin{matrix}
E(X)= \sum\limits_{k=1}^{K} x_{k}\cdot P(X=k) \\
V(X)= \sum\limits_{k=1}^{K} (x_{k}-E(X))^{2}\cdot P(X=k) \\
\sigma(X)=\sqrt{V(X)} \\
\gamma(X)= \frac{\sum\limits_{k=1}^{K} (x_{k}-E(X))^{3}\cdot P(X=k)}{\sigma^{3}(X)} \\
k(X)= \frac{\sum\limits_{k=1}^{K} (x_{k}-E(X))^{4}\cdot P(X=k)}{\sigma^{4}(X)} -3 
\end{matrix}$$
#### Variables aleatorias discretas notables
1. $X\sim Bernoulli(p):$ Sea $X$ la variable aleatoria discreta correspondiente al éxito ($= 1$) o fracaso ($= 0$) en un experimento con probabilidad $p$ de éxito.
2. $X\sim Binomial(n,p):$ Sea $X$ la variable aleatoria discreta correspondiente al número de éxitos en una secuencia de $n$ experimentos independientes cuyos únicos resultados posibles son éxito o fracaso. Cada uno de los experimentos tiene una probabilidad $p$ de éxito. **Obs:** $X\sim Bernoulli(p) \leftrightarrow X\sim Binomial(1,p)$
3. $X\sim Hipergeométrica(N,M,n):$ Considere una población con $N$ elementos, $M$ de los cuales son de un tipo dado. Se toma una muestra de tamaño $n$ al azar y sin reposición y sea $X$ la variable aleatoria discreta correspondiente al número de elementos en la muestra que son del tipo especial. **Obs:** Si $N,N-M,M >> n$ → Es una binomial con $p= \frac{M}{N}$ → $X\sim Binomial(n,p)$
4. $X\sim Geométrica(p):$ Se repiten experimentos independientes y con igual probabilidad de éxito hasta que se obtenga un éxito.
5. $X\sim Binomial~negativa(r,p):$ Se repiten experimentos independientes y con igual probabilidad de éxito hasta que se obtengan $r$ éxitos.

|   Propiedades    | $Bernoulli(p)$ |      $Binomial(n,p)$       |                  $Hipergeométrica(N,M,n)$                  |  $Geométrica(p)$  |   $Binomial~negativa(r,p)$   |          $Poisson(\lambda)$          |
| :--------------: | :------------: | :------------------------: | :--------------------------------------------------------: | :---------------: | :--------------------------: | :----------------------------------: |
|     $R_{X}$      |   $\{0,1\}$    |      $\{0,1,...,n\}$       |           $\{máx\{0,(N-M)\},...,mín\{(n,M)\}\}$            |  $\{0,1,...,n\}$  |       $\{0,1,...,n\}$        |           $\{0,1,...,n\}$            |
|     $P(X=k)$     |      $p$       | $\binom{n}{k}p^{k}q^{n-k}$ |    $\frac{\binom{M}{k}\binom{N-M}{n-k}}{\binom{N}{n}}$     |     $q^{k}p$      | $\binom{k+r-1}{k}q^{k}p^{r}$ | $\frac{\lambda^{k}}{k!}e^{-\lambda}$ |
|    $\mu_{x}$     |      $p$       |         $n\cdot p$         |                    $n\cdot \frac{M}{N}$                    |   $\frac{q}{p}$   |        $r\frac{q}{p}$        |              $\lambda$               |
| $\sigma_{x}^{2}$ |   $p\cdot q$   |     $n\cdot p \cdot q$     | $n\cdot \frac{M}{N}\cdot\frac{N-M}{N}\cdot\frac{N-n}{N-1}$ | $\frac{q}{p^{2}}$ |      $r\frac{q}{p^{2}}$      |              $\lambda$               |

