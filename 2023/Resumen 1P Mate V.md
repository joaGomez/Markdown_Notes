# Señales
##### En tiempo continuo
$$u(t) =
\begin{cases} 
0 \quad t < 0
\\ 1 \quad t \geq 0 
\end{cases}$$
$$r(t) =
\begin{cases} 
0 \quad t \le 0
\\ t \quad t > 0 
\end{cases}$$
$$p(t) =
\begin{cases} 
0 \quad t \le 0
\\ \frac {t^2}{2} \quad t > 0 
\end{cases}$$
$$\prod(t) =
\begin{cases} 
1 \quad |t| < \frac{1}{2} \\
0 \quad |t| > \frac{1}{2}
\end{cases}$$
$$\Lambda(t) =
\begin{cases} 
1 \ - \ |t| \quad |t| \leq 1
\\ 0 \ \ \ \quad \quad \quad |t| \geq 1 
\end{cases}$$
$$x(t) = A\cos(2\pi f_{0}t+\theta)$$
##### En tiempo discreto
$$\delta(n-n_{0})=\begin{cases} 
1 \quad n=n_{0} \\
0 \quad n\neq n_{0}
\end{cases}$$
### Periodicidad de una función
Sea $x:R \to K$, es una funcion periodica si $\exists \ \tau > 0 \ /$ $x(t+\tau) = x(t) \ \forall\  t \in R$  $\to$ $\tau$ es período de $x(t)$. Ademas, para cualquier $n \in N$ fijo: $x(t) = x(t+n\tau) \ \forall\  t \in R$.

**Tiempo continuo**: $T_0$ será el período fundamental de $x(t)$ / $T_{0}= inf\{ \tau > 0 \ / \ x(t+\tau) = x(t)\}$.

**Tiempo discreto**: $N_0$ será el período fundamental de $x(n)$ / $N_{0}= inf\{ N > 0 \ / \ x(n+N) = x(t)\}$.

#### Prop.
Si consideramos un senoide de forma: $x(t) = A\cos(2\pi f_{0}t+\theta)$ $\to$ para cada $n \in N$, $\tau_{n} = \frac{n}{f_0}$, y $T_{0} = \frac{1}{f_0}$ es su período fundamental.
#### Prop.
Si $x(t) = a = cte$ $\to$ La función es periódica pero no tiene período fundamental.
### Combinación lineal de señales periódicas
Sean $a_{1}\ y \ a_{2}$ no nulos, $x_{1} (t) \ y \  x_{2}(t)$ periódicas de períodos $T_{1} \ y \ T_{2}$ $\to$  $z(t) = a_{1}x_{1}(t) + a_{2}x_{2}(t)$ es periódica $\leftrightarrow$ $\frac{T_1}{T_{2}}= q$, con $q$ un numero racional.

