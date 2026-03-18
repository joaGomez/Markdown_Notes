**Def.** Un sistema es un modelo de la realidad cuya característica primordial es la de modificar señales. Describiremos los sistemas como mecanismos de **entrada-salida**, con una *entrada* o *señal que se modifica* $x(\cdot)$, y una *salida* o *señal que modificada* $y(\cdot)$, tal que el sistema se visualiza como:
$$x(\cdot) \to y(\cdot)$$
**Obs.** Simbolizaremos los sistemas como $\mathcal{S}$. Para **tiempo continuo** será $\mathcal{S}_{c}$, y para **tiempo discreto** será $\mathcal{S}_{d}$.

En **tiempo continuo**:
Para un sistema $\mathcal{S}_{c}$, resolveremos para $x(\cdot)$, $y(·)$ $\in D$, siendo $D$ el espacio de las funciones generalizadas.
$$x(t)\to y(t)$$
En **tiempo discreto**:
Para un sistema $\mathcal{S}_{d}$, el tratamiento lo haremos para $x(·)$, $y(·) ∈ P$, siendo $P$ el espacio de las sucesiones de números en $K$, es decir, $P = {x : \mathbb{Z},\to K}$, con $K = \mathbb{R}$ o $K = \mathbb{C}$.
$$x(n)\to y(n)$$
### Modelado de un sistema $\mathcal{S}$
**Def.**
Para tiempo continuo: Dada una función generalizada regular $x(\cdot)$ con dominio $\mathbb{R}$ y un intervalo $\mathcal{I} \subset \mathbb{R}$:
   $$x_{\mathcal{I}}(t)= \begin{cases} x(t) \quad si\quad t\in\mathcal{I} \\
 0 ~\qquad si\quad t\notin\mathcal{I}
\end{cases}  $$
Para tiempo discreto: Dado $x(\cdot)\in\mathcal{P}$ con dominio $\mathbb{Z}$, finito o infinito, ordenado en forma estrictamente creciente: 
   $$x_{\mathcal{I}}(n)= \begin{cases} x(n) \quad si\quad n\in\mathcal{I} \\
 0 ~\qquad si\quad n\notin\mathcal{I}
