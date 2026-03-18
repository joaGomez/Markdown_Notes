-----
Las señales son una función de la forma:
$$x: I \to K$$
Si el intervalo del dominio de la señal es en los reales ($\Re$) , es una señal en tiempo continuo. Por otro lado, si el dominio esta definido en los enteros ($Z$), es una señal en tiempo discreto.

## Tipos de señales
-----
-  Escalon unitario
$$u(t) =
\begin{cases} 
0 \quad t < 0
\\ 1 \quad t > 0 
\\ a \quad t = 0
\end{cases}$$
- Rampa unitaria
$$r(t) =
\begin{cases} 
0 \quad t \le 0
\\ t \quad t > 0 
\end{cases}$$
Donde $r(t) = \int_{-\infty}^{t}u(s) ds$. 
- Parabola unitaria
$$p(t) =
\begin{cases} 
0 \quad t \le 0
\\ \frac {t^2}{2} \quad t > 0 
\end{cases}$$
Donde $p(t) = \int_{-\infty}^{t}r(s) ds$. 
- Pulso unitario
$$\prod(t) =
\begin{cases} 
1 \quad |t| < \frac{1}{2}
\\ a \quad |t| = \frac{1}{2} \\
0 \quad |t| > \frac{1}{2}
\end{cases}$$
con $a \in [0,1]$  arbitrario y fijo.

![[Pasted image 20230802235520.png]]
- Señal triangular unitaria
$$\Lambda(t) =
\begin{cases} 
1 \ - \ |t| \quad |t| \leq 1
\\ 0 \ \ \ \quad \quad \quad |t| \geq 1 
\end{cases}$$
En particular:
$$\Lambda(\frac{t-t_{0}}{d}) =
\begin{cases} 
1 \ - \ |\frac{t-t_{0}}{d}| \quad |t-t_{0}| \leq d
\\ 0 \ \ \ \quad \ \ \quad \quad \quad |t-t_{0}| \geq d 
\end{cases}$$
Hasta aquí constituyen las funciones de singularidad, ya que en algun punto de su dominio no son derivables.

Se nota con $t$ las señales con tiempo continuo, y con $n$ las señales en tiempo discreto.

- Senoides
$$x(t) = A\cos(2\pi f_{0}t+\theta)$$
Siendo $A$ la amplitud de la señal, $f_0$ la frecuencia y $\theta$ la fase, donde $\theta \in [-\pi,\pi]$ .
## Funciones periódicas
----
Sea $x:R \to K$, es una funcion periodica si $\exists \ \tau > 0 \ /$ $x(t+\tau) = x(t) \ \forall\  t \in R$  $\to$ $\tau$ es período de $x(t)$. Ademas, para cualquier $n \in N$ fijo: $x(t) = x(t+n\tau) \ \forall\  t \in R$.

$T_0$ será el período fundamental de $x(t)$ / $T_{0}= inf\{ \tau > 0 \ / \ x(t+\tau) = x(t)\}$. Tiempo continuo.

$N_0$ será el período fundamental de $x(n)$ / $N_{0}= inf\{ N > 0 \ / \ x(n+N) = x(t)\}$. Tiempo discreto.
#### Prop.
Si consideramos un senoide de forma: $x(t) = A\cos(2\pi f_{0}t+\theta)$ $\to$ para cada $n \in N$, $\tau_{n} = \frac{n}{f_0}$, y $T_{0} = \frac{1}{f_0}$ es su período fundamental.
#### Prop.
Si $x(t) = a = cte$ $\to$ La función es periódica pero no tiene período fundamental.
##### Preposición 1
La periodicidad de una función es tal que $\tau = n \ T_{0}, con \ n \in N$.
### Combinación lineal de señales periódicas
##### Preposición 2
Sean $a_{1}\ y \ a_{2}$ no nulos, $x_{1} (t) \ y \  x_{2}(t)$ periódicas de períodos $T_{1} \ y \ T_{2}$ $\to$  $z(t) = a_{1}x_{1}(t) + a_{2}x_{2}(t)$ es periódica $\leftrightarrow$ $\frac{T_1}{T_{2}}= q$, con $q$ un numero racional.