- Si $\frac{T_{1}}{T_{2}} = \frac{p}{q}$, con $p,q \in N$ coprimos, $T_{0} = q T_{1} = p T_{2}$.
- Sean $a_{i}, i = 1, ... ,m$ no nulos y $x_{i}(t), i = 1, ... , m$ periódicas de períodos $T_{i}$. $\to$ $z(t) = \sum\limits_{i=1}^{m}a_{i}x_{i}(t)$ es periódica de período $T_{0} \leftrightarrow \frac{T_{1}}{T_{i}} = \frac{p_{i}}{q_{i}}$, $i = 2, ... , m$, con $p_{i},q_{i} \in N$ coprimos $(2 \leq i \leq m) \to T_{0} = (mcm \{ q_{2},...,q_{m}\})T_{1}$
- Sean $a_{i}, i = 1, ... ,m$ no nulos y $x_{i}(n), i = 1, ... , m$ periódicas de períodos $N_{i}$. $\to$ $z(n) = \sum\limits_{i=1}^{m}a_{i}x_{i}(n)$ es periódica de período $N_{0} = mcm \{ N_{1},...,N_{m}\}$.
### Desplazamiento en tiempo
Sea $\alpha \in I$, $d_{\alpha}:I \to I$, $d_{\alpha} (\mu) = \mu + \alpha$, $\mu \in I$, es el desplazamiento en tiempo. Y $d_{\alpha}^{-1} : I \to I$, $d_{\alpha}^{-1} = d_{- \alpha}$ → $x: \mathbb{R} \to \mathbb{R},~ \alpha=t_{0}, ~x\circ d_{t_{0}} (t)=x(t+t_{0})$
### Escalonamiento en tiempo
Sea $\beta \in I$, $\beta \neq 0, e_{\beta} : I \to I$, $e_{\beta} (\mu) = \beta \mu$, $\mu \in I$, es el escalonamiento en tiempo. Solo para el caso donde $I = R$, está definida $e_{\beta}^{-1} : R \to R, e_{\beta}^{-1} = e_{\frac{1}{\beta}}$ → $x: \mathbb{R} \to \mathbb{R},~ \beta=a>0, ~x\circ e_{a} (t)=x(at)$
### Representación espectral de señales
Sea $x(t) = A \ cos(2\pi f_{0}t+\theta) = A \ cos(\omega_{0}t+\theta), \omega_{0}=2\pi f_{0}$, $-\pi < \theta \leq \pi, A > 0$ 
$\to x(t) = Re(A \ e^{i(\omega_{0}t+\theta)})= Re(A\ e^{i\theta} e^{i\omega_{0}t}) = Re(\vec{X} e^{i\omega_{0}t}) = Re(\tilde{x} (t))$, donde $\vec{X}$ es un fasor, y $\tilde{x}(t)$ es un fasor rotatorio.
#### Diagrama unilateral
Se llama diagrama unilateral cuando la amplitud, la fase y la frecuencia son fijos para todos los valores en $I$ / $x(t) \to \{A, \theta, f_{0}\}$. Y si tengo una señal de la forma: $x(t)=\sum\limits_{i=1}^{n} A_{i}\ cos(2\pi f_{i}\ t+\theta_{i})$ → $x \leftrightarrow \{ \{A_{1}, \theta_{1}, f_{1}\},...,\{A_{n}, \theta_{n}, f_{n}\}\}$.
#### Diagramas bilaterales
Por otro lado, los diagramas bilaterales tienen en cuenta la expresión de la señal como la semisuma de su fasor rotatorio y su conjugado. Por lo tanto, $x \leftrightarrow \{ \{\frac{A}{2},\theta,f_{0}\}, \{\frac{A}{2},-\theta,-f_{0}\}\}$. Si tengo una señal de la forma: $x(t)=\sum\limits_{i=1}^{n} A_{i}\ cos(2\pi f_{i}\ t+\theta_{i})$ → $x \leftrightarrow \{ \{\frac{A_{1}}{2}, \theta_{1}, f_{1}\},\{\frac{A_{1}}{2}, -\theta_{1},-f_{1}\},...,\{\frac{A_{n}}{2}, \theta_{n}, f_{n}\}, \{\frac{A_{n}}{2},-\theta_{n},-f_{n}\}\}$.
##### Obs
En la representación bilateral, el espectro de la amplitud es **PAR**, y el espectro de fase es **IMPAR**.
### Energía y potencia
#### Def
Sea $x$ una señal en tiempo continuo, $x$ es de **energía** si: $0 < \lim_{t\to +\infty}\int_{-T}^{T}|x(t)|{^{2}}dt < \infty \Longrightarrow 0 < Ex=V.P.\int_{-\infty}^{\infty}|x(t)|^{2}dt < \infty$
#### Def
Sea $x$ una señal de tiempo continuo, $x$ es de **potenica** si: $0 < lim_{T\to \infty} \frac{1}{2T}\int_{-T}^{T}|x(t)|^{2}dt < \infty \Longrightarrow 0 < P_{x}=lim_{T\to \infty} \frac{1}{2T}\int_{-T}^{T}|x(t)|^{2}dt < \infty$
##### Prop
Una señal **NO** puede ser de potencia y de energía al mismo tiempo
##### Útil
$|e^{i\omega_{0}n}|=|e^{-i\omega_{0}n}|=1$
- Si tengo $y=x(\alpha t)$ → $E_{y}=\frac{E_{x}}{|\alpha|}$ y $P_{y}=P_{x}$.
##### Prop
Por la identidad de Parseval, la potencia de la suma es la suma de las potencias. Siempre y cuando, que sea una combinacion lineal de funciones ortogonales.
### Transformaciones lineales
Sea $x:R \to K$, la generalización de $x$ debe basarse en que no importan los valores individuales de $x$ sino su comportamiento global.
Supongo que $x$ es continua a trozos. Considero el conjunto de las funciones de prueba:
$C_{0}^{\infty}=\{\varphi:\Re \to K, C^{\infty}$ y que se anula fuera de $[-M_{\varphi},M_{\varphi}]\}$
##### Prop.
Sea $\alpha_{1}, \alpha_{2} \in K, \varphi_{1},\varphi_{2} \in C_{0}^{\infty}$ → $<x,\alpha_{1}\varphi_{1}+\alpha_{2}\varphi_{2}>=\alpha_{1}<x,\varphi_{1}>+\alpha_{2}<x,\varphi_{2}>=\int_{-\infty}^{\infty}x(t)[\alpha_{1}\varphi_{1}(t)+\alpha_{2}\varphi_{2}(t)]dt$
#### Def.
$<x,\bullet>:C_{0}^{\infty}\to K$ es una **Transformación Lineal**
  ###### Obs
  Como $C_{0}^{\infty}$ es un espacio de funciones → $<x,\bullet>$ es una función lineal
  ##### Notación
  Sea $L_{x}:C_{0}^{\infty}\to K$ tal que $L_{x}(\varphi)=\int_{-\infty}^{\infty}x(t)\varphi(t)dt$ → $L_{x}$ es una **Transformación Lineal**
### Funciones generalizadas
#### Def
Una distribución (función generalizada) es una función lineal (continua) sobre $C_{0}^{\infty}$ / $D=\{distribución \ sobre \ C_{0}^{\infty}\}$
#### Def.
$G\in D$ es una distribución regular si $\exists \ y:\ R \to K$ continua  a trozos tal que $<G,\varphi> = \int_{-\infty}^{+\infty}y(t)\varphi(t)dt \quad \forall \varphi \in C_{0}^{\infty}$
###### Obs.
$\exists$ distribuciones no regulares, como $\delta(t)$, conocida como, la **Delta de Dirac**: $<\delta, \varphi>=\varphi(0), \forall \varphi \in C_{0}^{\infty}$
##### Prop
$$\int_{a}^{b}f(t)\delta (t-t_{0})dt = 
\begin{cases} 
f(t_{0}) \quad t_{0}\in [a,b]\\
0 \quad \ \ \ \quad t_{0}\notin [a,b] \\
Indefinido \quad t_{0}=a \lor t_{0}=b
\end{cases}$$
### Igualdad en distribuciones
Si $\eta,\mu \in D$, digo que $\eta = \mu ~~~\leftrightarrow~ <\eta,\varphi>=<\mu, \varphi>, \forall \varphi \in C_{0}^{\infty}$
### Derivadas generalizadas de distribuciones
Sea $\eta \in D$, su derivada $\eta \ '$ está dada por: $<\eta \ ', \varphi>=-<\eta, \varphi \ '>, \forall  \varphi \in C_{0}^{\infty}$
- Su derivada de orden $n \in N$ está dada por:  $<\eta^{(n)}, \varphi>=(-1)^{n} <\eta, \varphi^{(n)}>, \forall  \varphi \in C_{0}^{\infty}$
###### Obs
Si $\varphi \in C_{0}^{\infty} \to \varphi^{(k)} \in C_{0}^{\infty}, \forall k \in N$
##### Derivadas generalizadas famosas
| Función |  Derivada   |
|:-------:|:-----------:|
|  r(t)   |    u(t)     |
|  u(t)   | $\delta(t)$ |
|         |             |

