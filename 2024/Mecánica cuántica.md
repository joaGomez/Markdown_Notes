#### Interpretación de la mecánica cuántica
La materia y la radiación electromagnética pueden concebirse tanto como partícula, como onda, dependiendo del fenómeno que se observe.

La amplitud de la onda asociada con la partícula se le llama **amplitud de probabilidad**, o **función de onda**, y se simboliza con $\Psi$.
$$\Psi(\hat{r_{1}}, \hat{r_{2}},..., \hat{r_{j}},...,t)=\psi (\hat{r_{j}})e^{-i\omega t}$$
$\psi$ no se puede observar, pero se puede medir la cantidad real $|\psi|^{2}$, conocida como **densidad de probabilidad**. Es la probabilidad relativa por cada unidad de volumen que la partícula encontrará en cualquier punto determinado en el volumen. La probabilidad de hallar la partícula en el elemento de volumen es:
$$P(x,y,z)dV=|\psi|^{2}dV$$
La funció de onda $\psi$ para una partícula libre ($U=0$ y $|\psi|^{2}=A^{2}=cte$) que se mueve a lo largo del eje $x$ se puede escribir como:
$$\psi(x)=A e^{i(kx-\omega t)}$$
Donde $k= \frac{2\pi}{\lambda}$. Además, se cumplen las siguientes igualdades:
$$\omega= \frac{E}{\hbar}=\frac{\hbar k^{2}}{2m} \quad k= \frac{p}{\hbar} \quad \lambda f= \frac{\omega}{k}=v_{f}=\frac{v_{g}}{2}= \frac{\hbar k}{2m} $$
#### Funciones de onda unidimensional y valores permitidos
La partícula debe estar ubicada a lo largo del eje $x: |\psi|^{2}dV\to|\psi|^{2}dx$.
$$P(x)dx=|\psi|^{2}dx$$
Aún cuando no es posible especificar la posición de una partícula con certeza completa, es posible por medio de $|\psi|^{2}$ especificar la probabilidad de observarla en una región que rodea un punto $x$ determinado. La probabilidad de hallar la partícula en el intervalo arbitrario $a\leq x\leq b$ es:
$$P_{ab}=\int_{a}^{b}|\psi|^{2}dx$$
La partícula debe estar en algún lugar a lo largo del eje $x$, la suma de las probabilidades en todos los valores de $x$ debe ser 1:
$$\int_{-\infty}^{\infty}|\psi|^{2}dx =1 $$
Cualquier función de onda que satisfaga esta ecuación se dice que está **normalizada**. Esto significa que la partícula existe en algún punto en el espacio.

Se denomina **valor esperado** a la posición promedio a la que se espera hallar la partícula después de muchas mediciones.
$$\langle x\rangle \equiv \int_{-\infty}^{\infty}\psi^{*}\cdot x\cdot\psi~ dx$$
Con los paréntesis $\langle ...\rangle$ se indican valores permitidos. Es posible hallar el valor esperado de cualquier función $f(x)$ asociado a una partícula:
$$\langle f(x)\rangle \equiv \int_{-\infty}^{\infty}\psi^{*}\cdot f(x)\cdot\psi~dx$$
#### La partícula cuántica bajo condiciones frontera
Una partícula confinada a una región unidimensional del espacio se modela como una partícula bajo rapidez constante. La magnitud de su cantidad de movimiento permanece constante, al igual que su energía cinética.

Si pensamos una partícula en una caja, las paredes son impenetrables, no existe probabilidad alguna de hallar la partícula fuera de la caja. $\psi$ debe ser $0$ para $x<0 \wedge x>L$, y por ser una función continua $\to \psi(x=0)=\psi(x=L)=0$.

La energía potencial del sistema no depende de la ubicación de la partícula $\to$ Es posible escoger su valor igual a $0$. Fuera de la vaja, la función de onda debe ser cero. Por eso, puedo también definir la energía potencial del sistema como infinitamente grande si la partícula estuviera fuera de la caja. Por lo tanto, la única manera de que una partícula este fuera de la caja, se necesita que el sistema tenga una cantidad infinita de energía, lo cual es imposible.

Dentro de una caja, se puede definir la función de onda como:
$$\psi(x)=A\cdot sen(\frac{2\pi x}{\lambda})$$
Donde se usa la longitud de onda de De Broglie asociada con la partícula.

Por las condiciones de borde: $\lambda= \frac{2L}{n} \to \psi(x)=A\cdot sen(\frac{n\pi x}{L})$

