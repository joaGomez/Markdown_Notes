##### Def
Tomando $z=e^{st}$, la transformada $\mathcal{Z}$ es una herramienta para el análisis de señales y sistemas en tiempo discreto. La notación será $\mathcal{Z}[x(n)](z)~ o ~X(z)$ 
##### Def
La transformada $\mathcal{Z}$ unilateral será:
$$\mathcal{Z}[x(n)](z)=\sum\limits_{n\in\mathbb{N_{0}}}x(n)z^{-n}$$

Y la transformada $\mathcal{Z}$ bilateral se escribirá como:
$$\mathcal{Z}_{b}[x(n)](z)=\sum\limits_{n\in\mathbb{Z}}x(n)z^{-n}$$
### Convergencia de la transformada de $\mathcal{Z}$
Supongamos que $x(n), n \in \mathbb{N_{0}}$ es tal que existen ctes positivas $c$ y $R$ tales que: $|x(n)|<cR^{n} \quad \forall n\in\mathbb{N_{0}} \longrightarrow |\sum\limits_{n\in\mathbb{N_{0}}}x(n)z^{-n}|\leq \sum\limits_{n\in\mathbb{N_{0}}}|x(n)||z^{-n}|<\sum\limits_{n\in\mathbb{N_{0}}} c (\frac{R}{ |z| })^{n} < \infty$ Si $R < |z|$.
Cuando existan las ctes $c$ y $R$ → Podremos definir su **radio de convergencia absoluta** $R_{ax}$ como $R_{ax}= ínf \{ R: |x(n)|<cR^{n} \quad \forall n\in\mathbb{N_{0}}\}$
###### Obs
La convergencia en $|z| = R_{ax}$ no se puede determinar como generalidad, ya que dependerá de cada función.
### Propiedades de la transformada $\mathcal{Z}$
1) **Linealidad:** Sean $b_{1},b_{2}$ escalares, tales que $|b_{1}|+|b_{2}|\neq 0$ → 
$$\mathcal{Z}[b_{1}x(n)+b_{2}y(n)](f)=b_{1}X(z)+b_{2}Y(z)$$
Y la convergencia se dá para $|z| > R_{ax}$ y $|z| > R_{ay}$, por lo que el radio de convergencia absoluta será $R=máx \{ R_{ax},R_{ay} \}$
2) **Desplazamiento en tiempo:**
$$\begin{split}
& \mathcal{Z}[x(n-n_{0})](z)=z^{-n_{0}}X(z)+z^{-n_{0}}\sum\limits_{m=-n_{0}}^{-1} x(m)z^{-m} \\
& \mathcal{Z}[x(n+n_{0})](z)=z^{n_{0}}X(z)-z^{n_{0}}\sum\limits_{m=0}^{n_{0}-1} x(m)z^{-m}
\end{split}$$
Notar que el radio de convergencia absoluta de la señal desplazada es el mismo que el de la original.
3) **Escalonamiento en frecuencia:** Sea $b\neq 0$ →
$$\mathcal{Z}[b^{n}x(n)](z)=X(\frac{z}{b})$$
Por lo que la serie convergerá absolutamente si $|z| > R_{ax}|b|$.
4) **Diferenciación en frecuencia:** Se sabe que $X(z)$ es analítica para todo $z$ tal que $|z| \geq r > R_{ax}$ y que la serie converge absoluta y uniformemente en esa región → $\frac{dX}{dz}=-z^{-1}\sum\limits_{n\in\mathbb{N_{0}}}nx(n)z^{-n}$, por lo tanto:
$$\mathcal{Z}[n^{k}x(n)](z)=(-z \frac{dX}{dz})^{k}(z)$$
con radio de convergencia absoluta $R_{ax}$.
5) **Transformada $\mathcal{Z}$ de la convolución:** Sean $x(n), y(n)$ causales, entonces se cumple que:
$$\mathcal{Z}[x*y(n)](z)=X(z)Y(z)$$
### Comportamiento asintótico
##### Teorema del valor inicial
Sea $x(n)$ causal, con transformada $\mathcal{Z}[x(n)]$ y radio de convergencia absoluta $R_{ax}$ → $\lim_{z\to \infty}X(z)=x(0)$
##### Teorema del valor final
Sea $x(n)$ causal, con transformada $\mathcal{Z}[x(n)]$, tal que $\exists \lim_{n\to\infty} x(n)=A$ → $\lim_{z\to 1}(1-z^{-1})X(z)=A$, cuando este límite se toma para $z$ tendiendo a $1$ por la región $R=\{ z:|z| > 1, |arg(z-1)| \leq \theta_{0} < \frac{\pi}{2} \}$ para algún $\theta_{0}$ fijo.
###### Obs
Para el uso de este teorema, debe tenerse cuidado con la **existencia** del límite de $x(n)$ cuando $n\to \infty$.
###### Obs
![[Pasted image 20230918141101.png]]
##### Proposición 2
Supomgamos que $x(n)$ es tal que $X(z)$ tiene una cantidad finita de polos $z_{1},...,z_{M}$ en $\mathbb{C}$ → Se cumplen las siguientes propiedades:
1) $\exists \lim_{n\to\infty} x(n)=0 \leftrightarrow |z_{i}| < 1, 1 \leq i \leq M$.
2) $\exists \lim_{n\to\infty} x(n)=a \leftrightarrow X(z)=X_{1}(z)+ \frac{a}{z-1}$ y $X_{1}(z)$ tiene sus $M-1$ polos dentro del círculo unitario.
3) En todo otro caso: $\nexists \lim_{n\to\infty} x(n)$.
### Inversión de la transformada $\mathcal{Z}$
![[Pasted image 20230918141848.png]]
1) **Inversión por división larga:** Se aplica a la inversión de la transformada $\mathcal{Z}$ de señales $x(n)$ causales. $X(z)$ debe ser un cociente de polinomios en $Z$, es decir:
$$X(z)= \frac{P(z)}{Q(z)}$$
Como $x(n)$ es causal → $gr(P(z)) \leq gr(Q(z))$, y el método consiste en hacer la división larga, es decir, en potencias de $z^{-1}$ de $P(z)$ por $Q(z)$.
![[Ejemplo_Inversión por división larga]]
2) **Inversión por series de Laurent:** Dado que una señal en tiempo discreto causal $x(n)$, su transformada de $\mathcal{Z}$ tiene solo potencias no positivas de $z$ → Su representación en series de potencias es una *serie de Laurent*, por lo que los coeficientes que acompañan a las potencias de $z^{-1}$ serán los correspondientes valores de $x(n)$. Por lo tanto, mediante este desarrollo para $X(z)$, podremos obtener $x(n)$.
![[Ejemplo_Inversión por series de Laurent]]
3)  **Inversión por integrales de línea:** Sean $X(z)=\sum\limits_n\in\mathbb{N_{0}} x(n)z^{-n}$ y $\Gamma$ una curva cerrada simple que contiene al origen en su interior, y que a su vez está contenida en la región de convergencia de $X(z)$ y supongamos que $X(z)$ tiene una cantidad finita de singularidades en la región encerrada por $\Gamma$. Como en la región de convergencia de $X(z)$, la convergencia es uniforme, tendremos que para todo $k \in \mathbb{N_{0}}$, $\oint_{\Gamma}z^{k-1}X(z)dz = \begin{cases} & i2\pi \quad si \quad n=k \\ & 0 \qquad si \quad n\neq k \end{cases}$ , en consecuencia:$$x(k)= \frac{1}{2\pi i}\oint_{\Gamma}z^{k-1}X(z)dz=\sum\limits_{j=1}^{M}Res[z^{k-1}X(z), z_{j}]$$
Donde $z_{1},...,z_{M}$ son los puntos singulares de $z^{k-1}X(z)$ que están en la región encerrada por $\Gamma$.
4) **Inversión por descomposición en fracciones simples:** Este método es particularmente útil en el caso en que $X(z)$sea una fución racional en $z$. Consideramos $X_{1}(z)$ una función racional en $z$ que es la transformada $\mathcal{Z}$ de $x_{1}(n)$ señal en tiempo discreto causal → $X_{1}(z)=\frac{P_{1}(z)}{Q(z)}$ con $P_{1}(z)$ y $Q(z)$ polinomios y $gr(P_{1}(z))\leq gr(Q(z))$ → $\exists ~ A ~ cte$ y $P(z)$ un polinomio con $gr(P) < gr(Q)$ tales que:
$$X_{1}(z)=A+\frac{P(z)}{Q(z)}= A + X(z)$$
