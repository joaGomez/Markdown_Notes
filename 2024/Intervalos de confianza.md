Se define $\bar{X}$ como un estimador puntual, ya que devuelve un solo valor como aproximación del parámetro.

Se mide la bondad de un estimador puntual mediante el error cuadrático medio:
$$ECM(\hat{\theta})= E[(\hat{\theta}-\theta)^{2}]=(E[\hat{\theta}]-\theta){^{2}}+E[(\hat{\theta}-E[\hat{\theta}])^{2}]$$
El estimador es insesgado si $E[\hat{\theta}]= \theta$. Un estimador es ideal si es insesgado de mínima varianza.

**Obs:** Si tomo un $n$ grande → Se dice que $\hat{\theta}$ es asintóticamente insesgado si:
$$\lim_{n\to \infty}E[\hat{\theta}(X_{1},..,X_{n})]-\theta=0$$
	Sean $X_{1},...,X_{n}$ variables aleatorias tales que su función de densidad de probabilidad/función de probabilidad acumulada se puede escribir con $\theta$ como parámetro a estimar → Ésta función se la denomina verosimilitud. Y el estimador de máxima verosimilitud es el valor de $\theta$ que maximiza la probabilidad.

**Obs:** Los estimadores de máxima verosimilitud son asintóticamente consistentes.
##### Estimación puntual de la media
Sean $X_{1},...,X_{n}$ variables aleatorias i.i.d con media $\mu=E[X_{1}]$. Un estimador de la media es el promedio:
$$\hat{\mu}=\hat{\mu}(X_{1},...,X_{n})= \frac{1}{n}\sum\limits_{k=1}^{n}X_{k}$$
**Observaciones:**
1. Es un estimador insesgado.
2. Por la ley de los grandes números → Es un estimador consistente.
3. Si $\sigma^{2}=Var[X_{1}] \to ECM(\hat{\mu})=Var[\bar{X}]= \frac{\sigma^{2}}{n}$.
4. Si $X_{1}\sim \mathcal{N}(\mu,\sigma) \Rightarrow \hat{\mu}\sim\mathcal{N}(\mu,\frac{\sigma}{\sqrt{n}})$.
5. Si $\sigma^{2}=Var[X_{1}]<\infty$, por TCL, $\hat{\mu}$ es asintóticamente normal. Es decir que, para $n$ grande, la distribución del estimador $\hat{\mu}$ se puede aproximar por la de una variable aleatoria $\sim\mathcal{N}(\mu, \frac{\sigma}{\sqrt{n}})$.
##### Estimación puntual de la varianza
Sean $X_{1},...,X_{n}$ variables aleatorias i.i.d con media $\mu=E[X_{1}]$y varianza $\sigma^{2}=Var[X_{1}]$. Un estimador de la varianza es la varianza muestral:
$$\hat{\sigma}{^{2}}=\hat{\sigma}{^{2}}(X_{1},...,X_{n})= S^{2}= \frac{1}{n-1}\sum\limits_{k=1}^{n}(X_{k}-\bar{X})^{2}= \frac{1}{n-1}\sum\limits_{k=1}^{n}X_{k}^{2}- \frac{n}{n-1}\bar{X}^{2}$$
**Observaciones:**
1. Es un estimador insesgado.
2. La varianza del estimador es: $ECM(\hat{\sigma}^{2})=Var[S^{2}]= \frac{\sigma^{4}}{n}(k+2+ \frac{2}{n-1})$, con $k=\frac{E[(X_{1}-E[X_{1}])^{4}]}{\sigma^{4}}-3$. Si $X_{1}$ es normal → $Var[S^{2}]= \frac{2\sigma^{4}}{n-1}$.
3. Si $X_{1}\sim \mathcal{N}(\mu,\sigma) \Rightarrow \frac{(n-1)S^{2}}{\sigma^{2}}\sim X_{n-1}^{2}$.
4. Si $k<\infty$, Chebychev nos permite probar una versión débil de los grandes números y que se trata de un estimador consistente.
5. Si $k<\infty$, por una versión del TCL, $S^{2}$ es asintóticamente normal. Por lo que, para un $n$ grande, la distribución de estimador de $S^{2}$ se puede aproximar por la de una variable aleatoria $\sim \mathcal{N}(\sigma^{2},\sqrt{Var[S^{2}]})$.
##### Estimación puntual de una proporción
Sean $X_{1},...,X_{n}$ variables aleatorias i.i.d con $X_{1}\sim$ Bernoulli($p$). cada $X_{i}$ marca la ocurrencia o no de un dado evento en una serie de experimentos independientes.
$$\hat{p}=\hat{p}(X_{1},...,X_{n})=F= \frac{1}{n}\sum\limits_{k=1}^{n}X_{k}$$
**Observaciones:**
1. Es un estimador insesgado.
2. Por la ley de los grandes números → Es un estimador consistente.
3. El error cuadrático medio es: $ECM(\hat{p})=Var[\hat{p}]= \frac{p(1-p)}{n}$.
4. $n\hat{p}\sim\text{Binomial}(n,p)$.
5. Por TCL, $\hat{p}$ es asintóticamente normal. Para $n$ grande, la distribución del estimador $\hat{p}$ se puede aproximar por la de una variable aleatoria $\sim \mathcal{N}(p, \sqrt{\frac{p(1-p)}{n}})$.
#### Estimación de intervalos
En ciertos casos, en vez de dar una estimación puntual de un parámetro $\theta$, se realiza la estimación de un intervalo de confianza $(\hat{\theta}_{l}^{\alpha}, \hat{\theta}_{u}^{\alpha})$ tal que:
$$P(\hat{\theta}_{l}^{\alpha}(X_{1},...,X_{n})<\theta < \hat{\theta}_{u}^{\alpha}(X_{1},...,X_{n}))= 1-\alpha$$
Donde $1-\alpha$ es el nivel de confianza del estimador.