Normalizando: $A=\sqrt{\frac{2}{L}} \to \psi_{n}(x)=\sqrt{\frac{2}{L}}\cdot sen(\frac{n\pi x}{L})$

Del valor de la longitud de onda, podemos obtener la cantidad de movimiento de la partícula: $p= \frac{nh}{2L}$

La energía potencial del sistema es igual a cero cuando la partícula está dentro de la caja $\to$ Los valores permitidos de la energía del sistema son únicamente la energía cinética de la partícula:
$$E_{n}=(\frac{h^{2}}{8mL^{2}})\cdot n{^{2}}$$
Para $n=1,2,3,...$
> Obs
> ![[Pasted image 20240509170356.png#center|200]]

**Obs:** La energía está cuantizada. La energía mínima corresponde al estado fundamental, es decir, cuando $n=1:$
$$E_{1}= \frac{h^{2}}{8mL^{2}} \Rightarrow E_{n}=n^{2}\cdot E_{1}$$
Los $n\geq 2$ corresponden a **estados excitados**.

**Obs:** La menor energía de una partícula en la caja es diferente de cero. Según la mecánica cuántica, la partícula nunca puede estar en reposo.
#### Ecuación de Schrödinger
La ecuación de Schrödinger, como se aplica a una partícula de masa $m$ confinada a moverse a lo largo del eje $x$ e interactuar con su ambiente por medio de una función de energía potencial $U(x)$ es:
$$- \frac{\hbar^{2}}{2m}\frac{d^{2}\psi}{dx^{2}}+U\cdot \psi = E\cdot \psi$$
Donde $E$ es una constante igual a la energía total del sistema. Además, esta ecuación es independiente del tiempo.

**Obs:** $K+U=E=cte$.

$U$ puede ser discontinuo con la posición $\to$ Es necesario obtener soluciones a la ecuación para diferentes regiones del eje $x$.

> Demo
> ![[Pasted image 20240429144537.png]]
#### Partícula en un pozo de potencial finito
Considere una partícula en un pozo de potencial finito, es decir, un sistema que tenga una energía potencial que sea cero cuando la partícula está en la región $0<x<L$  y un valor finito $U$ cuando la partícula está fuera de esta región. Si $E<U$, según la mecánica clásica, la partícula estaría de modo permanente ligada en el pozo de potencial. Si la partícula estuviera fuera del pozo, su energía cinética debería ser negativa, lo que contradice totalmente la física clásica. Pero según la física cuántica, existe una probabilidad finita de que la partícula pueda encontrarse fuera del pozo, incluso si $E<U$. La función de onda por lo general, es diferente de cero fuera del pozo.

Para las distintas regiones, el valor de la función de onda es:
$$\begin{split}
&\psi_{1}=Ae^{Cx}  &x<0 \\
&\psi_{3}=Be^{-Cx} &x>L \\
& \psi_{2}=F~sen(kx)+G~cos(kx)
\end{split}$$
Y las condiciones frontera son:
$$\begin{split}
&\psi_{1}=\psi_{2} \qquad & \frac{d\psi_{1}}{dx}=\frac{d\psi_{2}}{dx} \quad &x=0 \\
&\psi_{2}=\psi_{3} \qquad & \frac{d\psi_{2}}{dx}=\frac{d\psi_{3}}{dx} \quad &x=L
\end{split}$$
Entonces: $$\psi(x)=\begin{cases} 0  & x\notin [0,L]\\
 \\
\sqrt{\frac{2}{L}}\cdot sen\left(\frac{n \pi}{L}x\right)  & x\in[0,L]
\end{cases}$$
> Demo
> ![[Pasted image 20240429150350.png]]

**Obs:** Se dice que $\psi(x)$ corresponde a un estado ligado si $\psi(x)\to 0$ cuando $|x|\to \infty$. Por lo que si unda partícula cuántica se mueve en una región finita del espacio (espacio ligado), la energía está cuantizada.

Por lo visto en el caso del pozo de potencial infinito, si $U(x)\to \infty \Rightarrow \psi(x)=0\Rightarrow \psi(x,t)=0$.

Como vimos con la ecuación de Schrödinger, tenemos una ecuación diferencial de segundo orden, y la solución va a cambiar acorde al término $\frac{2m}{\hbar^{2}}(E-U_{0})$, por lo que para distintos valores de potencial, la solución será diferente.

- Con $E>U_{0}:$
$$\frac{d^{2}\psi(x)}{dx^{2}}+ \frac{2m}{\hbar^{2}}(E-U_{0})\psi(x)=0$$
Donde $k^{2}=\frac{2m}{\hbar^{2}}(E-U_{0})$, y la energía cinética es $K=E-U_{0}$.

La solución para $\psi(x)$ será:
$$\psi(x)=Ae^{ikx}+Be^{-ik x}=Asen(kx)+Bcos(kx)\Rightarrow \Psi(x,t)=Ae^{i(kx-\omega t)}+Be^{-i(k x+\omega t)}$$
Aquí vemos como para distintos valores de $U_{0}$ cambia $k$, por lo que cambia $\psi(x)$.

**Obs:** El primer término en $\Psi(x,t)$ está asociado a una onda propagándose en el eje $x$ positivo, y el segundo término en el eje $x$ negativo.

- Con $E<U_{0}:$
El problema en este caso es que nos daría un valor de energía cinética negativo, por lo que hay que hacer algunos cambios en la ec. de Schrödinger:
$$\frac{d^{2}\psi(x)}{dx^{2}}- \frac{2m}{\hbar^{2}}(U_{0}-E)\psi(x)=0$$
Donde $\alpha^{2}=\frac{2m}{\hbar^{2}}(U_{0}-E)$, y mi valor de $\alpha$ ya no está relacionado a la energía cinética del objeto cuántico.

La solución para $\psi(x)$ en este caso será:
$$\psi(x)=Ae^{\alpha x}+Be^{-\alpha x}\Rightarrow \Psi(x,t)=Ae^{\alpha x - i\omega t}+Be^{-\alpha x - i\omega t}$$
En este caso, $\Psi(x,t)$ no representa un frente de onda plano propagándose.
#### Ecuación de continuidad
$$\frac{\partial}{\partial x}j(x,t)=-\frac{\partial p}{\partial t}$$
Donde se define la densidad de corriente de probabilidad como:
$$j(x,t)= \frac{i\hbar}{2m}\left(\Psi(x,t) \frac{\partial \Psi^{*}(x,t)}{\partial x}-\Psi^{*}(x,t) \frac{\partial \Psi(x,t)}{\partial x}\right)$$
Donde puede tomar los siguientes valores para los distintos escenarios descriptos por el objeto cuántico:
- $\Psi(x,t)=Ae^{i(kx-\omega t)}\Longrightarrow j(x,t)= \frac{\hbar k}{m}|A|^{2}=v_{x}|A|^{2}$
- $\Psi(x,t)=Ae^{-i(kx+\omega t)}\Longrightarrow j(x,t)= \frac{\hbar k}{m}|B|^{2}=v_{x}|B|^{2}$
- $\Psi(x,t)=Ae^{\alpha x -i\omega t} \vee \Psi(x,t)=Be^{-\alpha x -i\omega t} \Longrightarrow j(x,t)= 0$

#### Reflexión de electrones
Para analizar el comportamiento de un electrón tras un cambio de energía potencial, no lo podemos analizar con el modelo clásico, ya que no se comportará como una pelota que acorde a si tiene la energía suficiente para pasar la pared de potencial es imposible que rebote. En el caso de la cuántica, si hay un cambio en $U(x)$ a lo largo del eje $x$ tengo que considerar la posibilidad de que el elctrón modifique su dirección.

Para esto debo considerar las condiciones de continuidad: $\Psi(x,t)$ debe ser continua, por lo que $\psi(x)$ también debe serlo. A su vez, como los cambios en la energía potencial son saltos finitos puedo tratarlos como discontinuidades evitables, por lo que también pido continuidad en la derivada.

> **Obs: Caso particular**
> Barrera de potencial $U(x_{0})=U_{0}<E$
> ![[Pasted image 20240511124701.png|300]]

##### Coeficientes de reflexión y transmisión
$$R= \frac{|j_{ref}|}{j_{inc}} \qquad T = \frac{j_{trans}}{j_{inc}} \qquad R+T=1 \Rightarrow j_{inc}= |j_{ref}|+j_{trans}$$
**Obs:** Si $0<E<U_{0}$ hay **efecto túnel**.

#### Oscilador armónico
Tengo que $U(x)=\frac{1}{2}kx^{2}$ y la energía $E=K+U= \frac{1}{2}m\omega^{2}A^{2}$. Y como el obejto cuántico se encuentra en un estado ligado, la energía está cuantizada, por que responde a la siguiente expresión: $$E_{n}=\left(n+ \frac{1}{2}\right)\hbar \omega \qquad n=0,1,2,...$$