- Si $\frac{T_{1}}{T_{2}} = \frac{p}{q}$, con $p,q \in N$ coprimos, $T_{0} = q T_{1} = p T_{2}$.
- Sean $a_{i}, i = 1, ... ,m$ no nulos y $x_{i}(t), i = 1, ... , m$ periódicas de períodos $T_{i}$. $\to$ $z(t) = \sum\limits_{i=1}^{m}a_{i}x_{i}(t)$ es periódica de período $T_{0} \leftrightarrow \frac{T_{1}}{T_{i}} = \frac{p_{i}}{q_{i}}$, $i = 2, ... , m$, con $p_{i},q_{i} \in N$ coprimos $(2 \leq i \leq m) \to T_{0} = (mcm \{ q_{2},...,q_{m}\})T_{1}$
- Sean $a_{i}, i = 1, ... ,m$ no nulos y $x_{i}(n), i = 1, ... , m$ periódicas de períodos $N_{i}$. $\to$ $z(n) = \sum\limits_{i=1}^{m}a_{i}x_{i}(n)$ es periódica de período $N_{0} = mcm \{ N_{1},...,N_{m}\}$
## Señales como vectores
----
Sea $\nu: \{ x: I \to K\}$ se cumple que:
- $\forall x,y \in \nu, (x+y)(\mu) = x(\mu) + y(\mu)$, con $\mu \in I$
- $\forall a \in K, \forall x \in \nu, (a.x)(\mu) = a.x(\mu)$, con $\mu \in I$

## Desplazamiento en tiempo
---
Sea $\alpha \in I$, $d_{\alpha}:I \to I$, $d_{\alpha} (\mu) = \mu + \alpha$, $\mu \in I$, es el desplazamiento en tiempo. Y $d_{\alpha}^{-1} : I \to I$, $d_{\alpha}^{-1} = d_{- \alpha}$.

![[Pasted image 20230802153646.png]]

## Escalonamiento en tiempo
---
Sea $\beta \in I$, $\beta \neq 0, e_{\beta} : I \to I$, $e_{\beta} (\mu) = \beta \mu$, $\mu \in I$, es el escalonamiento en tiempo. Solo para el caso donde $I = R$, está definida $e_{\beta}^{-1} : R \to R, e_{\beta}^{-1} = e_{\frac{1}{\beta}}$

![[Pasted image 20230802154811.png|600]]
![[Pasted image 20230802154841.png|600]]
## Representacion espectral de señales
---
Sea $x(t) = A \ cos(2\pi f_{0}t+\theta) = A \ cos(\omega_{0}t+\theta), \omega_{0}=2\pi f_{0}$, $-\pi < \theta \leq \pi, A > 0$ 
$\to x(t) = Re(A \ e^{i(\omega_{0}t+\theta)})= Re(A\ e^{i\theta} e^{i\omega_{0}t}) = Re(\vec{X} e^{i\omega_{0}t}) = Re(\tilde{x} (t))$, donde $\vec{X}$ es un fasor, y $\tilde{x}(t)$ es un fasor rotatorio.
![[Pasted image 20230802163606.png]]

Se llama diagrama unilateral cuando la amplitud, la fase y la frecuencia son fijos para todos los valores en $I$ / $x(t) \to \{A, \theta, f_{0}\}$. Y si tengo una señal de la forma: $x(t)=\sum\limits_{i=1}^{n} A_{i}\ cos(2\pi f_{i}\ t+\theta_{i})$ → $x \leftrightarrow \{ \{A_{1}, \theta_{1}, f_{1}\},...,\{A_{n}, \theta_{n}, f_{n}\}\}$. 
![[Pasted image 20230805112207.png]] ![[Pasted image 20230805112220.png]]

