**Obs:** La transformada Z para los sistemas de tiempo discreto tiene el mismo objetivo que la transformada de Laplace para los sistemas de tiempo continuo.

Supongamos que queremos encontrar la transformada de Laplace para una señal discreta. Para obtener una señal discreta a partir de una señal continua en $t$, debemos muestrear la señal continua $x(t)$ con un tren de impulsos ideales.

La señal muestreada tiene la forma:
$$x^{*}(t)=\sum_{n=-\infty}^{\infty}x(t)\delta(t-nT)$$
Al aplicar la transformada de Laplace a $x^{*}(t)$:
$$\mathcal{L}\{ x^{*}(t) \} = \mathcal{L}\left\{  \sum_{n=-\infty}^{\infty} x(t)\delta(t-nT) \right\} = \mathcal{L}\left\{  \sum_{n=-\infty}^{\infty} x(nT)\delta(t-nT) \right\} = \sum_{n=0}^{\infty} x(nT)e^{-nTs}$$
Vemos que $x^{*}(s)$ contiene al factor $e^{-nTs}$. Como consecuencia tenemos que la transformada de Laplace de este tipo de señales no genera funciones racionales en $s$, lo que habitualmente ocurre con la mayoría de las señales continuas en el tiempo. Es evidente que este hecho hace que la transformada de Laplace de este tipo de señales no goce de los beneficios que tienen las transformadas de las señales continuas. Otra dificultad aparece cuando se desea realizar la transformada inversa. Se puede resolver el problema realizando el siguiente cambio de variable:
$$z=e^{sT} \qquad \qquad s= \frac{1}{T}\ln(z)$$
A partir de este cambio, la transformada de Laplace $X^{*}(s)$ será:
$$X(z)=\sum_{n=0}^{\infty}x(nT)z^{-n}$$
#### Relación entre el plano S y el plano Z
Como consecuencia del cambio de variable realizado, es necesario estudiar cual es la relación existente entre ambos planos. Para ello recordemos que $s$ es una variable compleja y se puede escribir como $s=\sigma + j\omega$. Por lo tanto:
$$z=e^{sT}=e^{(\sigma+j\omega)T}=e^{\sigma T}e^{j\omega T}$$
Donde $\omega_{s}= \frac{2\pi}{T}$
![[Pasted image 20250409124133.png#center|600]]
#### Propiedades
1) El eje $j\omega$ se transforma en la circunferencia de radio $|z|=1$. Sabemos que para encontrar la respuesta en frecuencia de un sistema analógico debemos evaluar al mismo sobre $s=j\omega$. Por lo tanto para encontrar la respuesta en frecuencia de un sistema discreto lo debemos hacer sobre $|z|=1$ es decir en: $z=e^{j\omega T}$.
$$X(e^{j\omega T})=\sum_{n=-\infty}^{\infty}x(nT)e^{-j\omega nT} \qquad \text{DTFT}$$
2) Para que un sistema analógico sea estable, debe tener todas sus singularidades en el semiplano izquierdo ($\sigma<0$). Como éste se transforma en $|z|<1$, resulta que todas las singularidades de un sistema discreto estable deberán estar dentro del círculo de radio $1$.
3) Una revolución completa alrededor del círculo $|z|=1$ corresponde a una variación $\omega_{s}$ a lo largo del eje $j\omega$.
#### Definición
La transformada Z de una secuencia $x(n)$ se define como:
$$X(z)=\sum_{n=-\infty}^{\infty}x(nT)z^{-n} \qquad \forall z\text{~donde } X(z)~\text{converge}$$
#### Teorema de Laurent
1) Dada una $G(z)$ tal que sea analítica e unívoca sobre 2 círculos concéntricos $C_{1}$ y $C_{2}$ con centro en $a$, y en el anillo comprendido entre $C_{1}$ y $C_{2}$, podemos expresar a $G(z)$ como:
$$G(z)=\sum_{n=-\infty}^{\infty}A_{n}(z-a)^{-n} \quad \text{donde} \quad A_{n}= \frac{1}{2\pi j} \oint_{\Gamma}G(z)(z-a)^{n-1} dz$$
	Siendo $\Gamma$ un camino cerrado entre $C_{1}$ y $C_{2}$.