### Composición de funciones generalizadas con funciones
$\eta \in D, g:\Re \to \Re (g \in C_{0}^{\infty})$ estrictamente monótona $(g'(t)\neq 0 \forall t)$. Sea $x$ continua a trozos y sea $\varphi \in C_{0}^{\infty}$
$$<x \ \circ \ g, \varphi> = \int_{-\infty}^{\infty}(x \ \circ \ g)(t)\varphi(t)dt=\int_{-\infty}^{\infty}(\frac{x(\tau)}{|g'(g^{-1}(\tau)|})\varphi(g^{-1}(\tau))d\tau=<x,\frac{1}{|g'(g^{-1}(\tau)|}(\varphi \ \circ \ g^{-1}(.))>$$
### Delta de Dirac
#### Def
$$<\delta,\varphi>=\int_{-\infty}^{\infty}\delta (t)\varphi (t)dt = \varphi(0)$$
#### Propiedades
$$\begin{split}
&<x, \varphi>=\int_{-\infty}^{\infty}x(t)\varphi(t)dt \quad \quad \varphi \in C_{0}^{\infty} \\
& \delta^{(n)}(at)= \frac{1}{|a|} (\frac{1}{a})^{n} \delta^{(n)}(t) \\
& g(t)\delta^{(n)}(t-t_{0})=\sum\limits_{j=0}^{n} (-1)^{n-j}\binom{n}{j}g^{(n-j)}(t_{0})\delta^{(j)}(t-t_{0}) \\
& \delta(f(t))=\sum\limits_{n\in\mathbb{Z}} \frac{1}{|f'(t_{n})|}\delta(t-t_{n})
\end{split}$$
### Convolución lineal
#### Tiempo continuo
$$(x\ast y)(t)=\int_{-\infty}^{\infty}x(\tau)y(t-\tau)d\tau$$
#### Tiempo discreto
$$(x\ast y)(n)=\sum\limits_{k=-\infty}^{\infty}x(k)y(n-k)$$
#### Propiedades
- $(x\ast y)=(y\ast x)$
- $(x\ast y)\ast z=x\ast (y\ast z)$
- $(ax+by)\circledast z(t)=a.x\circledast z(t)+b.y\circledast z(t)$
- $x,y$ continuas a trozos en $\mathbb{R}$ → $(x\ast y)$ continua en $\mathbb{R}$
- $x,y \in \mathcal{L^{1}}$ → $(x\ast y) \in \mathcal{L^{1}}$
- $x,y,x',y' \in \mathcal{L^{1}}$ → $(x\ast y)'=(x'\ast y)=(x\ast y') \in \mathcal{L^{1}}$
#### Famosas
- $(\prod\ast\prod)(t)=\Lambda(t)$
- $(x\ast u)(t)=\int_{-\infty}^{t}x(\tau)d\tau$
- $(x\ast u)(n)=\sum\limits_{k=-\infty}^{n}x(k)$
- $x(t)\ast\delta(t-t_{0})=x(t-t_{0})$
### Problema de la división
Dadas $y\in D, g$ una función analítica → Encontra $x \in D / g.x=y$
###### Obs
  Si $g(t)\neq 0 \forall t$ → $\frac{1}{g(t)}$ es analítica → $x=\frac{y}{g}$
  En todo otro caso:
  - Encontrar la sol. gral $x_{h}$ del problema homogéneo / $g.x=0$
  - Encontrar una sol. particular $x_{p}$ de $g.x=y$, la sol. buscando $x=x_{h}+x_{p}$ 
  ### Solución general de la homógenea
  - $g$ tiene un único cero de orden $n$ en $t=a$ → $g(t)=(t-a)^{n}g_{1}(t)$, con $g_{1}$ analítica y $g_{1}(a)\neq 0$
   → $x_{h}(t)=c_{0} \ \delta(t-a)+c_{1} \ \delta'(t-a)+...+c_{n-1} \ \delta^{n-1}(t-a)$
   ###### Obs
   Notar que $<\delta^{n}(t-a),\varphi>=(-1){^n}\varphi^{(n)}(a)$ con $c_{0},c_{1},...,c_{n-1}$ arbitrarios
  - $g$ tiene ceros $\{t_{k}, k\in Z\}$, $t_{k}$ tiene orden $n_{k}$ y $\nexists \ \lim_{k \ \to \ \pm \ \infty}t_{k}$ → $x_{h}=\sum\limits_{k\in Z}x_{h,k}$ con $x_{h,k}=c_{0}^{k} \ \delta(t-t_{k})+c_{1}^{k} \ \delta'(t-t_{k})+...+c_{n_{k-1}}^{k} \ \delta^{n_{k-1}}(t-t_{k})$
   ### Solución particular
### Convolución periódica
Dadas dos señales en tiempo discreto $x(n),\ y(n)$ periódicas de período $N$, su **convolución periódica ($x\circledast y$)** es la siguiente señal en tiempo discreto:
$$x \circledast y (n) = \sum\limits_{k=0}^{N-1}x(k)y(n-k), \quad n\in Z$$
#### Propiedades
- $x\circledast y(n+N)=x\circledast y(n)$
- $\sum\limits_{k=n_{0}}^{n_{0}+N-1}x(k)y(n-k)=\sum\limits_{s=0}^{N-1}x(s)y(n-s)$
- $(x\circledast y)=(y\circledast x)$
- $(x\circledast y)\circledast z=x\circledast (y\circledast z)$
- $(ax+by)\circledast z(n)=a.x\circledast z(n)+b.y\circledast z(n)$
#### Obs
Deducimos que para cualquier par de señales $x(n), y(n)$, periódicas de período $N$ y $\forall \ n_{0}\in Z$ se verifica: $\sum\limits_{k=n_{0}}^{n_{0}+N-1}x(k)y(k)=\sum\limits_{k=0}^{N-1}x(k)y(k)$.
# Series de Fourier
#### Serie generalizada
Sea $V$ un $K-espacio \ vectorial$ con producto interno y $\phi=\{\phi_{k}, k\in N\}$ un conjunto ortogonal y $0 \notin \phi$ 
$$v=\sum\limits_{k=1}^{n}c_{k}\phi_{k}$$
tal que $c_{j}=\frac{<w,\phi_{j}>}{<\phi_{j},\phi_{j}>}=\frac{<w,\phi_{j}>}{||\phi_{j}||^2}$ con $1\leq j \leq n$.
Entonces la serie generalizada de Fourier es:
$$v=\sum\limits_{k=1}^{n}\frac{<w,\phi_{k}>}{||\phi_{k}||^2}\phi_{k}$$
### Desigualdad de Bessel
$$\sum\limits_{k=1}^{\infty}|c_{k}|^{2}||\phi_k||^{2}\leq||v||^{2}$$
##### Def
se dice que $\Phi \subset V$ es *completo* si dado $v \in V$ tal que $<v, \phi> =0\ \forall \ \phi \in \Phi \to v = 0$.
Para un conjunto $\Phi$ completo → Vale la **igualdad de Parseval**
$$\sum\limits_{k=1}^{\infty}|c_{k}|^{2}||\phi_{k}||^{2} = ||v||^{2} \longrightarrow (\sum\limits_{k=1}^{\infty}|c_{k}|^{2}||\phi_{k}||^{2})^{\frac{1}{2}} = ||v||$$
### Convergencia en norma
Se escribe $v\sim\sum\limits_{k=1}^{\infty}c_{k}\phi_{k}$, donde se entiende a $\sim$ como que la serie converge a $v$ en norma → $\lim_{n\to \infty}||\sum\limits_{k=1}^{n}c_{k}\phi_{k}- v|| = 0$ 
##### Def
Decimos que $\sum\limits_{k=1}^{n}c_{k}\phi_{k}$ es la **serie generalizada de Fourier**. 
   ###### Propiedades
   - **Unicidad**: Sean $x_{1}, x_{2}$ dos series generalizadas de Fourier con los mismos coeficientes → $x_{1}=x_{2}$ → $||x_{1}-x_{2}|| = 0$. Además verifica: $<x_{1}-x_{2},\phi_{n}> =     <x_{1},\phi_{n}> - <x_{2},\phi_{n}> = 0~\forall \phi_{n} \in \phi$
   - **Linealidad**: Sean $x, y$ dos vectores de $V$, de coeficientes de Fourier $\{X_{n}, n \in \mathbb{N}\}$ e $\{Y_{n}, n \in \mathbb{N}\}$, con $\alpha, \beta \in K$ → Los coeficientes de Fourier de $\alpha x + \beta y$ son $\{\alpha X_{n}+\beta Y_{n}, n \in \mathbb{N}\}$, y por las propiedades de linealidad de producto interno, obtenemos que:$$\frac{<\alpha x+\beta y,\phi_n>}{||\phi_{n}||^{2}}=\alpha\frac{<x,\phi_n>}{||\phi_{n}||^{2}} + \beta\frac{<y,\phi_n>}{||\phi_{n}||^{2}} =\alpha X_{n}+\beta Y_{n} \ \forall n \in N$$
### Series exponenciales de Fourier
#### En tiempo discreto
Sea $N \in \mathbb{N}$ un número fijo. Considero $I_{N}=\{0,...,N-1\}$ tal que $V:\{x:I_{N}\to \mathbb{C}\}$ es un espacio vectorial de dimensión finita (N), ya que es isomorofo a $\mathbb{c}^{N}$, conjunto de las N-uplas de números complejos, mediante la asignación: $x \longrightarrow (x(0),...,x(N-1))$.
 ##### Prop
 Sean $x,y \in V$, se define el producto interno tal que: $$<x,y> = \sum\limits_{n=0}^{N-1}x(n)y^{*}(n)$$Por lo tanto dado que $V$ es de dmensión finita → $w$ ya no será una proyeccón ortogonal de $x$, sino que será la representación *exacta* de $x$ en los términos de la base $\Phi$, es decir, que podemos escribir
$$x(n)=\sum\limits_{k=0}^{N-1}c_{k}e^{i2\pi f_{0}kn}, \qquad \forall\ n \in \mathbb{Z}$$
$$c_{k}=\frac{1}{N}\sum\limits_{n=0}^{N-1}x(n)e^{-i2\pi f_{0}kn}$$
#### Propiedades
Considero dos señales en tiempo discreto $x_{1}(n), x_{2}(n)$ periódicas de período $N$ con coeficientes de Fourier $\{ c_{k}\}$ y $\{ d_{k}\}$
1. **Desplazamiento en tiempo:**
	Sean $n_{0} \in \mathbb{Z}, y(n)=x_{1}(n-n_{0}), n \in \mathbb{Z}$ y $\{ h_{k} \}$ los coeficientes de Fourier de $y(n)$ 
	→ $h_{k}=e^{-i2\pi f_{0}kn_{0}}c_{k}$
2. **Convolución periódica:**
	Sean $\{ h_{k} \}$ los coeficientes de Fourier de $x_{1} \circledast x_{2}(n)$ → $h_{k} = N c_{k} d_{k}$
#### En tiempo continuo
Sea $x:[t_{0},t_{0}+T]\to \mathbb{K}$, la serie exponencial de Fourier que se le asocia es:
$$x(t)\sim \sum\limits_{k\in\mathbb{Z}}X_{k}e^{ik\omega_{0}t}$$
Con los coeficientes: $X_{k}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T}x(t)e^{-ik\omega_{0}t}dt$
#### Igualdad de Parseval
$$\sum\limits_{k\in \mathbb{Z}} |X_{k}|^{2}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T}|x(t)|^{2} dt$$
#### Función nula
La función nula no es la función que vale 0 en todo su dominio, sino quees el *conjunto de todas las funciones* $\mu \in \mathcal{L}_{(t_{0}, T)}^{2}$ que 
verifican:
$$\int_{t_{0}}^{t_{0}+T}|\mu(t)|^{2}dt=0$$
#### Prop
Con el resultado anterior, podemos definir de otra forma la igualdad entre dos funciones, tal que, si $\exists\ x_{1},x_{2} \in \mathcal{L}_{(t_{0}, T)}^{2}$
entonces:
$$x_{1}=x_{2}\Leftrightarrow \int_{t_{0}}^{t_{0}+T}|x_{1}(t)-x_{2}(t)|^{2}dt=0$$
### Serie trigonométrica de Fourier
$$x(t)\sim a_{0}+\sum\limits_{n\in\mathbb{N}}a_{n}cos(n\omega_{0}t)+b_{n}sen(n\omega_{0}t)$$
Y los coeficientes serán:
$$\begin{split} 
& a_{0}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T}x(t)dt \\
& a_{n}= \frac{2}{T}\int_{t_{0}}^{t_{0}+T}x(t)cos(n\omega_{0}t)dt \qquad n\in \mathbb{N} \\
& b_{n}=\frac{2}{T}\int_{t_{0}}^{t_{0}+T}x(t)sen(n\omega_{0}t)dt \qquad n\in \mathbb{N}
\end{split}$$
#### Igualdad de Parseval
$$\frac{2}{T}\int_{t_{0}}^{t_{0}+T}|x(t)|^{2}dt=2|a_{0}|^{2}+\sum\limits_{n\in\mathbb{N}}|a_{n}|^{2}+|b_{n}|^{2}$$
#### Obs
Supongamos que la serie exponencial converge a $x(t)$ en el intervalo $[t_{0}, t_{0}+T]$:
$$x(\tau)=\sum\limits_{k\in \mathbb{Z}}X_{k}e^{ik\omega_{0}\tau} = \sum\limits_{k\in \mathbb{Z}}X_{k}e^{ik\omega_{0}(\tau+nT)}\qquad \forall \tau \in [t_{0},t_{0}+T], n\in \mathbb{Z}$$
#### Propiedades
- Teniendo en cuenta esta última superposición, y dado que $e^{in\omega_{0}t}, cos(n\omega_{0}t)$ y $sen(n\omega_{0}t)$ son también funciones periódicas de período $T$, obtenemos la siguiente propiedad:
$$\int_{t_{0}}^{t_{0}+T}x(t)dt=\int_{0}^{T}x(t)dt=\int_{-\frac{T}{2}}^{\frac{T}{2}}x(t)dt$$
- **Desplazamiento en $\tau$:** 
Sea $x(t)$ periódica de período $T$ y supongamos que $\{ X_{n}, n \in \mathbb{Z} \}$ son sus coeficientes de la serie exponencial y sea $y(t)=x(t+\tau)$ $$Y_{n}=X_{n}e^{in\omega_{0}\tau}$$
Si tengo que $z(t)=x(t)e^{-i2\pi f_{0}kt}$, entonces la relación de sus coeficientes será:$$Z_{n}=x_{n-k}$$
- **Coeficientes de la serie exponencial y trigonométrica:**
Sea $x(t)$ periódica de período $T$ y supongamos que $\{ X_{n}, n\in \mathbb{Z} \}$ y $\{ a_{0},a_{n}, b_{m}, n, m\in\mathbb{N} \}$ son sus coeficientes de la serie exponencial y la trigonométrica.$$X_{0}= a_{0}\qquad X_{n}= \frac{1}{2}(a_{n}-ib_{n}) \qquad X_{-n}=\frac{1}{2}(a_{n}+ib_{n})$$$X_{0}$ se denomina *el valor medio* de la señal $x(t)$.	
- **$x(t)$ es una señal real:**
Entonces los coeficientes de la serie trigonométrica serán también reales y $X_{-n}=X_{n}^{*} \quad \forall n\in \mathbb{N}$ 
- **Si $x(t)$ es una señal par:**
Tendremos que $x(t)cos(n\omega_{0}t)$ es una *función par* y $x(t)sen(n\omega_{0}t)$ *impar*, por lo que:$$
	\begin{split}
	& a_{0}=\frac{2}{T}\int_{0}^{\frac{T}{2}}x(t)dt
	
	\\ & a_{n}=\frac{4}{T}\int_{0}^{\frac{T}{2}}x(t)cos(n\omega_{0}t)dt
	
	\\ & b_{n}=0
	\end{split}$$
De estos resultados obtenemos que:	$$X_{n}=X_{-n}=\frac{a_{n}}{2}\quad \forall n\in \mathbb{N}$$
- **Si $x(t)$ es una señal impar:**
Tendremos que $x(t)cos(n\omega_{0}t)$ es una *función impar* y $x(t)sen(n\omega_{0}t)$ *par*, por lo que:$$
	\begin{split}
	& a_{0}=0
	
	\\ & a_{n}= 0
	
	\\ & b_{n}= \frac{4}{T}\int_{0}^{\frac{T}{2}}x(t)sen(n\omega_{0}t)dt
	\end{split}$$
De estos resultados obtenemos que:	$$X_{n}=X_{-n}=-i\frac{b_{n}}{2}\quad \forall n\in \mathbb{N}$$
## Representación espectral de señales periódicas
Únicamente consideraremos *señales reales*. Sea pues $x(t)$ una señal real periódica de período $T$.
  #### Serie trigonométrica y representación espectral unilateral (Aplicación):
  ![[Pasted image 20230824005804.png|#center|500]]![[Pasted image 20230824005848.png|400]]
 #### Serie exponencial y representación bilateral (Aplicación):
 ![[Pasted image 20230824010018.png|400]]
### Extensión de la S.F
Sea $x(t)$ una señal definida en $[0,L]$ → Propiedades acorde al tipo de extensión:
- **Extensión periódica:** Asumimos que el período es $T=L$ y $\omega_{0}L=2\pi$, la extensión viene dada por $x(t+kL)=x(t) \ \forall t\in[0,L), \forall k \in \mathbb{Z}$, y los *coeficientes de Fourier* serán:
$$\begin{split}
& a_{0} = \frac{1}{L}\int_{0}^{L}x(t)dt \\
& a_{n} = \frac{2}{L}\int_{0}^{L}x(t)cos(\frac{n2\pi}{L}t)dt \\
& b_{n} = \frac{2}{L}\int_{0}^{L}x(t)sen(\frac{n2\pi}{L}t)dt
\end{split}$$
De este modo, la serie trigonométrica de Fourier será en este caso:
$$x(t)\sim a_{0}+\sum\limits_{n\geq 1}a_{n}cos(\frac{n2\pi}{L}t)+b_{n}sen(\frac{n2\pi}{L}t)$$
- **Extensión par:** Serie de cosenos. Asumimos que el período es $T=2L$ y $\omega_{0}L=\pi$, y la extensión viene dada por: $x(-t)=x(t) \ \forall t \in[0,L]$ y $x(t+2kL)=x(t) \ \forall t \in [-L,L], \forall k \in \mathbb{Z}$, y los *coeficientes de Fourier* serán:
$$\begin{split}
& a_{0} = \frac{1}{L}\int_{0}^{L}x(t)dt \\
& a_{n} = \frac{2}{L}\int_{0}^{L}x(t)cos(\frac{n\pi}{L}t)dt \\
& b_{n} = 0 \\
& x(t)\sim a_{0}+\sum\limits_{n\geq 1}a_{n}cos(\frac{n\pi}{L}t)
\end{split}$$
- **Extensión impar:** Serie de senos. Asumimos que el período es $T=2L$ y $\omega_{0}L=\pi$, y la extensión viene dada por: $x(-t)=-x(t) \ \forall t \in[0,L]$ , $x(t+2kL)=x(t) \ \forall t \in [-L,L], \forall k \in \mathbb{Z}$ y $x(kL)=0, \forall k\in\mathbb{Z}$ y los *coeficientes de Fourier* serán:
$$\begin{split}
& a_{0} = a_{n} = 0 \\
& b_{n} = \frac{2}{L}\int_{0}^{L}x(t)sen(\frac{n\pi}{L}t)dt \\
& x(t)\sim \sum\limits_{n\geq 1}b_{n}sen(\frac{n\pi}{L}t)
\end{split}$$
### Convergencia de las series de Fourier
##### Teorema de la convergencia puntual
Sea $x:[t_{0},t_{0}+T)\to K$ continua a trozos y en $\tau ~\exists~ x~'(\tau^{+})$ y $x'(\tau^{-})$, entonces si $x\sim\sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi n f_{0}t}$ → $\frac{x(\tau^{+})+x(\tau^{-})}{2}=\sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi n f_{0}t}$
##### Teorema de la convergencia uniforme
Sea $S(t)=\sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi n f_{0}t}$ y si $k\in\mathbb{N}_{0}$ → $S_{k}(t)= \sum\limits_{n=-k}^{k}X_{n}e^{i2\pi n f_{0}t}$
La serie **converge puntualmente** en $\tau^{*}$ si $lim_{k\to \infty}|S(\tau^{*})-S_{k}(\tau^{*})|=0$