\end{cases}  $$
### Clasificación de los sistemas $\mathcal{S}$
**Def.**
- Un sistema $\mathcal{S}_{c}(\mathcal{S}_{d})$ es **instantáneo** o de **memoria nula** si cualquiera sea $t_{0}\in\mathbb{R}(n_{0}\in\mathbb{Z})$, la salida $y$, en el instante inicial, $t_{0}(n_{0})$, depende sólamente de la entrada $x$ aplicada en ese instante inicial.
- Un sistema $\mathcal{S}$ es **dinámico** si cualquiera sea $t_{0}\in\mathbb{R}(n_{0}\in\mathbb{Z})$, la salida $y$, en el instante inicial, $t_{0}(n_{0})$, depende no sólo de la entrada $x$ aplicada en ese instante inicial, sino también de la aplicada antes y/o después de ese instante.
- Se dice que el sistema $\mathcal{S}_{c}(\mathcal{S}_{d})$ es *causal* o *no anticipativo* si $y(\cdot)$ en $t^{*}\in\mathbb{R}(n^{*}\in\mathbb{Z})$, **no** depende de la entrada $x(\cdot)$ aplicada *después* de $t^{*}(n^{*})$, sino de la aplicada en ese instante y eventualmente antes. En otro caso, se dice que el sistema $\mathcal{S}_{c}(\mathcal{S}_{d})$ es *no causal* o *anticipativo*.
**Obs.** Sean dos sistemas $x_{1}(\cdot),~x_{2}(\cdot)\in\mathcal{D}$, si el sistema es **causal**, entonces se cumple que:
$$\begin{split}
& x_{1}(t)=x_{2}(t)~\forall t\leq t^{*} \Rightarrow y_{1}(t^{*})=y_{2}(t^{*}) \qquad t^{*}\in\mathbb{R} \\
& x_{1}(n)=x_{2}(n)~\forall n\leq n^{*} \Rightarrow y_{1}(n^{*})=y_{2}(n^{*}) ~~ n^{*}\in\mathbb{Z}
\end{split}$$
**Def.** Un sistema $\mathcal{S}_{c}(\mathcal{S}_{d})$ es de *tiempo invariante* o *fijo* o *estacionario*, si $\forall x\in \mathcal{D}(x\in \mathcal{P})$:
$$\begin{split}
& x(t)\to y(t)\Rightarrow x(t-\alpha)\to y(t-\alpha)\quad \forall t,\alpha\in\mathbb{R} \\
& x(n)\to y(n)\Rightarrow x(n-n_{0})\to y(n-n_{0})\quad \forall n,n_{0}\in\mathbb{Z}
\end{split}$$
**Obs.** Un sistema $\mathcal{S}$ es **tiempo invariante** si sus características no cambian con el tiempo.
### Sistemas relajados (Caracterización entrada-salida)
**Def.** Un sistema *está relajado* en $t_{0}(n_{0})$ $\longleftrightarrow$ La salida $y_{[0,\infty]}(\cdot)(y_{[n_{0},\infty]}(\cdot))$ está sóla y exclusivamente determinada por la entrada $x_{[0,\infty]}(\cdot)(x_{[n_{0},\infty]}(\cdot))$.
**Obs.** Si en particular $t_{0}=-\infty(n_{0}=-\infty)$ → El sistema está **relajado**.
**Def.** Si el sistema está relajado, la salida está excitada unívocamente por la entrada. Por lo que podemos caracterizar el operador $\mathcal{H}:\mathcal{D}\to\mathcal{D}(\mathcal{H}:\mathcal{P}\to\mathcal{P})$, de forma que:
$$y(\cdot)=\mathcal{H}[x](\cdot)$$
#### Propiedades
1) Sistema $\mathcal{S}$ *lineal*:
$$\mathcal{H}[\alpha_{1}x_{1}+\alpha_{2}x_{2}]=\alpha_{1}\mathcal{H}[x_{1}]+\alpha_{2}\mathcal{H}[x_{2}]$$
2) Sistema $\mathcal{S}$ *causal*:
$$\begin{split}
& y(t)= \mathcal{H}[x_{(-\infty,t]}](t) \quad \forall t\in\mathbb{R} \\
& y(n)= \mathcal{H}[x_{(-\infty,n]}](n) \quad \forall n\in\mathbb{Z}
\end{split}$$
3) Sistema $\mathcal{S}$ es *tiempo invariante*:
$$\begin{split}
& \mathcal{H}[x~\circ~d_{-\alpha}](t)= \mathcal{H}[x](t-\alpha)~\forall t,\alpha\in\mathbb{R} \\
& \mathcal{H}[x~\circ~d_{-n_{0}}](n)= \mathcal{H}[x](n-n_{0})~\forall n,n_{0}\in\mathbb{Z}
\end{split}$$
**Obs.** Sea la *homogeneidad* la propiedad de un sistema, tal que: $\mathcal{H}[\alpha x_{1}]=\alpha \mathcal{H}[x_{1}]$, y la *aditividad* la propiedad de un sistema, tal que: $\mathcal{H}[x_{1}+x_{2}]=\mathcal{H}[x_{1}]+\mathcal{H}[x_{2}]$.
Se puede demostrar que la homogeneidad **no implica** la aditividad (Ni para tiempo continuo ni discreto). Sin embargo, cuando $K=\mathbb{R}$, la aditividad *casi* implica homogeneidad. Para completar esta implicancia, el sistema debe ser *continuo*.

**Def.** Un sistema $\mathcal{S}_{c}$ es *continuo* si dada una familia $\{ x_{h}, h\in I\}\subset \mathcal{D}$ siendo $I\subset\mathbb{R}$ un intervalo y $h_{0} \in I$ tales que $\lim_{h\to h_{0}} x_{h}=x^{*}$ → $\lim_{h\to h_{0}} \mathcal{H}[x_{h}]=\mathcal{H}[x^{*}]$ (en el sentido de las funciones generalizadas).

**Def.** Un sistema $\mathcal{S}_{d}$ es *continuo* si dada una sucesión $\{ x_{j}, j\in \mathbb{Z}\}\subset \mathcal{P}$ tal que $\lim_{j\to \infty} x_{j}=x^{*}$ → $\lim_{j\to \infty} \mathcal{H}[x_{j}]=\mathcal{H}[x^{*}]$.

#### Prop.
Si un sistema $\mathcal{S}$ es aditivo y continuo → es homogéneo.

