Teorías lineales y no lineales.

En las teorías lineales se cumple que a partir de las soluciones que obtenga de la ecuación, podré crear una nueva solución a partir de la combinació n lineal de las otras soluciones. En las teorías no lineales no se cumple esto.

Se define al **operador** como un objeto matemático, el cual al aplicarlo sobre una función me da como resultado otra función. Se nota a los operadores con ^ encima del operador.

##### Operador lineal
$$\hat{A}(c_{1}\varphi_1+c_{2}\varphi_{2})=c_{1}\hat{A}\varphi_{1}+c_{2}\hat{A}\varphi_{2} \qquad c_{1},c_{2}\in \mathbb{C}$$
##### Conmutador
$$\hat{A}(\hat{B}\varphi)=\hat{B}(\hat{A}\varphi)$$
Esto se cumplirá si los operadores son conmutables, por lo que se debe cumplir que: $\left[\hat{A};\hat{B}\right]\varphi=\hat{A}(\hat{B}\varphi)-\hat{B}(\hat{A}\varphi)=0$
##### Ecuación de autovalores
$$\hat{A}\varphi_{n}=a_{n}\varphi_{n}$$
Donde $\varphi_{n}$ es la **autofunción n**, y $a_{n}$ el **autovalor n**.

Si $a$ es el autovalor de $n$ autofunciones, se dice que el problema es degenerado de grado $n$.

![[Pasted image 20240515165054.png#center|400]]
##### Operador hermítico
Es un operador lineal que se aplica en el espacio de Hilbert, donde se cumple por el producto escalar: $<\varphi_{1}, \hat{A}\varphi_{2} > = <\hat{A}^{*}\varphi_{1},\varphi_{2} >$ $\Rightarrow$ podemos afirmar que $\hat{A}=\hat{A}^{*}$, y si se cumple esto, $\hat{A}$ es un **operador hermítico**.

**Obs:** Para la ecuación de autovalores de un operador hermítico, los autovalores son reales. Y si los dominios coinciden totalmente $\to$ Operador autoadjunto.

**Obs:** Las autofunciones de un operador hermítico correspondientes a autovalores distintos son ortogonales → Su producto escalar es cero.
#### Operadores cuánticos
A todo observable le corresponde un operador cuántico que es lineal y hermítico, que se obtiene a partir de las siguientes reglas:
1. **Operador posición:** $\vec{r}=(x;y;z)\to \hat{\vec{r}}=\vec{r}$.
2. **Operador cantidad de movimiento:** $\vec{p}=(p_{x};p_{y};p_{z})\to \hat{\vec{p}}=-i\hbar \nabla=-i\hbar (\frac{\partial}{\partial x};\frac{\partial}{\partial y};\frac{\partial}{\partial z})$.
3. A todo observable que pueda expresarse como $A=A(\vec{r},\vec{p})\to \hat{A}=A(\hat{\vec{r}},\hat{\vec{p}})$.
	- $\hat{K}=- \frac{\hbar^{2}\nabla^{2}}{2m}$
	- $\hat{U}=U(\vec{r})$
	- Problemas conservativos: $H=K+U\to \hat{H}=\hat{K}+\hat{U}=- \frac{\hbar^{2}\nabla^{2}}{2m}+U(\vec{r})$, entonces con el operador Hamiltoniano podemos reescribir la ec. de Schrödinger independiente del tiempo: $\hat{H}\psi(\vec{r})=E\psi(\vec{r}) \to \hat{H}\psi(x)=E\psi(x)$ (1D)
$$[\hat{x};\hat{p}_{x}]=[\hat{y};\hat{p}_{y}]=[\hat{z};\hat{p}_{z}]=i\hbar$$
$$[\hat{x};\hat{p}_{y}/(\hat{p}_{z})]=[\hat{y};\hat{p}_{x}/(\hat{p}_{z})]=[\hat{z};\hat{p}_{x}/(\hat{p}_{y})]=0$$
Si el conmutador de dos operadores cuánticos es cero, quiere decir que los observables representados por dichos operadores cuánticos pueden ser medidos simultáneamente y con precisión arbitraria. Por lo tanto, no existe una relación de incertidumbre entre estos. Si el conmutador entre los operadores no es cero, estos si tendrán una relación de incertidumbre.

![[Pasted image 20240515174235.png#center|300]]

Para escribir la ecuación de Schrödinger completa como ec. de autovalores, se debe establecer el **operador energía** $\hat{E}=i\hbar \frac{\partial}{\partial t}$, de modo que la ecuación quede como: $\hat{H}\Psi(x,t)=\hat{E}\Psi(x,t)$. Pero notamos que el operador $\hat{E}$ no puede ser autovalores de $\hat{H}$, por lo que no podemos decir que es una ecuación de autovalores.

![[Pasted image 20240515175251.png#center|400]]

![[Pasted image 20240515175408.png#center|400]]

**Obs:** Los operadores poseen un conjunto completo de autofunciones ortonormales, es decir, ortogonales y normalizados.

La función de onda $\Psi(\vec{r},t)$ puede ser ecrita de la siguiente manera: $\Psi(\vec{r},t)=\sum\limits_{i}c_{i}(t)\phi_{i}(\vec{r})$, donde los $c_{i}(t)$ son coeficientes completos que dependen del tiempo y las $\phi_{i}(\vec{r})$ son las autofunciones de alguno de los operadores cuánticos.

![[Pasted image 20240515200013.png#center|250]]

Además, se debe cumplir que $\sum\limits_{i}|c_{i}(t)|^{2}=1$.
#### Superposición de estados
Al escribir la función de onda, existe una superposición de funciones de onda de estados estacionarios de diferentes energías.

![[Pasted image 20240515200321.png#center|300]]

La dependencia del tiempo depende de la diferencia de energías $E_{1}$ y $E_{2}$ y no de sus valores individuales.

Una serie de medidas de un observable $A$ en un conjunto de sistemas idénticos  dará en general una distribución de resultados (Los instrumentos no marcan siempre lo mismo).

Se define el valor medio de $A$ (valor de expectación) a la expresión:
$$<A> =\bar{A}=\int_{\Omega}\Psi^{*}(\vec{r},t)(\hat{A}\Psi(\vec{r},t))d\omega$$
En valores propios discretos se define el valor medio de la siguiente forma:
$$<A> =\sum\limits_{i}|c_{i}(t)|^{2}a_{i}$$
Donde se cumple $\hat{A}\phi_{i}=a_{i}\phi_{i}$. Y además los valores de $|c_{i}(t)|^{2}$ representan las probabilidades de medir el autovalor $a_{i}$.

**Obs:** Se dice que el observable es nítido si la incertidumbre del operador es cero.

![[Pasted image 20240515202257.png#center|300]]
