-----
[[Transformadas famosas]]
### Transformada en tiempo continuo
Sea $x:\mathbb{R}\to K$ tal que $\mathcal{F}[x(t)](f)=X(f)=\hat{x} (f)= \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt$ cuando la integral existe.
##### Prop
Si $x \in \mathcal{L}^{1}$ → $X(f) \exists~ \forall~ f \in \mathbb{R}$ y $X:\mathbb{R} \to K$ es uniformemente continua.
 ##### Obs
 ![[Pasted image 20230829102439.png|500]]
### Transformada en tiempo discreto
Sea $x:\mathbb{Z} \to K$, se define $\mathcal{F}_{d}[x(n)](f)=X(f)=\hat{x}(f)=\sum\limits_{n\in\mathbb{Z}} x(n)e^{-i2\pi f n}$, cuando la suma exista.
##### Prop
Si $x\in \mathcal{C}^{1}, \mathcal{F}_{d}[x(n)](f)\  \exists \ \forall f \in \mathbb{R}$. Además, $\mathcal{F}_{d}[x(n)](f)$ es periódica de período 1 y uniformemente continua.
 ##### Obs 
 ![[Pasted image 20230829103014.png|500]]
##### Obs
![[Pasted image 20230829103350.png]]
### Propiedades de la transformada de Fourier
1) **Dualidad:** 
	$\mathcal{F}[x](f)=X(f) \Longrightarrow \mathcal{F}[X](f)=x(-f)=x\circ e_{-1}$, donde $[e_{-1}(s)=-s]$
	Además, si $x$ es *par*: $F[X]=x$
	**Ej.**![[Pasted image 20230829104224.png]]
	##### Obs
	Para tiempo discreto se cumple que:![[Pasted image 20230829105045.png|600]]
2) **Linealidad:**
	Vale tanto para tiempo continuo como para tiempo discreto.
	![[Pasted image 20230829105201.png|500]]
3) **Desplazamiento en frecuencia:**
	$\mathcal{F}[x(t)e^{i2\pi f_{0}t}](f)=X(f-f_{0})=X\circ d_{-f_{0}}(f) \quad (d_{b}(s)=s+b)$
	$\mathcal{F}_{d}[x(n)e^{i2\pi f_{0}n}](f)=X(f-f_{0})$ 

  ##### Obs ![[Pasted image 20230829105809.png|500]]
4) **Desplazamiento en tiempo:**
	$\mathcal{F}[x(t-t_{0})](f)=X(f)e^{-i2\pi f_{0}t_{0}}$ (Tiempo coninuo)
	$\mathcal{F}_{d}[x(n-n_{0})](f)=X(f)e^{-i2\pi f_{0}n_{0}}$ (Tiempo discreto)

5) **Escalamiento en tiempo:**
	$\mathcal{F}[x(at)](f)=\frac{1}{ |a| }X(\frac{f}{a})$ con $a\neq 0$ 
	##### Obs ![[Pasted image 20230829112029.png|400]]
6) **Transformada de la derivada:**
	$x:\mathbb{R}\to K \quad x^{(k)} \in \mathcal{L}^{1} \quad k=0,1,...,n$, y $\lim_{ |t|\to\infty} x^{(k)}(t)=0 \quad k =0, 1, ..., n-1$ → $\mathcal{F}[x^{(n)}(t)](f)=(i2\pi f)^{(n)}X(f)$

7) **Derivada de la transformada:**
	En tiempo continuo: $t^{k}x(t)\in \mathcal{L}^{1} \quad k=0,1,...,n$, y $\mathcal{F}[x(t)](f)=X(f)$
	$\Longrightarrow \mathcal{F} [(-i2\pi t)^{n}x(t)](f)=\frac{d^{n}}{df^{n}}X(f)$
	Esto se debe, ya que: $\mathcal{F}[t^{k}\varphi (t)]=(\frac{-1}{i2\pi})^{k}\frac{d^{n}}{df^{n}}\mathcal{F}[\varphi (t)](f) \quad \forall k$
![[Pasted image 20230905091439.png]]
	En tiempo discreto: $\mathcal{F}_{d} [(-i2\pi t)^{m}x(n)](f)=\frac{d^{m}}{df^{m}}X(f)$
8) **Transformada de la convolución:**
	Si $x \leftrightarrow X,~ y \leftrightarrow Y \Longrightarrow \mathcal{F}[x*y(n)](f)=X(f).Y(f)$ 