### Respuesta impulsiva
**Obs.** Se analizará la respuesta impulsiva en sistemas relajados, lineales y continuos.

#### En tiempo continuo:
$$y(t)=\mathcal{H}[x](t)=\int_{-\infty}^{\infty}x(\tau)h(t,\tau)d\tau$$
Donde $h(t,\tau)=\mathcal{H}[T_{(1,-\tau)}\delta](t)$ es la *respuesta impulsiva del sistema*, e indica cuál es la salida del mismo en el instante $t$ cuando se le aplica como entrada el impulso $\delta$ centrado en el instante $\tau$.

**Obs.** Trabajaremos con respuestas impulsivas que sean funciones generalizadas que involucren combinaciones lineales de la delta de Dirac y sus derivadas, del tipo $h(t,\tau)=\sum\limits_{n=0}^{N}\varphi_{n}(\tau)\delta^{(n)}(t-\tau)+h_{1}(t,\tau)$, por lo que obtenemos la siguiente expresión:
$$y(t)=\mathcal{H}[x](t)=\sum\limits_{n=0}^{N}(\varphi_{n}x)^{(n)}(t)+\int_{-\infty}^{\infty} x(\tau)h_{1}(t,\tau)d\tau$$
#### En tiempo discreto:
$$y(n)=\sum\limits_{k\in\mathbb{Z}}x(k)h(n,k)$$
Donde $h(n,k)=\mathcal{H}[\delta\circ d_{-k}](n)$ es la *respuesta impulsiva del sistema* y representa la salida del mismo en el instante $n$ correspondiente a la entrada $\delta$ aplicada en el instante $k$.
### Caracterizaciones que involucran a la respuesta impulsiva
**Obs.** Si un sistema lineal, continuo o discreto, está relajado en $t_{0}(n_{0})$ → $\forall t \geq t_{0}(n \geq n_{0})$:
$$\begin{split}
& y(t)=\int_{t_{0}}^{\infty}x(\tau)h(t,\tau)d\tau \\
& y(n)=\sum\limits_{k=n_{0}}^{\infty}x(k)h(n,k)
\end{split}$$
1) *Sistemas causales*
- En tiempo continuo: El sistema será causal $\leftrightarrow$ $h(t,\tau)=0$ si $t<\tau$, entonces:$$y(t)=\int_{-\infty}^{t}x(\tau)h(t,\tau)d\tau$$
A su vez, si el sistema también es relajado en $t_{0}$, para todo $t\geq t_{0}:$$$y(t)=\int_{t_{0}}^{t}x(\tau)h(t,\tau)d\tau$$
- En tiempo discreto: El sistema será causal $\leftrightarrow$ $h(n,k)=0$ si $n<k$, entonces: $$y(n)=\sum\limits_{K=-\infty}^{n}x(k)h(n,k)$$
A su vez, si el sistema causal está relajado en $n_{0}$, para todo $n\geq n_{0}:$ $$y(n)=\sum\limits_{K=n_{0}}^{n}x(k)h(n,k)$$
2) *Sistemas tiempo invariantes*
- En tiempo continuo: El sistema es tiempo invariante si $\mathcal{H}[x\circ d_{-\alpha}](t)=\mathcal{H}[x]\circ d_{-alpha}(t)$ $\forall~t,\alpha \in \mathbb{R}$, entonces:
$$y(t)=\int_{-\infty}^{\infty}x(t-\tau)h(\tau)d\tau=x*h(t)$$
- En tiempo discreto: El sistema es tiempo invariante si $\mathcal{H}[x\circ d_{-l}](n)=\mathcal{H}[x]\circ d_{-l}(n)$ $\forall~n,l \in \mathbb{Z}$, entonces:
$$y(n)=\sum\limits_{k\in\mathbb{Z}}x(n-k)h(k)=x*h(n)$$
### Sistemas de primer orden
Consideramos el sistema descripto por la ecuación diferencial: $a_{0}(t) \frac{dy}{dt}+a_{1}(t) y=f(t)$ → La solución a la ecuación será $y=y_{h}+y_{p}$, tal que $y_{h}=A\varphi(t)=Ae^{p(t)}$ y $y'_{p}(t)=C'(t)\varphi(t)+C(t)\varphi'(t)$, donde $C'(t)=\hat{\varphi}f(t)$
- Caso a: $f(t)=\delta(t-\tau)$ → $C(t, \tau)=\hat{\varphi}(\tau)u(t-\tau)$, y la respuesta impulsiva será $h(t,\tau)=\hat{\varphi}(\tau)\varphi(t)u(t-\tau)$.
- Caso b: $f(t)=\delta'(t-\tau)$ → $C(t,\tau)=\hat{\varphi}(\tau)\delta(t-\tau)-\hat{\varphi}'\tau u(t-\tau)$, y su respuesta iimpulsiva será $h(t,\tau)= \frac{1}{a_{0}(\tau)}\delta(t-\tau)-\hat{\varphi}'(\tau)\varphi(t)u(t-\tau)$.
### Sistemas de segundo orden
Consideramos el sistema descripto por la ecuación diferencial: $a_{0}(t) \frac{d^{2}y}{dt^{2}}+a_{1}(t) \frac{dy}{dt}+a_{2}(t)y=f(t)$ → $y=y_{h}+y_{p}$, tal que $y_{h}=A_{1}\varphi_{1}(t)+A_{2}\varphi_{2}(t)$ y $y_{p}=C_{1}(t)\varphi_{1}(t)+C_{2}(t)\varphi_{2}(t)$, donde $C'_{1}(t)=- \frac{f(t)\varphi_{2}(t)}{a_{0}(t)W(\varphi_{1}, \varphi_{2})(t)}$, $C'_{2}(t)= \frac{f(t)\varphi_{1}(t)}{a_{0}(t)W(\varphi_{1}, \varphi_{2})(t)}$ y el wronskiano es:
$$W(\varphi_{1}, \varphi_{2})(t)=det\begin{bmatrix}
\varphi_1(t) & \varphi_2(t) \\
\varphi'_1(t) & \varphi'_2(t)
\end{bmatrix}$$
Y la respuesta impulsiva será: $h(t,\tau)=C_{1}(t,\tau)\varphi_{1}(t)+C_{2}(t,\tau)\varphi_{2}(t)$.
### Integrales de Duhamel para un sistema $S_{c}$
Sea la repuesta de $\mathcal{H}[x]$ para un sistema lineal relajado y fijo para una entrada $x(t)$ → $(\mathcal{H}[x])'=\mathcal{H}[x']$.
### Estabilidad de sistemas LTI
**Def.** Un sistema $\mathcal{S}$ es BIBO-*estable* si a una entrada acotada le corresponde una salida acotada.
- En **tiempo continuo**: 
	- Sea $h(t)$ es una función continua a trozos tal que:	$$y(t)=(h*x)(t)=\int_{-\infty}^{\infty}h(\tau)x(t-\tau)d\tau \Rightarrow |y(t)| \leq M_{x}\int_{-\infty}^{\infty}|h(\tau)|d\tau$$
	Por lo tanto será BIBO-*estable* si $\int_{-\infty}^{\infty}|h(\tau)|d\tau < \infty$.
	- Sea $h(t)=k\delta(t)+h_{1}(t)$ cpn $k$ cte y $h_{1}(t)$ continua a trozos → El sistema será BIBO-*estable* $\leftrightarrow \int_{-\infty}^{\infty}h_{1}(\tau)d\tau < \infty$ (Se demuestra igual que en el anterior item).
