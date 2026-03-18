----
#### Def
Toda combiación lineal de señales periódicas $x(t)=\sum\limits_{n=1}^{N}a_{n}x_{n}(t)$ donde cada señal $x_{n}(t)$ tiene período fundamental $T_{n}$ resulta periódica $\leftrightarrow \frac{T_{n}}{T_{m}}$ es un número racional $1\leq n, m\leq N$. En particular, $x(t)$ será periódica si $T_{n}=\frac{T_{0}}{n}$ para $T_{0}>0$ fijo, y $T_{0}$ será su período fundamental.
## Series generalizadas de Fourier
---
Sea $V$ un $K-espacio \ vectorial$ con producto interno y $\phi=\{\phi_{k}, k\in N\}$ un conjunto ortogonal y $0 \notin \phi$ 

$$w=P_{s}(v)=\sum\limits_{k=1}^{n}c_{k}\phi_{k}$$
tal que $c_{j}=\frac{<w,\phi_{j}>}{<\phi_{j},\phi_{j}>}=\frac{<w,\phi_{j}>}{||\phi_{j}||^2}$ con $1\leq j \leq n$.
Además $c_{j}$ es el *j-ésimo coeficiente generalizado de Fourier de $v$ en el sistema* $\phi$
$$P_{s_{n}}(v)=\sum\limits_{k=1}^{n} \frac{<v,\phi_{k}>}{<\phi_{k},\phi_{k}>}\phi_{k}$$
##### Def
Dados un $K$ un espacio vectorial $V$ con producto interno, un subespaciio $S$ de $V$ y un vector $v\in V$, la proyección ortogonal de $v$ sobre $S$ es el únco vector $P_{s}(v)$, de $S$ tal que $<v-P_{s}(v),s> = 0 ~\forall s \in S$
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
## Series exponenciales de Fourier
---
Sea $N \in \mathbb{N}$ un número fijo. Considero $I_{N}=\{0,...,N-1\}$ tal que $V:\{x:I_{N}\to \mathbb{C}\}$ es un espacio vectorial de dimensión finita (N), ya que es isomorofo a $\mathbb{c}^{N}$, conjunto de las N-uplas de números complejos, mediante la asignación: $x \longrightarrow (x(0),...,x(N-1))$.
 ##### Prop
 Sean $x,y \in V$, se define el producto interno tal que: $$<x,y> = \sum\limits_{n=0}^{N-1}x(n)y^{*}(n)$$Sea $f_{0} = \frac{1}{N}$ y consideremos el siguiente conjunto de vectores de $V:\phi = \{ \phi_{1},...,\phi_{N} \}$ definidos según:$$\phi_{k}(n)=e^{i2\pi f_{0}kn}$$
 Por lo tanto dado que $V$ es de dmensión finita → $w$ ya no será una proyeccón ortogonal de $x$, sino que será la representación *exacta* de $x$ en los términos de la base $\Phi$, es decir, que podemos escribir
$$x(n)=\sum\limits_{k=0}^{N-1}c_{k}e^{i2\pi f_{0}kn}, \qquad \forall\ n \in \mathbb{Z}$$
*Determina la representación en series de Fourier de x, señal de tiempo discreto periódica de período N.*
###### Obs
Si hacemos la representación espectral de $x(n)$, el espectro se repertirá a intervalos de $Nf_{0}$
###### Ejemplos
![[Pasted image 20230822125820.png|500]]
### Propiedades del desarrollo en serie de Fourier en tiempo discreto
---
Considero dos señales en tiempo discreto $x_{1}(n), x_{2}(n)$ periódicas de período $N$ con coeficientes de Fourier $\{ c_{k}\}$ y $\{ d_{k}\}$
1. **Desplazamiento en tiempo:**
	Sean $n_{0} \in \mathbb{Z}, y(n)=x_{1}(n-n_{0}), n \in \mathbb{Z}$ y $\{ h_{k} \}$ los coeficientes de Fourier de $y(n)$ 
	→ $h_{k}=e^{-i2\pi f_{0}kn_{0}}c_{k}$