2) La serie de Laurent es convergente y representa a la $G(z)$ en el anillo que se obtiene al aumentar el radio de $C_{2}$ y reducir el de $C_{1}$ en forma continua, hasta alcanzar los puntos donde $G(z)$ es singular.
3) La serie de Laurent de $G(z)$ es única en el anillo comprendido entre $C_{1}$ y $C_{2}$. Sin embargo, $G(z)$ puede tener distintos desarrollos en serie para diferentes anillos alrededor del mismo centro.
![[Pasted image 20250410102820.png#center|550]]
	Si comparamos la definición general de la transformada Z con la serie de Laurent, vemos que la Transformada Z de $X(z)$ corresponde al desarrollo de $X(z)$ alrededor del origen ($a=[0,0]$). De lo expuesto anteriormente surge que, dada una $X(z)$, tendremos diferentes desarrollos según sea la zona de convergencia elegida. Como este hecho tiene un impacto directo sobre la anti transformada, debemos estudiarlo con más detalle.
#### Secuencias finitas
Una secuencia $x(n)$ en la que un número finito de valores son distintos de cero, se conoce como secuencia finita. La transformada Z de dicha secuencia será:
$$X(z)=\sum_{n=n_{1}}^{n_{2}}x(nT)z^{-n} \qquad \qquad \text{siendo $n_1$ y $n_{2}$ finitos y enteros}$$
Para que $X(z)$ sea convergente, deberá cumplirse que:
$$|X(z)|<\infty \quad  \forall ~n ~ \text{tal que } n_{1}<n<n_{2}$$
Bajo estas condiciones, $z$ puede tomar cualquier valor, salvo $z=\infty$ (si $n_{1}<0$), y $z=0$ (si $n_{2}>0$)

En otras palabras, $X(z)$ será convergente en el intervalo $0 \leq |z| \leq \infty$ pudiendo quedar excluidos los puntos particulares $z=0$ y/o $z=\infty$ según sean $n_{1}$ y $n_{2}$. Vamos a estudiar los posibles casos:

![[Pasted image 20250410104320.png#center|500]]

![[Pasted image 20250410104341.png#center|500]]

![[Pasted image 20250410104418.png#center|500]]
#### Secuencias no finitas
Si en una secuencia finita uno o ambos límites no es finito, se dice que la secuencia es infinita.
1) Secuencias bilaterales: $X(z)=\sum_{n=-\infty}^{\infty}x(nT)z^{-n}$ 
![[Pasted image 20250410105921.png#center|450]]
2) Secuencias unilaterales derechas: $X(z)=\sum_{n=n_{1}}^{\infty}x(nT)z^{-n}$ 
![[Pasted image 20250410110001.png#center|450]]
3) Secuencias unilaterales izquierdas: $X(z)=\sum_{n=-\infty}^{n_{2}}x(nT)z^{-n}$
![[Pasted image 20250410110103.png#center|450]]
Son de particular interés las secuencias U.D. dado que estas representan a un sistema causal si $n_{1}\geq 0$. Se puede demostrar que estas secuencias convergen fuera de un círculo de radio $r_{1}$ es decir $|z| > r_{1}$.
#### Estabilidad
Un sistema lineal es estable si $\sum_{k=0}^{\infty}|h(n)|<\infty$

![[Pasted image 20250410111448.png#center]]

Esto significa que para que el sistema sea estable la región de convergencia debe contener a la circunferencia de radio 1. 

Si además queremos que el sistema sea causal, el infinito deberá pertenecer a la región de convergencia. De aquí se desprende que un sistema causal y estable deberá tener todos los polos dentro del círculo unitario. 

Es importante aclarar que la causalidad y la estabilidad son atributos independientes. Un sistema puede ser causal y no ser estable, ser estable y no causal. 

Debe además notarse que no basta con conocer una $H(z)$ para encontrar su antitransformada $h(n)$, sino también se deberá indicar la región de convergencia. 

En el caso particular de los sistemas estables y causales, la región de convergencia se extiende desde el círculo unitario hasta el infinito.
#### Función de transferencia
Cualquier sistema lineal, invariante y causal puede ser presentado por la siguiente ecuación:
$$\begin{split}
& y(n)=\sum_{k=0}^{M}b_{k}\cdot x(n-k) - \sum_{k=1}^{N}a_{k}\cdot y(n-k) \quad \text{donde $b_{0}=1$} \\
& Y(z)= \sum_{k=0}^{M}b_{k}\cdot X(z)\cdot z^{-k} - \sum_{k=1}^{N}a_{k}\cdot Y(z) \cdot z^{-k} \\
& H(z)= \frac{Y(z)}{X(z)} = \frac{\sum_{k=0}^{N}b_{k}\cdot z^{-k}}{1+\sum_{k=1}^{N}a_{k}\cdot z^{-k}}
\end{split}$$
##### Casos particulares
1) Caso 1: $a_{k}=0$, $1\leq k \leq N$
$$H(z)=\sum_{k=0}^{M}b_{k}\cdot z^{-k}= \frac{z^{M}}{z^{M}}\sum_{k=0}^{M}b_{k}\cdot z^{-k}= \frac{1}{z^{M}}\sum_{k=0}^{M}b_{k}\cdot z^{M-k}$$
Este sistema tiene M ceros cuyos valores dependerán de y M polos en el origen ($z=0$). Es decir que tenemos M polos triviales en $z=0$ y M ceros no triviales. Nótese que en este caso los sistemas son siempre estables. A los sistemas que tienen este tipo de transferencia se los conoce por los siguientes nombres: 
- FIR: Finite impulse response Filters 
- MA: Moving average Filters 
- All zero Filters
2) Caso 2: $b_{k}=0$, $1\leq k\leq M$
$$H(z)=\frac{z^{N}}{z{^{N}}} \frac{b_{0}}{1+\sum_{k=1}^{N}a_{k}\cdot z^{-k}}=\frac{b_{0}\cdot z^{N}}{\sum_{k=0}^{N}a_{k}\cdot z^{N-k}} \qquad a_{0}=1$$
En este caso $H(z)$ contiene N polos cuyos valores dependen de los coeficientes y un cero múltiple en $z=0$. Igual que antes, estos ceros se consideran triviales. A los sistemas que tienen este tipo de transferencia se los conoce por los siguientes nombres:
- AR: Auto Regressive 
- IIR: Infinite Impulse Response 
- All Pole Filters
3) Caso 3: $a_{k}\neq 0$, $1\leq k\leq N$ y $b_{k}\neq 0$, $1\leq k\leq M$
Este es el caso más general. El sistema no posee polos o ceros triviales. Las denominaciones más usadas de estos sistemas son: 
- ARMA: Auto Regressive Moving Average 
- IIR: Infinite Impulse Response
#### Transformada Z unilateral
Dada la transformada Z bilateral de una función, se puede definir la transformada Z unilateral o causal de una secuencia $x(n)$ como:
$$X^{+}(z)=\sum_{n=-\infty}^{\infty}x(nT)u(n)z^{-n}=\sum_{n=0}^{\infty}x(nT)z^{-n}$$
La transformada Z unilateral de una función siempre parte de $n=0$, independientemente de que $x(n)\neq 0$ $\forall n:n<0$.

Esta transformada tiene las siguientes propiedades:
- No contiene información de la función para $n<0$.
- Es única para funciones causales.
- La región de convergencia es siempre exterior a un circuito de radio r.

**Obs:** Del último punto surge que no es necesario especificar la región de convergencia dado que está implícita.
##### Atraso temporal
Dada $x(n) \leftrightarrow X^{+}(z)$    $$Z^{+}\{x(n-k)\}=z^{-k}\left( \sum_{l=-k}^{-1}x(l)z^{-l}+ \sum_{l=-0}^{\infty}x(l)z^{-l} \right)$$
El primer término se debe a que al desplazar la señal original hacia la derecha en $k$ muestras, implica que $k$ muestras que existían para valores de $n<0$ entraron en el semieje positivo, y por lo tanto deberán ser tenidas en cuenta. Desarrollando la expresión, se obtiene:
$$Z^{+}\{ x(n-k) \} = z^{-k}\left( \sum_{n=1}^{k}x(-n)z^{n}+X^{+}(z) \right) $$
##### Avance temporal
Dada $x(n) \leftrightarrow X^{+}(z)$    $$Z^{+}\{x(n+k)\}=\sum_{n=0}^{\infty}x(n+k)z^{-n} = z^{k}\left( X^{+}(z)-\sum_{l=k}^{k-1}x(l)z^{-l} \right)$$
**Observación:**
$$Y^{+}(z) = \overbrace{H(z)X^{+}(z)}^{\text{Zero State Response}} + \overbrace{H(z)A(z)}^{\text{Zero Input Response}}=H(z)X^{+}(z)+H(z)X_{ic}(z)= Y_{zs}^{+}(z)+Y_{zi}^{+}(z)
$$
La cantidad $X_{ic}$ puede interpretarse como una excitación equivalente debido a las condiciones iniciales.