- En **tiempo discreto**:
	Un sistema $\mathcal{S}_{d}$ LTI con respuesta impulsiva $h(n)$ es BIBO-*estable* $\leftrightarrow \sum\limits_{n\in\mathbb{Z}} |h(n)| < \infty$.
### Respuesta en frecuencia de un sistema LTI
##### En **tiempo continuo**: 
- La respuesta en frecuencia de un sistema $\mathcal{S}$ LTI con respuesta impulsiva $h(t)$ es: $$H(f)=\int_{-\infty}^{\infty}h(\tau)e^{-i2\pi f\tau}d\tau$$
> **Obs.**
> 1. La respuesta en frecuencia $H(f)$ es la transformada de Fourier de la respuesta impulsiva $h(t)$.
> 2. Las exponenciales complejas $e^{i2\pi ft}$ son *autofunciones* de $\mathcal{H}$ correspondientes a los valores $H(f)$ del mismo → $\mathcal{H}[e^{i2\pi ft}]=H(f)e^{i2\pi ft}$.

- La entrada $x(t)$ es una señal periódica de período $T$ → Su desarrollo en serie exponencial de Foruier será tal que $x(t)\sim \sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi nf_{0}t}$, con $f_{0}=\frac{1}{T}$, y $X_{n}=|X_{n}|e^{i \theta_{n} }$ → Sea $y(t)$ la salida del sistema LTI:
![[Pasted image 20231031092542.png]]
##### En **tiempo discreto**:
- La respuesta en frecuencia de un sistema $\mathcal{S}_{d}$ LTI con respuesta impulsiva $h(n)$ es: $$H(f)=\sum\limits_{k\in\mathbb{Z}} h(k)e^{-i2\pi fk}$$
> **Obs.**
> 1. Para un sistema $\mathcal{S}_{d}$ LTI si $x(\cdot)\to y(\cdot)$ entonces $y(n)=(h*x)(n)$, siendo $h(n)$ su respuesta impulsiva → Si aplico la transformada de Fourier en tiempo discreto para la igualdad → $Y(f)=X(f)H(f)$.
> 2. Igual que para tiempo continuo, $e^{i2\pi fn}$ son *autofunciones* de $\mathcal{H}$ correspondientes a los autovalores $H(f)$ → $\mathcal{H}[e^{i2\pi fn}]=H(f)e^{i2\pi fn}$.
> 3. Por la periodicidad de la transoformada de Fourier en tiempo discreto → Debo especificar $H(f)$ en un intervalo de longitud $1$, por lo que tomaremos por conveniencia $\frac{-1}{2}<f\leq \frac{1}{2}$.

