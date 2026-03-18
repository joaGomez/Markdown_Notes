Sean $\{X_{k} \}_{k=1}^{n}$ variables aleatorias independientes, llamamos a la sumatoria de éstas $S_{n}:$
$$S_{n}=\sum\limits_{k=1}^{n}X_{k}$$
$$E[S_{n}]=\sum\limits_{k=1}^{n}E[X_{k}] \qquad Var[S_{n}]=\sum\limits_{k=1}^{n}Var[X_{k}]$$
![[Pasted image 20240509175208.png|400]]

###### Desigualdad de Markov
$$P(|X|\geq \varepsilon) \leq \frac{E[|X|]}{\varepsilon} \qquad \varepsilon > 0$$
###### Desigualdad de Chebychev
$$P(|X-E[X]|\geq \varepsilon) \leq \frac{Var[X]}{\varepsilon^{2}} \qquad \varepsilon > 0$$
La desigualdad de Chebychev se puede usar para la suma $S_{n}$ variables aleatorias i.i.d $\{X_{k}\}_{k=1}^{n}$ para todo $\varepsilon>0:$
$$P\left(\left|\frac{S_{n}}{n}-E[X_{1}]\right|\geq \varepsilon\right)\leq \frac{Var[X_{1}]}{n\varepsilon^{2}}$$
Por la **ley débil de los grandes números**, se dice que para todo $\varepsilon>0:$
$$\lim_{n\to \infty}P(|\bar{X}_{n}-\mu|\geq \varepsilon)=0$$
La probabilidad de que el promedio y el valor medio difieran en algo se hace cada vez más pequeña a medida que se promedian más datos. Por lo que la **ley fuerte de los grandes números** afirma que:
$$P(\lim_{n\to \infty}\bar{X}_{n}=\mu)=1$$
Sea $A \subseteq \Omega$ un evento y sea $p=P(A)$. Supongamos que el experimento se repite varias veces en forma independiente, de modo que definimos la variable que define el evento como:
$$l_{k}=\begin{cases}1 \quad \text{Ocurrió A en el k-ésimo experimento}\\ 0 \quad \text{Caso contrario}\end{cases}$$
Las variables $l_{k}(A)$ con i.i.d con $E[l_{k}(A)]=p$, y $Var[l_{k}(A)]=p(1-p)$, definimos la frecuencia relativa de ocurrencia del evento $A$ en los primeros $n$ experimentos como:
$$\hat{P}_{n}= \frac{1}{n}\sum\limits_{k=1}^{n}l_{k}(A)$$
Sean $\{X_{k}\}_{k=1}^{n}$ i.i.d con $\mu=E[X_{1}]$ y $\sigma^{2}=Var[X_{1}]$, definimos $Z_{n}= \frac{\bar{X}_{n}-\mu}{\frac{\sigma}{\sqrt{n}}}$ $\to$ se define el **teorema central del límite** como:
$$\lim_{n\to \infty}F_{Z_{n}}(z)=\lim_{n\to \infty}P(Z_{n}\leq z)=\Phi(z)$$
**Obs:** A medida que $n$ se hace más grande, $Z_{n}$ se parece más a una variable $Z\sim N(0,1)$, por lo que para $n>20$ se cumplen las siguientes aproximaciones:
$$\begin{align*}
F_{Z_{n}}(z)&= P(Z_{n}\leq z)\simeq \Phi(z)\\
F_{\bar{X}_{n}}(x)&= P(\bar{X}_{n}\leq x)\simeq \Phi(\frac{x-\mu}{\frac{\sigma}{\sqrt{n}}})\\
F_{S_{n}}(s)&= P(S_{n}\leq s)\simeq \Phi(\frac{s-n\mu}{\sqrt{n}~\sigma})
\end{align*}$$
Sea $A \subseteq \Omega$ un evento y sea $p=P(A)$, de modo que definimos por la ley fuerte de los grandes números que $\lim_{n\to \infty} \hat{P}_{n}=p$ (con probabilidad 1). Por el teorema central del límite, para un $n$ muy grande:
$$F_{\hat{P}_{n}}(q)=P(\hat{P}_{n}\leq q)\simeq \phi\left(\frac{q-p}{\sqrt{\frac{p(1-p)}{n}}}\right)$$
##### Corrección por continuidad
El teorema central del límite es válido tanto para variables aleatorias continuas, como para variables aleatorias discretas. Para un $n$ muy grande (pero finito), estamos aproximando la distribución de una variable aleatoria discreta por la de una continua. Para que la aproximación sea correcta, hay que ajustar la distribución continua de la normal a la distribución discreta.
$$\begin{align*}
P(S_{n}=s)&= P\left(s- \frac{1}{2}<S_{n}\leq s+ \frac{1}{2}\right) \simeq \phi(\frac{s+ \frac{1}{2}-n\mu}{\sqrt{n}~\sigma}) - \phi(\frac{s- \frac{1}{2}-n\mu}{\sqrt{n}~\sigma})\\
P(\bar{X}_{n}=x)&= P\left(x- \frac{1}{2n}<\bar{X}_{n}\leq x+ \frac{1}{2n}\right) \simeq \phi(\frac{x+ \frac{1}{2n}-\mu}{\frac{\sigma}{\sqrt{n}}}) - \phi(\frac{x- \frac{1}{2n}-\mu}{\frac{\sigma}{\sqrt{n}}})\\
\end{align*}$$