### Antitransformada de Fourier
- En señales en tiempo discreto:
	Sea $x: \mathbb{Z} \to , x \in c^{1}$ y $x \leftrightarrow X, X$ es periódica y uniformemente continua.
	$X(f) = \sum\limits_{n\in\mathbb{Z}} x(n)e^{-i2\pi f k}$, notamos $\int_{<1>} ... df = \int_{f_{0}}^{f_{0}+1} ... df$
	Por lo que si quiero antitransformar:	$$\int_{<1>} X(f)e^{i2\pi fk} df =\int_{<1>}\sum\limits_{n\in\mathbb{Z}}x(n)e^{i2\pi f (k-n)}df=x(k)$$
	Ya que $$\int_{<1>}e^{i2\pi f (k-n)}df = \begin{cases} 
1 \quad k=n
\\ 0 \quad k\neq n
\end{cases}$$
Entonces, tenemos que:
$$\mathcal{F}_{d}^{-1}[X(f)](k)=\int_{<1>} X(f) e^{i2\pi f k}df = x(k)$$

- En señales en tiempo continuo:
Sea $x:\mathbb{R}\to K, \quad x(t)\leftrightarrow X(f)$, la transformada inversa de Fourier de $X(f)$ es:
$$\mathcal{F}_{d}^{-1}[X(f)](t)=\int_{-\infty}^{\infty} X(f) e^{i2\pi f t}df$$Cuando la integral existe.
1) Si $x(t) \in \mathcal{L}^{1}$ y continua, y $X(f) \in \mathcal{L}^{1} \Rightarrow x(t)=\int_{-\infty}^{\infty}X(f) e^{i2\pi f t}df \qquad \forall t \in \mathbb{R}$
2) Si $x(t) \in \mathcal{L}^{1}$, tiene un salto en $\tau$ y $\exists~ x'(\tau^{+}), x'(\tau^{-}) \Longrightarrow \frac{x'(\tau^{+})+x'(\tau^{-})}{2} = \lim_{L\to\infty} \int_{-L}^{L}X(f) e^{i2\pi f \tau}df$
### Extensiones de T.F
1) Extensión:
![[Pasted image 20230905095911.png]]
*Defino* $\mathcal{F}[x(t)](f)=X(f) \quad \forall~ f \in \mathbb{R}$. Se puede probar que si $y_{L}(t)=\int_{-L}^{L}X(f) e^{i2\pi f t}df \quad (L\in\mathbb{R})$ → $\lim_{L\to \infty} )=\int_{-\infty}^{\infty} |x(t) - y_{L}(t)|^{2}dt = 0$

![[Pasted image 20230905100404.png]]
Puedo ver como se reparte el campo de la energía en la frecuencia. Puedo calcular la energía conociendo la señal o de esta nueva forma, con la transformada de Fourier.

2) Transformada de Fourier de distribuciones
	Si $x \in \mathcal{D}$ *defino* $\mathcal{F}[x(t)](f) \in \mathcal{D}$ en la siguiente forma: Dada $\varphi \in C_{0}^{\infty}, <\mathcal{F}[x(t)](f), \varphi (f)> = <x(t),\hat{\varphi}(t)>$
	##### Obs
	 $\varphi \in C_{0}^{\infty} \Rightarrow \hat{\varphi}\in C_{0}^{\infty}$ 
![[Pasted image 20230905193620.png]]
##### Obs
Para las transformadas de Fourier de las distribuciones valen las siguientes propiedades de la transformada de Fourier:
- Dualidad
- Desplazamiento en frecuencia
- Desplazamiento en tiempo
- Escalonamiento
- Derivación de la transformada
- Transformación de la derivada
- Transformación de la convolución
### Transformada de la integral de una función
$x(t) \in \mathcal{L}^{1}, x \leftrightarrow X(f)$ → $\mathcal{F}[\int_{-\infty}^{t}x(s)ds](f)=X(f).U(f)=\frac{X(f)\delta (f)}{2} + \frac{X(f)}{i2\pi f}=\frac{X(0)\delta(f)}{2}+ \frac{X(f)}{i2\pi f}$
#### Transformada de Fourier de una función periódica
1)  Transformada de Fourier de series de distribuciones (funciones generalizadas):
	Sea ${x_{k}, k \in \mathbb{N}}$ una sucesión de funciones generalzadas y para cada $n \in  \mathbb{N}$, tenemos que $S_{n}=\sum\limits_{k=1}^{n}x_{k}$ → La función generalzada $x$, es la suma de la serie de las ${x_{k}}$ → $x=\sum\limits_{k\geq1} x_{k} \leftrightarrow x= \lim_{n\to\infty} S_{n}$.
	Por lo que cada función de prueba $\phi$, si $\alpha_{k,\phi}=< x_{k},\phi > \to \exists$ la serie $\alpha_{\phi}=\sum\limits_{k\geq1} \alpha_{k,\phi}=<x,\phi>$