2. **Convolución periódica:**
	Sean $\{ h_{k} \}$ los coeficientes de Fourier de $x_{1} \circledast x_{2}(n)$ → $h_{k} = N c_{k} d_{k}$
## Series exponencial y trigonométrica de Fourier en tiempo continuo
---
Consideremos $t_{0}\in \mathbb{R}$ y $T>0$ fijos y el conjunto de funciones: $$\mathcal{L}_{t_{0},T}^{2}= \{ x:[t_{0}, t_{0}+T]\to K:\int_{t_{0}}^{t_{0}+T}|x(t)|^2~dt<\infty \}$$ donde $\mathcal{L}_{t_{0},T}^{2}$ es un K-espacio vectorial con las operaciones:
- $(x_{1}+x_{2})(t)\triangleq x_{1}(t)+x_{2}(t)$
- $(\alpha x_{1})(t) \triangleq \alpha x_{1}(t)$
$\forall t \in [t_{0},t_{0}+T]$, todo $\alpha \in K$ y $x_{1}, x_{2} \in \mathcal{L}_{(t_{0}, T)}^{2}$ cualesquiera.
#### Función nula
La función nula no es la función que vale 0 en todo su dominio, sino quees el *conjunto de todas las funciones* $\mu \in \mathcal{L}_{(t_{0}, T)}^{2}$ que 
verifican:
$$\int_{t_{0}}^{t_{0}+T}|\mu(t)|^{2}dt=0$$
#### Prop
Con el resultado anterior, podemos definir de otra forma la igualdad entre dos funciones, tal que, si $\exists\ x_{1},x_{2} \in \mathcal{L}_{(t_{0}, T)}^{2}$
entonces:
$$x_{1}=x_{2}\Leftrightarrow \int_{t_{0}}^{t_{0}+T}|x_{1}(t)-x_{2}(t)|^{2}dt=0$$

> Por otra parte, se puede comprobar que < , >: $\mathcal{L}_{(t_{0}, T)}^{2} \times \mathcal{L}_{(t_{0}, T)}^{2} \to K$ definido por:    
> $<x_{1},x_{2}>\triangleq \int_{t_{0}}^{t_{0}+T}x_{1}(t)x_{2}^{*}(t)$ 
es un producto interno en $\mathcal{L}_{(t_{0}, T)}^{2}$

> Se utiliza la notación $f_{0}=\frac{1}{T},w_{0}=2\pi f_{0}=\frac{2\pi}{T}$

### Teorema 1
El conjuntp $\{ e^{in\omega_{0}t},n\in \mathbb{Z} \}$ es ortogonal y completo en $\mathcal{L}_{(t_{0},T)}^{2}$
con el producto interno definido anteriormente.
###### Obs
Es inmediato comprobar que:
$$<e^{in\omega_{0}t},e^{in\omega_{0}t}> = \int_{t_{0}}^{t_{0}+T} e^{in\omega_{0}t}e^{-in\omega_{0}t} dt = \begin{cases}
0 \qquad n\neq m\\
T \qquad n = m \\
\end{cases}$$
Los **coeficientes de la serie exponencial de Fourier** de $x \in \mathcal{L}_{(t_{0},T)}^{2}$ vienen dados por:
$$X_{k}= \frac{<x,e^{ik\omega_{0}t}>}{<e^{ik\omega_{0}t},e^{ik\omega_{0}t}>}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T} x(t)e^{-ik\omega_{0}t} dt \qquad \forall k \in \mathbb{Z}$$
Tal que la *serie exponencial de Fourier* asociada a $x$ es:
$$x \sim \sum\limits_{k\in \mathbb{Z}}X_{k}e^{ik\omega_{0}t}$$
La **igualdad de Parseval** será en este caso:
$$\sum\limits_{k\in \mathbb{Z}} |X_{k}|^{2}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T}|x(t)|^{2} dt$$
### Teorema 2
Este teorema nos permite obtener los coeficientes de la serie trigonométrica de Fourier de una señal $x \in \mathcal{L}_{(t_{0},T)}^{2}$
El conjunto $\{ 1, cos(n\omega_{0}t), sen(m\omega_{0}t), n, m \in \mathbb{N} \}$ es ortogonal y completo en $\mathcal{L}_{(t_{0},T)}^{2}$
con producto interno definido.
> Los coeficientes de la **serie trigonométrica de Fourier** de $x \in \mathcal{L}_{(t_{0},T)}^{2}$, vienen dadas por:
> $a_{0}=\frac{1}{T}\int_{t_{0}}^{t_{0}+T}x(t)dt$
> $a_{n}= \frac{2}{T}\int_{t_{0}}^{t_{0}+T}x(t)cos(n\omega_{0}t)dt \qquad n\in \mathbb{N}$
> $b_{n}=\frac{2}{T}\int_{t_{0}}^{t_{0}+T}x(t)sen(n\omega_{0}t)dt \qquad n\in \mathbb{N}$