Sabemos que $x(t)=\frac{\tilde{x}(t)+\bar{\tilde{x}}(t)}{2}$, ya que $cos(t)=Re(e{^{it}})=\frac{1}{2}\ Re(e{^{it}}+e{^{-it}})$ 

 ![[Pasted image 20230805112053.png#center|300]]
Por otro lado, los diagramas bilaterales tienen en cuenta la expresión de la señal como la semisuma de su fasor rotatorio y su conjugado. Por lo tanto, $x \leftrightarrow \{ \{\frac{A}{2},\theta,f_{0}\}, \{\frac{A}{2},-\theta,-f_{0}\}\}$. Si tengo una señal de la forma: $x(t)=\sum\limits_{i=1}^{n} A_{i}\ cos(2\pi f_{i}\ t+\theta_{i})$ → $x \leftrightarrow \{ \{\frac{A_{1}}{2}, \theta_{1}, f_{1}\},\{\frac{A_{1}}{2}, -\theta_{1},-f_{1}\},...,\{\frac{A_{n}}{2}, \theta_{n}, f_{n}\}, \{\frac{A_{n}}{2},-\theta_{n},-f_{n}\}\}$. 

  ![[Pasted image 20230805112839.png]] ![[Pasted image 20230805112857.png]]

En la representación bilateral, el espectro de la amplitud es **PAR**, y el espectro de fase es **IMPAR**.

  ![[Pasted image 20230807164635.png|400]]   ![[Pasted image 20230807165146.png|400]] 

## Energía y potencia
---
#### Def
Sea $x$ una señal en tiempo continuo, $x$ es de **energía** si: $0 < \lim_{t\to +\infty}\int_{-T}^{T}|x(t)|{^{2}}dt < \infty \Longrightarrow 0 < Ex=V.P.\int_{-\infty}^{\infty}|x(t)|^{2}dt < \infty$
- Ej: [[Ejemplos, señal de energía]]
#### Def
Sea $x$ una señal de tiempo continuo, $x$ es de **potenica** si: $0 < lim_{T\to \infty} \frac{1}{2T}\int_{-T}^{T}|x(t)|^{2}dt < \infty \Longrightarrow 0 < P_{x}=lim_{T\to \infty} \frac{1}{2T}\int_{-T}^{T}|x(t)|^{2}dt < \infty$
- Ej: [[Ejemplos, señal de potencia]]
##### Prop
Una señal **NO** puede ser de potencia y de energía al mismo tiempo
   ![[Pasted image 20230814164207.png|700]]
##### Prop
Por la identidad de Parseval, la potencia de la suma es la suma de las potencias. Siempre y cuando, que sea una combinacion lineal de funciones ortogonales.
   ![[Pasted image 20230814174740.png|600]]
## Transformación lineal
---
Sea $B=\{ \bar{v}_{1},...,\bar{v}_{n}\}$ una base ortonormal de $V$ → $$<\bar{v}_{i},\bar{v}_{j}> = 
\begin{cases} 
1 \quad i=j
\\ 0 \quad i \neq j  
\end{cases}$$ Consideramos un vector $\omega \in V$ fijo. Para cada $v \in V$ le asigno $<\omega, v>= L_{\omega}(v)$, con: $L_{\omega}:V\to K$. 
Además, $L_{\omega}(\alpha v_{1}+\beta v_{2}) =\  <\omega,\alpha v_{1}+\beta v_{2}> = \alpha \ <\omega,v_{1}>+\beta <\omega,v_{2}>=\alpha L_{\omega}(v_{1})+\beta L_{\omega}(v_2)$ → $L_{\omega}$ es una T.L

##### Prop.
$\omega$ se puede ontener a partir de los valores que toma $L_\omega$ en la base $B$:
$\omega = \alpha_{1}\bar{v}_{1}+\alpha_{2}\bar{v}_{2}+...+\alpha_{n}\bar{v}_{n}$ → $L_{\omega}(\bar{v}_{j})=<\alpha_{1}\bar{v}_{1}+...+\alpha_{j}\bar{v}_{j}+...+\alpha_{n}\bar{v}_{n},\bar{v}_{j}>=\alpha_{j}<\bar{v}_{j},\bar{v}_{j}>=\alpha_{j}$

Sea $x:R \to K$, la generalización de $x$ debe basarse en que no importan los valores individuales de $x$ sino su comportamiento global.
Supongo que $x$ es continua a trozos. Considero el conjunto de las funciones de prueba:
$C_{0}^{\infty}=\{\varphi:\Re \to K, C^{\infty}$ y que se anula fuera de $[-M_{\varphi},M_{\varphi}]\}$ 
#### Def.
$$<x, \varphi>=\int_{-\infty}^{\infty}x(t)\varphi(t)dt \quad \quad \varphi \in C_{0}^{\infty}$$
##### Prop.
Sea $\alpha_{1}, \alpha_{2} \in K, \varphi_{1},\varphi_{2} \in C_{0}^{\infty}$ → $<x,\alpha_{1}\varphi_{1}+\alpha_{2}\varphi_{2}>=\alpha_{1}<x,\varphi_{1}>+\alpha_{2}<x,\varphi_{2}>=\int_{-\infty}^{\infty}x(t)[\alpha_{1}\varphi_{1}(t)+\alpha_{2}\varphi_{2}(t)]dt$
#### Def.
$<x,\bullet>:C_{0}^{\infty}\to K$ es una **Transformación Lineal**
  ###### Obs
  Como $C_{0}^{\infty}$ es un espacio de funciones → $<x,\bullet>$ es una función lineal
  ##### Notación
  Sea $L_{x}:C_{0}^{\infty}\to K$ tal que $L_{x}(\varphi)=\int_{-\infty}^{\infty}x(t)\varphi(t)dt$ → $L_{x}$ es una **Transformación Lineal**
## Funciones Generalizadas
----
#### Def
Una distribución (función generalizada) es una función lineal (continua) sobre $C_{0}^{\infty}$ / $D=\{distribución \ sobre \ C_{0}^{\infty}\}$
#### Def.
$G\in D$ es una distribución regular si $\exists \ y:\ R \to K$ continua a trozos tal que $<G,\varphi> = \int_{-\infty}^{+\infty}y(t)\varphi(t)dt \quad \forall \varphi \in C_{0}^{\infty}$
###### Obs.
$\exists$ distribuciones no regulares, como $\delta(t)$, conocida como, la **Delta de Dirac**: $<\delta, \varphi>=\varphi(0), \forall \varphi \in C_{0}^{\infty}$
   
   ![[Pasted image 20230808095638.png|700]]
#### Def
$$\int_{-\infty}^{\infty}f(t)\delta (t-t_{0})dt = f(t_{0})$$
  ##### Prop
$$\int_{a}^{b}f(t)\delta (t-t_{0})dt = 
\begin{cases} 
f(t_{0}) \quad t_{0}\in [a,b]\\
0 \quad \ \ \ \quad t_{0}\notin [a,b] \\
Indefinido \quad t_{0}=a \lor t_{0}=b
\end{cases}$$
### Igualdad en distribuciones
---
Si $\eta,\mu \in D$, digo que $\eta = \mu \leftrightarrow <\eta,\varphi>=<\mu, \varphi>, \forall \varphi \in C_{0}^{\infty}$
  ![[Pasted image 20230808100234.png|800]]
### Propiedades y definiciones en D
---
- $D$ es un espacio vectorial **+** y **.** (por escalares) $\alpha, \beta \in K; \eta, \mu \in D$, defino $\alpha . \eta + \beta . \mu$ 
$$<\alpha . \eta + \beta . \mu,\varphi>=\alpha<\eta,\varphi>+\beta<\mu,\varphi>, \forall \varphi \in C_{0}^{\infty}$$
- Producto de una distribución por una función $C_{0}^{\infty}$ 
$\eta \in D, g \in C_{0}^{\infty}$, si quiero saber cuanto da $g.\eta$ → 
   
   ![[Pasted image 20230808101739.png|700]]
###### Ejemplo
  ![[Pasted image 20230808101950.png|700]]
###### Obs
No se puede definir en general el producto de distribuciones
### Derivadas generalizadas de distribuciones
----
Sea $\eta \in D$, su derivada $\eta \ '$ está dada por: $<\eta \ ', \varphi>=-<\eta, \varphi \ '>, \forall  \varphi \in C_{0}^{\infty}$
- Su derivada de orden $n \in N$ está dada por:  $<\eta^{(n)}, \varphi>=(-1)^{n} <\eta, \varphi^{(n)}>, \forall  \varphi \in C_{0}^{\infty}$
###### Obs
Si $\varphi \in C_{0}^{\infty} \to \varphi^{(k)} \in C_{0}^{\infty}, \forall k \in N$
##### Ejemplos de derivadas generalizadas de funciones
- [[Ejemplos de derivadas generalizadas de funciones]] 

### Composición de funciones generalizadas con funciones
---
$\eta \in D, g:\Re \to \Re (g \in C_{0}^{\infty})$ estrictamente monótona $(g'(t)\neq 0 \forall t)$. Sea $x$ continua a trozos y sea $\varphi \in C_{0}^{\infty}$
$$<x \ \circ \ g, \varphi> = \int_{-\infty}^{\infty}(x \ \circ \ g)(t)\varphi(t)dt=\int_{-\infty}^{\infty}(\frac{x(\tau)}{|g'(g^{-1}(\tau)|})\varphi(g^{-1}(\tau))d\tau=<x,\frac{1}{|g'(g^{-1}(\tau)|}(\varphi \ \circ \ g^{-1}(.))>$$
###### Ejemplo
   
   ![[Pasted image 20230808111701.png|800]]

Generalización
   
   
   ![[Pasted image 20230808112259.png|600]]
   

### Problema de la división
---
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
   ![[Pasted image 20230809141225.png|800]]
   ![[Pasted image 20230809141356.png|800]]
### Ecuaciones con funciones generalizadas
----
##### Prop
$$\begin{cases}
g(t)\delta(t-t_{0}) = g(t_{o})\delta(t-t_{0})\\
g(t)\delta'(t-t_{0})=g(t_{0})\delta'(t-t_{0})-g'(t_{0})\delta(t-t_{0}) \\
g(t)\delta''(t-t_{0})=g(t_{0})\delta''(t-t_{0})-2g'(t_{0})\delta'(t-t_{0})+g''(t_{0})\delta(t-t_{0})
\end{cases}$$
Generalizando:
$$g(t)\delta^{(n)}(t-t_{0})=\sum\limits_{j=0}^{n} (-1)^{n-j}\binom{n}{j}g^{(n-j)}(t_{0})\delta^{(j)}(t-t_{0})$$
#### Def
Sean $\eta \in D, n\in N$ y si $n^{(*)}$ 
Se dice que $\lim_{n\to \infty}$ 


### Importante
$y \in D$ se aplica a $\varphi \in C_{0}^{\infty}$. En el caso de la $\delta (t-t_{0})$ basta que $\varphi$ sea comtinua en **$t_{0}$**.

## Convolución lineal
----
#### Def
Dadas dos señales en tiempo discreto, $x(n),\ y(n)$, su **convolución lineal ($x*y$)** es la siguiente señal en tiempo discreto:
$$x*y(n)=\sum\limits_{k\in Z}x(k)y(n-k), \quad n\in Z$$
cuando la suma de la serie exista.
### Propiedades
1) **Asociatividad**
   ![[Pasted image 20230815115922.png|650]]
2) **Conmutatividad**
   ![[Pasted image 20230815120006.png|650]]
3) **Distributividad**
   ![[Pasted image 20230815120045.png|650]]
## Convolución periódica
---
Dadas dos señales en tiempo discreto $x(n),\ y(n)$ periódicas de período $N$, su **convolución periódica ($x\circledast y$)** es la siguiente señal en tiempo discreto:
$$x \circledast y (n) = \sum\limits_{k=0}^{N-1}x(k)y(n-k), \quad n\in Z$$
### Propiedades
1) **Periodicidad**
   ![[Pasted image 20230815120823.png|650]]
2) **Invariancia respecto del intervalo de sumación**
   ![[Pasted image 20230815120948.png|650]]
  ###### Obs
  Deducimos que para cualquier par de señales $x(n), y(n)$, periódicas de período $N$ y $\forall \ n_{0}\in Z$ se verifica:
   ![[Pasted image 20230815121223.png|300]]
  3) **Asociatividad** 
   ![[Pasted image 20230815121504.png|300]]
   4) **Conmutatividad**
   ![[Pasted image 20230815121629.png|650]]
   5) **Distributivudad**
   ![[Pasted image 20230815121854.png|650]]
   