**Obs:** Si se fija $\hat{\theta}_{l}^{\alpha}=-\infty$ → Intervalo unilateral a derecha. Si se fija $\hat{\theta}_{u}^{\alpha}=+\infty$ → Intervalo unilateral a izquierda. Si ambos $|\hat{\theta}_{l}^{\alpha}|, |\hat{\theta}_{u}^{\alpha}|<\infty$ → Intervalo bilateral.
##### Intervalo para la media con varianza conocida
Sean $X_{1},...,X_{n}$ variables aleatorias i.i.d con media $\mu=E[X_{1}]$ **desconocida** y varianza $\sigma^{2}=Var[X_{1}]$ **conocida**. Los intervalos con un nivel de confianza $\gamma\cdot 100\%$:
1. Unilateral a derecha: $$I_{r}^{\gamma}=\left(-\infty, \bar{X}+z_{\gamma}\cdot \frac{\sigma}{\sqrt{n}}\right)$$Donde $z_{p}=\Phi^{-1}(p)$.
2. Unilateral a izquierda: $$I_{l}^{\gamma}=\left(\bar{X}-z_{\gamma}\cdot \frac{\sigma}{\sqrt{n}},+\infty\right)$$Donde $z_{\alpha}=-z_{1-\alpha}$.
3. Bilateral: $$I_{lr}^{\gamma}=\left(\bar{X}-z_{\frac{1+\gamma}{2}}\cdot \frac{\sigma}{\sqrt{n}},\bar{X}+z_{\frac{1+\gamma}{2}}\cdot \frac{\sigma}{\sqrt{n}}\right)$$
Si las variables aleatorias no son normales, pero $n$ es grande, el TCL nos permite utilizar estos mismos intervalos de confianza.

**Obs:** Sean o no normales las variables aleatorias, si la varianza($\sigma^{2}$) es desconocida, para n muy grande, se pueden utilizar estos mismos intervalos de confianza reemplazando $\sigma$ desconocido por el estimador $S$.
#### Intervalo para la proporción con muestras grandes
Sean $p$ una probabilidad y $\hat{p}$ un estimador resultante de $n$ exerimentos independientes. Si $n$ es grande, se tienen los siguientes intervalos con un nivel de confianza de $\gamma\cdot 100\%:$
1. Unilateral a derecha: $$I_{r}^{\gamma}=\left[0,\hat{p}+z_{\gamma}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right)$$
2. Unilateral a izquierda: $$I_{l}^{\gamma}=\left(\hat{p}-z_{\gamma}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}},1\right]$$
3. Bilateral: $$I_{lr}^{\gamma}=\left(\hat{p}-z_{\frac{1+\gamma}{2}}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}},\hat{p}+z_{\frac{1+\gamma}{2}}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right)$$
Estos intervalos de confianza son muy parecidos a los de la media con varianza conocida. Esto es debido a que $p$ es el valor medio de las variables aleatorias i.i.d con distribución Bernoulli, $\hat{p}$ es la media muestral y al hecho que podemos aplicar al TCL. Sin embargo, hay algunas diferencias:
- $p\in[0,1]$.
- Se desconoce la varianza real, y se la reemplaza por el estimador $\hat{p}(1-\hat{p})$. Se puede mosttrar que esta aproximación es buena para $n$ grande.
#### Intervalo para la media de variables aleatorias normales
Sean $X_{1},...,X_{n}$ variables aleatorias i.i.d normales con media $\mu=E[X_{1}]$ y varianza $\sigma{^{2}}=Var[X_{1}]$ desconocidas. Luego, se tienen los siguientes intervalos con un nivel de confianza de $\gamma\cdot 100\%:$
1. Unilaterala a derecha: $$I_{r}^{\gamma}= \left(-\infty, \bar{X}+t_{n-1,\gamma} \frac{S}{\sqrt{n}} \right)$$Donde $t_{k,p}$ es el $100p$ percentil de una variable aleatoria con distribución t-student con $k$ grados de libertad.
2. Unilateral a izquierda: $$I_{l}^{\gamma}= \left(\bar{X}-t_{n-1,\gamma} \frac{S}{\sqrt{n}},+\infty \right)$$Recordemos que $t_{n-1,\alpha}=-t_{n-1,1-\alpha}$.
3. Bilateral: $$I_{lr}^{\gamma}= \left(\bar{X}-t_{n-1,\frac{1+\gamma}{2}} \frac{S}{\sqrt{n}}, \bar{X}+t_{n-1,\frac{1+\gamma}{2}} \frac{S}{\sqrt{n}} \right)$$
Dado que para $k$ muy grande la distribución $t$ de student es muy parecida a la normal, para $n>200$ no hace mucha diferencia si se utilizan los percentiles de distribución Gaussiana.