La serie **trigonométrica de Fourier** asociada con $x$ es:
$$x(t)\sim a_{0}+\sum\limits_{n\in\mathbb{N}}a_{n}cos(n\omega_{0}t)+b_{n}sen(n\omega_{0}t)$$
La **igualdad de Parseval** está dada por:
$$\frac{2}{T}\int_{t_{0}}^{t_{0}+T}|x(t)|^{2}dt=2|a_{0}|^{2}+\sum\limits_{n\in\mathbb{N}}|a_{n}|^{2}+|b_{n}|^{2}$$
#### Obs
Supongamos que la serie exponencial converge a $x(t)$ en el intervalo $[t_{0}, t_{0}+T]$:
$$x(\tau)=\sum\limits_{k\in \mathbb{Z}}X_{k}e^{ik\omega_{0}\tau} = \sum\limits_{k\in \mathbb{Z}}X_{k}e^{ik\omega_{0}(\tau+nT)}\qquad \forall \tau \in [t_{0},t_{0}+T], n\in \mathbb{Z}$$

> Deducimos que la suma de la serie representa a la *extensión periódica de período T* de $x(t)$. Por lo tanto si ahora $x(t)$ es una función periódica de período $T$ e $y = x|_{[t0,t0+]}$ es la restricción de $x$ al intervalo $[t_{0}, t_{0} +T]$ para algún $t_{0}$ arbitrario, y la serie exponencial de Fourier asociada a $y$ aproxima a esta última, también lo hará con $x(t)$, para valores de $t$ que no están en el intervalo $[t_{0}, t_{0} + T]$. En particular, si la serie converge a $y(\tau)$ para algún $\tau \in [t_{0}, t_{0}+ T]$ fijo, también convergerá a $x(\tau_{n})$ para $\tau_{n} = \tau + nT, n \in \mathbb{Z}$.

##### Prop
Teniendo en cuenta esta última superposición, y dado que $e^{in\omega_{0}t}, cos(n\omega_{0}t)$ y $sen(n\omega_{0}t)$ son también funciones periódicas de período $T$, obtenemos la siguiente propiedad:
$$\int_{t_{0}}^{t_{0}+T}x(t)dt=\int_{0}^{T}x(t)dt=\int_{-\frac{T}{2}}^{\frac{T}{2}}x(t)dt$$
#### Propiedades de las series de Fourier
1) **Coeficientes de las series exponenciales y desplazamiento en $\tau$:** 
	Sea $x(t)$ periódica de período $T$ y supongamos que $\{ X_{n}, n \in \mathbb{Z} \}$ son sus coeficientes de la serie exponencial y sea $y(t)=x(t+\tau)$ $$Y_{n}=X_{n}e^{in\omega_{0}\tau}$$
	Si tengo que $z(t)=x(t)e^{-i2\pi f_{0}kt}$, entonces la relación de sus coeficientes será:$$Z_{n}=x_{n-k}$$