Sea $x:[t_{0},t_{0}+T) \to K$ continua, $x(t_{0})=x(t_{0}+T)$ y $x'$ es continua a trozos en $[t_{0},t_{0}+T)$ → La serie de Fourier de $x$ converge *(a x)* **absoluta y continuamente** en $[t_{0},t_{0}+T)$.
Por lo que vale que:$$x(t)=\sum\limits_{n\in\mathbb{Z}}X_{n}e^{i2\pi n f_{0}t}$$
##### Teorema de la derivación
Sea $x:[t_{0},t_{0}+T) \to K$ continua tal que $x(t_{0})=x(t_{0}+T)$ y tal que $x'(t)$ es continua a trozos en $[t_{0},t_{0}+T)$ → Si $\exists ~ x''(\tau^{+})$ y $x''(\tau^{-})$, vale que:
$$\frac{x'(\tau^{+})+x'(\tau^{-})}{2}=\sum\limits_{n\in\mathbb{Z}-{\{0\}}}(i2\pi n f_{0})~X_{n}e^{i2\pi n f_{0}t}$$
# Transformada de Fourier
#### Famosas
1) $\prod\left(\frac{t}{\tau}\right)\leftrightarrow \tau~sinc(f~\tau)$, con $sinc(f)=\frac{sen(\pi f)}{\pi f}$
2) $\delta(t-t_{0}) \leftrightarrow e^{-i2\pi ft_{0}}$
3) $\bigwedge(\frac{t}{\tau}) \leftrightarrow \tau ~ sinc^{2}(f~\tau)$, con $\bigwedge(\frac{t}{\tau})= \begin{cases} 1 - \frac{|t|}{\tau} \quad |t|\leq\tau\\ 0 \quad en~otro~caso \end{cases}$
#### En tiempo continuo
Sea $x:\mathbb{R}\to K$ tal que $\mathcal{F}[x(t)](f)=X(f)=\hat{x} (f)= \int_{-\infty}^{\infty}x(t)e^{-i2\pi ft}dt$ cuando la integral existe.
##### Prop
Si $x \in \mathcal{L}^{1}$ → $X(f) \exists~ \forall~ f \in \mathbb{R}$ y $X:\mathbb{R} \to K$ es uniformemente continua.
#### En tiempo discreto
Sea $x:\mathbb{Z} \to K$, se define $\mathcal{F}_{d}[x(n)](f)=X(f)=\hat{x}(f)=\sum\limits_{n\in\mathbb{Z}} x(n)e^{-i2\pi f n}$, cuando la suma exista.
##### Convergencia
$x(n) \in l^{1} \leftrightarrow \sum\limits_{n\in\mathbb{Z}}|x(n)|<\infty$ → $X(f)~ \exists~ \forall ~ f\in\mathbb{R}$ y $X(f)$ es una función uniformemente continua.
##### Prop
Si $x\in \mathcal{C}^{1}, \mathcal{F}_{d}[x(n)](f)\  \exists \ \forall f \in \mathbb{R}$. Además, $\mathcal{F}_{d}[x(n)](f)$ es periódica de período 1 y uniformemente continua.
#### Propiedades
1) **Dualidad:** 
$\mathcal{F}[x](f)=X(f) \Longrightarrow \mathcal{F}[X](f)=x(-f)=x\circ e_{-1}$, donde $[e_{-1}(s)=-s]$
Además, si $x$ es *par*: $F[X]=x$
Para tiempo discreto se cumple que: $X_{k}=x(-k)$, el k-ésimo coeficiente de la serie exp. de Fourier de $X(f)$ es $x(-k)$.
2) **Linealidad:**
Vale tanto para tiempo continuo como para tiempo discreto.
3) **Desplazamiento en frecuencia:**
$\mathcal{F}[x(t)e^{i2\pi f_{0}t}](f)=X(f-f_{0})=X\circ d_{-f_{0}}(f) \quad (d_{b}(s)=s+b)$
$\mathcal{F}_{d}[x(n)e^{i2\pi f_{0}n}](f)=X(f-f_{0})$ 
4) **Desplazamiento en tiempo:**
$\mathcal{F}[x(t-t_{0})](f)=X(f)e^{-i2\pi f_{0}t_{0}}$ (Tiempo coninuo)
$\mathcal{F}_{d}[x(n-n_{0})](f)=X(f)e^{-i2\pi f_{0}n_{0}}$ (Tiempo discreto)
5) **Escalamiento en tiempo:**
$\mathcal{F}[x(at)](f)=\frac{1}{ |a| }X(\frac{f}{a})$ con $a\neq 0$ 
6) **Transformada de la derivada:**
$x:\mathbb{R}\to K \quad x^{(k)} \in \mathcal{L}^{1} \quad k=0,1,...,n$, y $\lim_{ |t|\to\infty} x^{(k)}(t)=0 \quad k =0, 1, ..., n-1$ → $\mathcal{F}[x^{(n)}(t)](f)=(i2\pi f)^{(n)}X(f)$
7) **Derivada de la transformada:**
En tiempo continuo: $t^{k}x(t)\in \mathcal{L}^{1} \quad k=0,1,...,n$, y $\mathcal{F}[x(t)](f)=X(f)$
$\Longrightarrow \mathcal{F} [(-i2\pi t)^{n}x(t)](f)=\frac{d^{n}}{df^{n}}X(f)$
Esto se debe, ya que: $\mathcal{F}[t^{k}\varphi (t)]=(\frac{-1}{i2\pi})^{k}\frac{d^{n}}{df^{n}}\mathcal{F}[\varphi (t)](f) \quad \forall k$
En tiempo discreto: $\mathcal{F}_{d} [(-i2\pi t)^{m}x(n)](f)=\frac{d^{m}}{df^{m}}X(f)$
8) **Transformada de la convolución:**
Si $x \leftrightarrow X,~ y \leftrightarrow Y \Longrightarrow \mathcal{F}[x*y(n)](f)=X(f).Y(f)$
9) **Transformada de la integral de una función:**
$x(t) \in \mathcal{L}^{1}, x \leftrightarrow X(f)$ → $\mathcal{F}[\int_{-\infty}^{t}x(s)ds](f)=X(f).U(f)=\frac{X(f)\delta (f)}{2} + \frac{X(f)}{i2\pi f}=\frac{X(0)\delta(f)}{2}+ \frac{X(f)}{i2\pi f}$
10) **Transformada de Fourier de distribuciones:**
Si $x \in \mathcal{D}$ *defino* $\mathcal{F}[x(t)](f) \in \mathcal{D}$ en la siguiente forma: Dada $\varphi \in C_{0}^{\infty}, <\mathcal{F}[x(t)](f), \varphi (f)> = <x(t),\hat{\varphi}(t)>$
Además, si $\varphi \in C_{0}^{\infty} \Rightarrow \hat{\varphi}\in C_{0}^{\infty}$
![[Pasted image 20230905193620.png]]
11) **Transformada de una funciones periódicas:**
- De series de distribuciones:
Sea ${x_{k}, k \in \mathbb{N}}$ una sucesión de funciones generalzadas y para cada $n \in  \mathbb{N}$, tenemos que $S_{n}=\sum\limits_{k=1}^{n}x_{k}$ → La función generalzada $x$, es la suma de la serie de las ${x_{k}}$ → $x=\sum\limits_{k\geq1} x_{k} \leftrightarrow x= \lim_{n\to\infty} S_{n}$.
Por lo que cada función de prueba $\phi$, si $\alpha_{k,\phi}=< x_{k},\phi > \to \exists$ la serie $\alpha_{\phi}=\sum\limits_{k\geq1} \alpha_{k,\phi}=<x,\phi>$
- Sea $x(t)$ una función cont. a trozos, periódica de período $T$, y tal que en toda discontinuidad de $x$ existan sus derivadas laterales. Además, $f_{0}=\frac{1}{T}$ y $X_{n}$ son sus coeficientes en serie exponencial, entonces obtenemos lo siguiente:
$$\mathcal{F}[x(t)](f)=\sum\limits_{n\in\mathbb{Z}}X_{n}\delta (f-nf_{0})$$
12) **Diferenciación en frecuencia:**
$\mathcal{F}[t^{k}x(t)](f)=(\frac{-1}{i2\pi})^{k} \frac{d^{k}X}{df^{k}}$
$\mathcal{F_{d}}[n^{k}x(n)](f)=(\frac{-1}{i2\pi})^{k} \frac{d^{k}X}{df^{k}}$
### Antitransformada de Fourier
#### En tiempo continuo
Sea $x:\mathbb{R}\to K, \quad x(t)\leftrightarrow X(f)$, la transformada inversa de Fourier de $X(f)$ es:$$\mathcal{F}^{-1}[X(f)](t)=\int_{-\infty}^{\infty} X(f) e^{i2\pi f t}df=x(t)$$Cuando la integral existe.
#### En tiempo discreto
Sea $x: \mathbb{Z} \to , x \in c^{1}$ y $x \leftrightarrow X, X$ es periódica y uniformemente continua.
$$\mathcal{F}_{d}^{-1}[X(f)](k)=\int_{<1>} X(f) e^{i2\pi f k}df = x(k)$$
#### Prop
1) Sean $x,y \in \mathcal{L^{2}}$ con T.F $X,Y$ → $X,Y \in \mathcal{L^{2}}$ y se cumple lo siguiente:
- $\int_{-\infty}^{\infty}x(t)y^{*}(t)dt=\int_{-\infty}^{\infty}X(f)Y^{*}(f)df$
- Si $x=y$, como $x(t)x^{*}(t)=|x(t)|^{2}$ → $\int_{-\infty}^{\infty}|x(t)|^{2}dt=\int_{-\infty}^{\infty}|X(f)|^{2}df=E_{x}$ (Fórmula de Parseval)
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