2)  Transformada de Fourier de funciones periódicas:
	Sea $x(t)$ una función cont. a trozos, periódica de período $T$, y tal que en toda discontinuidad de $x$ existan sus derivadas laterales. Además, $f_{0}=\frac{1}{T}$ y $X_{n}$ son sus coeficientes en serie exponencial → Por hipótesis, $x$ es una función generalizada regular.
	$$x(t)=\sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi nf_{0}t}$$
		
		Vale como igualdad de funciones generalizadas salvo en una cantidad  finita de                                      discontinuidades

Entonces obtenemos lo siguiente:
$$\mathcal{F}[x(t)](f)=\sum\limits_{n\in\mathbb{Z}}X_{n}\delta (f-nf_{0})$$

![[Pasted image 20230909103245.png]]
### Transformada de Fourier en tiempo discreto
Dada una señal en tiempo discreto $x(n)$ se define su transformada de Fourier, como:
$$\mathcal{F}_{d}[x(n)](f)=\sum\limits_{n\in\mathbb{Z}}x(n)e^{-i2\pi nf}$$
en el caso en que la serie converja.
##### Obs
![[Pasted image 20230909104437.png]]
###### Existencia de la T.F en tiempo discreto
![[Pasted image 20230909104617.png]]
### Transformada inversa de Fourier en tiempo discreto
Por el teorema 3, se probó que la serie converge uniformemente, entonces:
$$\int_{<1>}X(f)e^{i2\pi f n} df = x(n)$$
Siendo la notación: $X(f)=\mathcal{F}_{d}[x(n)](f)$ 
##### Props
![[Pasted image 20230912090528.png|600]]
![[Pasted image 20230912105806.png|600]]
![[Pasted image 20230912105846.png|600]]
![[Pasted image 20230912105914.png|600]]
### Transformada de Fourier y ecuaciones diferenciales ordinarias
![[Pasted image 20230909103704.png]]
##### [[Ejemplo, EDO]]
##### Algunas transformadas
![[Pasted image 20230911162923.png|400]]
### Diagramas espectrales
Sea $x:\mathbb{R}\to \mathbb{R}, ~ x\leftrightarrow X$, donde $X(f)=\int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt$, entonces:
$$\begin{split}
& X(f)=\int_{-\infty}^{\infty}x(t)cos(2\pi ft)dt-i\int_{-\infty}^{\infty}x(t)sen(2\pi ft)dt \\
& X^{*}(f)=X(-f)=\int_{-\infty}^{\infty}x(t)cos(2\pi ft)dt+i\int_{-\infty}^{\infty}x(t)sen(2\pi ft)dt
\end{split}$$

Si $X(f)=|X(f)|e^{i\theta f}, ~ X(-f)=|X(f)|e^{i\theta (-f)}, ~ X^{*}(f)=|X(f)|e^{-i\theta f}$
Donde nos resulta interesante para los diagramas, las siguientes igualdades:
$$|X(f)| = |X(-f)| = |X^{*}(f)| \qquad -\theta f= \theta (-f)$$
#### Obs
- El *diagrama bilateral de amplitud* ($|X(f)| ~vs~ F$) va a ser **simétrico respecto del eje de las "$y$"**.
- El *diagrama bilateral de fase* ($\theta (f) ~ vs ~ f$) va a ser **simétrico respecto del origen**.
### Densidades espectrales
Sea $x:\mathbb{R}\to K$. Si $x(t)$ es de *energía* → Existe $0<\int_{-\infty}^{\infty}|x(t)|^{2}dt < \infty$
Por la igualdad de Parseval, si $X(f)= \mathcal{F} [x(t)](f) \to E_{x}= \int_{-\infty}^{\infty}|x(t)|^{2}dt = \int_{-\infty}^{\infty}|X(f)|^{2}df$

Sea la **densidad espectral de energía** $G_{x}(f)=|X(f)|^{2} \Rightarrow E_{x}=\int_{-\infty}^{\infty}G_{x}(f) df$

> Si $0 \leq f_{1} < f_{2}$ → $E_{x[f1,f2]}=\int_{f1}^{f2}G_{x}(f) df + \int_{-f2}^{-f1}G_{x}(f) df$
> ![[Pasted image 20230912095621.png|200]]
![[Pasted image 20230912100228.png]]

Sea $X_{T} \in \mathcal{L}^{2}$, de *potencia*, y $P=\lim_{T\to\infty} \frac{1}{2T}\int_{-\infty}^{\infty}|x_{T}(t)|^{2}dt$, por la *igualdad de Parseval* $|x_{T}(t)|^{2}=|X_{T}(f)|^{2}$, por lo tanto:
Sea $S(f)=\lim_{T\to\infty} \frac{1}{2T}|X_{T}(f)|^{2}$ la **densidad espectral de potencia** de $x$ → $P=\int_{-\infty}^{\infty}S(f)df$