1) **Coeficientes de la serie exponencial y trigonométrica:**
	Sea $x(t)$ periódica de período $T$ y supongamos que $\{ X_{n}, n\in \mathbb{Z} \}$ y $\{ a_{0},a_{n}, b_{m}, n, m\in\mathbb{N} \}$ son sus coeficientes de la serie exponencial y la trigonométrica.$$X_{0}= a_{0}\qquad X_{n}= \frac{1}{2}(a_{n}-ib_{n}) \qquad X_{-n}=\frac{1}{2}(a_{n}+ib_{n})$$	$X_{0}$ se denomina *el valor medio* de la señal $x(t)$.	

3) **$x(t)$ es una señal real:**
		Entonces los coeficientes de la serie trigonométrica serán también reales y $X_{-n}=X_{n}^{*} \quad \forall n\in \mathbb{N}$ 
1) **Si $x(t)$ es una señal par:**
	Tendremos que $x(t)cos(n\omega_{0}t)$ es una *función par* y $x(t)sen(n\omega_{0}t)$ *impar*, por lo que:$$
	\begin{split}
	& a_{0}=\frac{2}{T}\int_{0}^{\frac{T}{2}}x(t)dt
	
	\\ & a_{n}=\frac{4}{T}\int_{0}^{\frac{T}{2}}x(t)cos(n\omega_{0}t)dt
	
	\\ & b_{n}=0
	\end{split}$$
	De estos resultados obtenemos que:	$$X_{n}=X_{-n}=\frac{a_{n}}{2}\quad \forall n\in \mathbb{N}$$
5) **Si $x(t)$ es una señal impar:**
	Tendremos que $x(t)cos(n\omega_{0}t)$ es una *función impar* y $x(t)sen(n\omega_{0}t)$ *par*, por lo que:$$
	\begin{split}
	& a_{0}=0
	
	\\ & a_{n}= 0
	
	\\ & b_{n}= \frac{4}{T}\int_{0}^{\frac{T}{2}}x(t)sen(n\omega_{0}t)dt
	\end{split}$$
	De estos resultados obtenemos que:	$$X_{n}=X_{-n}=-i\frac{b_{n}}{2}\quad \forall n\in \mathbb{N}$$
## Representación espectral de señales periódicas
---
Únicamente consideraremos *señales reales*. Sea pues $x(t)$ una señal real periódica de período $T$.
  #### Serie trigonométrica y representación espectral unilateral (Aplicación):
  ![[Pasted image 20230824005804.png|500]]![[Pasted image 20230824005848.png|500]]
 #### Serie exponencial y representación bilateral (Aplicación):
 $$x(t)\sim \sum\limits_{k\in\mathbb{Z}}X_{k}e^{ik\omega_{0}t}$$
 ![[Pasted image 20230824010018.png|500]]
## Desarrollo en series de senos y cosenos
----
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
& b_{n} = 0
\end{split}$$
De este modo, la serie trigonométrica de Fourier será en este caso:
$$x(t)\sim a_{0}+\sum\limits_{n\geq 1}a_{n}cos(\frac{n\pi}{L}t)$$
- **Extensión impar:** Serie de senos. Asumimos que el período es $T=2L$ y $\omega_{0}L=\pi$, y la extensión viene dada por: $x(-t)=-x(t) \ \forall t \in[0,L]$ , $x(t+2kL)=x(t) \ \forall t \in [-L,L], \forall k \in \mathbb{Z}$ y $x(kL)=0, \forall k\in\mathbb{Z}$ y los *coeficientes de Fourier* serán:
$$\begin{split}
& a_{0} = a_{n} = 0 \\
& b_{n} = \frac{2}{L}\int_{0}^{L}x(t)sen(\frac{n\pi}{L}t)dt
\end{split}$$
De este modo, la serie trigonométrica de Fourier será en este caso:
$$x(t)\sim \sum\limits_{n\geq 1}b_{n}sen(\frac{n\pi}{L}t)$$
## Convergencia de las series de Fourier
---
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