### Análisis de sistemas LTI mediante la T.F
##### En **tiempo continuo**:
Sea la salida de un sistema $\mathcal{S}_{c}$, $y(t)=(h*x)(t)$ → $Y(f)=H(f)X(f)$.
- **Prop.** Sea $x(t)$ una *señal de energía* → Si el sistema LTI es BIBO-*estable* y la respuesta impulsiva $h(t)$ continua a trozos, y $\int_{-\infty}^{\infty}|Y(f)|^{2}df \neq 0$, la salida $y(t)$ del sistema será también de **energía**.
- Para señales de potencia, tomando $x(t)$ de potencia como entrada y $T>0$, entonces si tenemos lo siguiente ![[Pasted image 20231031095933.png]]
La relación entre las densidades espectrales de potencia de la salida y de la entrada es:
$$S_{y}(f)=\lim_{T\to \infty} \frac{1}{2T}|Y_{T}(f)|^{2}=\lim_{T\to \infty} \frac{1}{2T}|H(f)|^{2}|X_{T}(f)|^{2}=|H(f)|^{2}S_{x}(f)$$
##### En **tiempo discreto**:
- **Prop.** Sea $x(n)$ una *señal de energía* → Si el sistema LTI es BIBO-*estable* y  $\int_{<1>}|Y(f)|^{2}df \neq 0$, la salida $y(n)$ del sistema será también de **energía**.
- La densidad espectral de potencia de la transformada de Fourier en tiempo discreto de la señal de salida es:
$$S_{y}(f)=|Y(f)|^{2}=|H(f)|^{2}|X(f)|^{2}=|H(f)|^{2}S_{x}(f)$$
### Análisis de sistemas $\mathcal{S}_{c}$ LTI mediante la transformada de Laplace
**Def.** La *función de transferencia* del sistema $\mathcal{S}_{c}$ es la transformada de Laplace de la respuesta impulsiva del sistema:
$$H(s)=\mathcal{L}[h(t)](s)=\int_{0^{-}}^{\infty} h(t)e^{-st}dt$$
> **Observaciones sobre la función de transferencia**
> 1. Si el sistema es BIBO-*estable* → $\int_{0^{-}}^{\infty} |h(t)|dt<\infty$ → $H(s)$ existe para todo $s$ tal que $Re(s)>0$.
> 2. Si las singularidades de $H(s)$ tienen parte real nula → **No** garantizan la BIBO-*etabilidad*.
> 3. Para calcular la función de transferencia de un sistema $\mathcal{S}_{c}$ LTI descrito por ecuaciones diferenciales → Aplicamos la transformada de Laplace con condiciones iniciales nulas (sistema relajado):
> Tengo el sistema: $\sum\limits_{k=0}^{n}a_{k}y^{(k)}(t)=\sum\limits_{l=0}^{m}b_{l}x^{(l)}(t)$, entonces aplicando Laplace nos queda: $\sum\limits_{k=0}^{n}a_{k}s^{k}Y(s)=\sum\limits_{l=0}^{m}b_{l}s^{l}X(s)$ → $H(s)=\frac{Y(s)}{X(s)}= \frac{\sum\limits_{l=0}^{m}b_{l}s^{l}}{\sum\limits_{k=0}^{n}a_{k}s^{k}}= \frac{N(s)}{D(s)}$Y como los coeficientes son reales, los polos de $H(s)$ son reales o complejos conjugados.
> Para que sea BIBO-*estable* debe cumplirse que:
> a) $gr(N(s))\leq gr(D(s))$ → $m\leq n$. Sino el sistema no será BIBO-*estable*.
> b) Si los polos de $H(s)$ tienen parte real nula y son múltiples → La respuesta impulsiva no será módulo integrable, y el sistema no será BIBO.
> c) Si estos polos son simples el sistema tampoco será BIBO.