Sea $X_{T} \in \mathcal{L}^{2}$, de *potencia*, y $P=\lim_{T\to\infty} \frac{1}{2T}\int_{-\infty}^{\infty}|x_{T}(t)|^{2}dt$, por la *igualdad de Parseval* $|x_{T}(t)|^{2}=|X_{T}(f)|^{2}$, por lo tanto:
Sea $S(f)=\lim_{T\to\infty} \frac{1}{2T}|X_{T}(f)|^{2}$ la **densidad espectral de potencia** de $x$ → $P=\int_{-\infty}^{\infty}S(f)df$
# Transformada Z
##### Def
Tomando $z=e^{st}$, la transformada $\mathcal{Z}$ es una herramienta para el análisis de señales y sistemas en tiempo discreto. La notación será $\mathcal{Z}[x(n)](z)~ o ~X(z)$ 
##### Obs
La relación entre la transformada Z y la transformada de Fourier es mediante el cambio de variable: $Z=e^{i\omega t}$
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
1) **Inversión por división larga:** Se aplica a la inversión de la transformada $\mathcal{Z}$ de señales $x(n)$ causales. $X(z)$ debe ser un cociente de polinomios en $Z$, es decir:
$$X(z)= \frac{P(z)}{Q(z)}$$
Como $x(n)$ es causal → $gr(P(z)) \leq gr(Q(z))$, y el método consiste en hacer la división larga, es decir, en potencias de $z^{-1}$ de $P(z)$ por $Q(z)$.
2) **Inversión por series de Laurent:** Dado que una señal en tiempo discreto causal $x(n)$, su transformada de $\mathcal{Z}$ tiene solo potencias no positivas de $z$ → Su representación en series de potencias es una *serie de Laurent*, por lo que los coeficientes que acompañan a las potencias de $z^{-1}$ serán los correspondientes valores de $x(n)$. Por lo tanto, mediante este desarrollo para $X(z)$, podremos obtener $x(n)$.
3)  **Inversión por integrales de línea:** Sean $X(z)=\sum\limits_n\in\mathbb{N_{0}} x(n)z^{-n}$ y $\Gamma$ una curva cerrada simple que contiene al origen en su interior, y que a su vez está contenida en la región de convergencia de $X(z)$ y supongamos que $X(z)$ tiene una cantidad finita de singularidades en la región encerrada por $\Gamma$. Como en la región de convergencia de $X(z)$, la convergencia es uniforme, tendremos que para todo $k \in \mathbb{N_{0}}$, $\oint_{\Gamma}z^{k-1}X(z)dz = \begin{cases} & i2\pi \quad si \quad n=k \\ & 0 \qquad si \quad n\neq k \end{cases}$ , en consecuencia:$$x(k)= \frac{1}{2\pi i}\oint_{\Gamma}z^{k-1}X(z)dz=\sum\limits_{j=1}^{M}Res[z^{k-1}X(z), z_{j}]$$
Donde $z_{1},...,z_{M}$ son los puntos singulares de $z^{k-1}X(z)$ que están en la región encerrada por $\Gamma$.
4) **Inversión por descomposición en fracciones simples:** Este método es particularmente útil en el caso en que $X(z)$sea una fución racional en $z$. Consideramos $X_{1}(z)$ una función racional en $z$ que es la transformada $\mathcal{Z}$ de $x_{1}(n)$ señal en tiempo discreto causal → $X_{1}(z)=\frac{P_{1}(z)}{Q(z)}$ con $P_{1}(z)$ y $Q(z)$ polinomios y $gr(P_{1}(z))\leq gr(Q(z))$ → $\exists ~ A ~ cte$ y $P(z)$ un polinomio con $gr(P) < gr(Q)$ tales que:
$$X_{1}(z)=A+\frac{P(z)}{Q(z)}= A + X(z)$$