### Análisis de sistemas $\mathcal{S}_{d}$ LTI mediante la transformada $\mathcal{Z}$
**Def.** La *función de transferencia* de un sistema $\mathcal{S}_{d}$ LTI $\mathcal{S}$ causal, es la transformada $\mathcal{Z}$ de la respuesta impulsiva del mismo:
$$H(z)=\mathcal{Z}[h(n)](z)=\sum\limits_{k\geq0}h(k)z^{-k}$$
> **Observaciones sobre la función transferencia**
> 1. Si el sistema es BIBO-*estable* → $\sum\limits_{k\geq0}|h(k)|<\infty$ → $H(z)~\exists~\forall~|z|\geq 1$.
> 2. Si las singularidades de $H(z)$ están en el borde del círculo unitario no garantiza la BIBO-*estabilidad*.
> 3. Para calcular la función de transferencia de un sistema descrito por ecuaciones de diferencias a coeficientes ctes. → Aplicamos la transformada $\mathcal{Z}$ con condiciones iniciales nulas: $\sum\limits_{k=0}^{N}a_{k}z^{-k}Y(z)=\sum\limits_{l=0}^{M}b_{l}z^{-l}X(z)$ → $H(z)=\frac{Y(z)}{X(z)}= \frac{\sum\limits_{l=0}^{M}b_{l}z^{-l}}{\sum\limits_{k=0}^{N}a_{k}z^{-k}}= \frac{N(z)}{D(z)}$
> Para que el sistema con función de trasferencia $H(z)$ sea BIBO-*estable*, debe cumplirse que todos los polos de $H(z)$ estén dentro del circulo unitario, entonces necesariamente se cumplirá que $\lim_{n\to \infty} |h(n)|=0$.

### Interconexión de sistemas
Dados dos sistemas LTI con repuestas impulsivas $h_{1}(t)$ y $h_{2}(t)$, y sus respectivas respuestas en frecuencia $H_{1}(f), H_{2}(f)$ o funciones de transferencia $H_{1}(s),H_{2}(s)$, consideraremos 3 tipos de interconexiones:
1. **Interconexión en serie**:
![[Pasted image 20231101093404.png|400]]
Obtenemos que $y(t)=(h*x)(t)$, donde $h(t)=(h_{2}*h_{1})(t)$, y si transformamos por Laplace ambos miembros obtenemos que $H(s)=H_{2}(s)H_{1}(s)$.
2. **Interconexión en paralelo**:
![[Pasted image 20231101093801.png|400]]

Obtenemos que $y(t)=(h*x)(t)$, donde $h(t)=h_{1}(t)+h_{2}(t)$, y si transformamos por Laplace ambos miembros obtenemos que $H(s)=H_{1}(s)+H_{2}(s)$.
3. **Interconexión por realimentación**:
![[Pasted image 20231101094629.png]]
En este caso, obtenemos la siguiente expresión: $[\delta+h_{1}*h_{2}]*y(t)=h_{1}*x(t)$ y transformando por la Laplace, nos queda que $H(s)=\frac{Y(s)}{X(s)}=\frac{H_{1}(s)}{1+H_{1}(s)H_{2}(s)}$.