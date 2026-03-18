Uno de los problemas que aparecen al tratar el modelo de Bohr, más allá de la imposibilidad de trabajar átomos multielectrónicos, es que no explica el efecto Zeeman. Este efecto ocurre ya que si estamos en presencia de un campo magnético, no solo se ve la línea espectral esperada, sino que se ven más. En la circunferencia de radio $r_{n}$ entra un número entero ($n$) de veces la longitud de onda de De Broglie del electrón.

**Obs:** El modelo de Bohr es incompatible con el principio de incertidumbre, ya que según Bohr el eléctron debería tener una trayectoria (circular) bien definida, mientras que el principio de incertidumbre niega rotundamente este hecho.

Por esta misma razón, surge el modelo de Schrödinger, a partir de la mecánica cuántica. Según Schrödinger, el eléctro se mueve en la distribución de energía potencial que resulta en la interacción núcleo/electrón.

La energía potencial es descrita por la siguiente expresión:
$$U(r)= \frac{1}{4\pi \varepsilon_{0}} \frac{ze^{2}}{r}$$
Donde $r=\sqrt{x^{2}+y^{2}+z^{2}}$, ya que el modelo de Schrödinger es tridimensional. Además, $U(r)$ es independiente del tiempo, y tiene simetría esférica.
> Caso 3D para el pozo de potencial infinito
> ![[Pasted image 20240520144105.png|1000]]

$$\hat{H}\Psi(\vec{r},t)=\hat{E}\Psi(\vec{r},t)$$
Tengo en cuenta que está en estado estacionario ($\Psi(\vec{r},t)=\psi(\vec{r})e^{-i\omega t};\omega= \frac{E}{\hbar}$), por lo la expresión queda tal que:
$$\hat{H}\psi(\vec{r})=E\psi(\vec{r})$$
Esta ecuación está en coordenadas esféricas $\to \nabla^{2}$ está en coordenadas esféricas. Por lo que $\psi(\vec{r})=\psi(r,\theta,\varphi)$. Y se cumplen las siguientes igualdades: $x=r~sen(\theta)cos(\varphi),~y=r~sen(\theta)sen(\varphi),~z=r~cos(\theta)$.

![[Pasted image 20240519142001.png#center|400]]

Para poder trabajar con mayor facilidad la ec. de Schrödinger, aplicamos una sepación de variables: $\psi(r,\theta,\varphi)=R(r)Y(\theta,\varphi)=R(r)f(\theta)g(\varphi)$.

**Obs:** $Y_{lm_{l}}(\theta,\varphi)$ son los harmónicos esféricos y ya están normalizados.

**Obs:** $\hat{\vec{L}}$ se vuelve un observable de interés por estar en coordenadas esféricas.
$$\hat{\vec{L}}=\hat{\vec{r}}\times\hat{\vec{p}}=(\hat{y}\hat{p}_{z}-\hat{z}\hat{p}_{y})\hat{i}+(\hat{z}\hat{p}_{x}-\hat{x}\hat{p}_{z})\hat{j}+(\hat{x}\hat{p}_{y}-\hat{y}\hat{p}_{x})\hat{k}=\hat{L}_{x}\hat{i}+\hat{L}_{y}\hat{j}+\hat{L}_{z}\hat{k}$$
Donde se cumple:
$$\begin{align*}
\hat{L}_{x}&= i\hbar(sen(\varphi) \frac{\partial}{\partial \theta}+cotg(\theta)cos(\varphi)\frac{\partial}{\partial \varphi}) \\
\hat{L}_{y}&= -i\hbar(cos(\varphi) \frac{\partial}{\partial \theta}-cotg(\theta)sen(\varphi)\frac{\partial}{\partial \varphi}) \\
\hat{L}_{z}&= -i\hbar \frac{\partial}{\partial \varphi}
\end{align*}$$
Además:
$$\hat{L}^{2}=\hat{L}_{x}^{2}+\hat{L}_{y}^{2}+\hat{L}_{z}^{2}=-\hbar^{2}(\frac{\partial^{2}}{\partial \theta^{2}}+cotg(\theta)\frac{\partial}{\partial \theta}+cosec^{2}(\theta)\frac{\partial^{2}}{\partial \varphi^{2}})$$
> Observaciones:
> 1. $[\hat{L}^{2};\hat{L}_{x}]=[\hat{L}^{2};\hat{L}_{y}]=[\hat{L}^{2};\hat{L}_{z}]=0$
> 2. $[\hat{L}_{x};\hat{L}_{y}]=i\hbar\hat{L}_{z},~[\hat{L}_{z};\hat{L}_{x}]=i\hbar\hat{L}_{y},~[\hat{L}_{y};\hat{L}_{z}]=i\hbar\hat{L}_{x}$
> 3. $\vec{L}$ no puede ser nítido, ya que si lo fuese rompería rompería con el principio de incertidumbre. $\vec{L}=cte$.
> 4. $|\vec{L}|,~\vec{L}_{z}$ son nítidos.
> 5. $L_{x},~L_{y}$ son difusos.
> 6. $E$ nítida. Pero si superpongo estados de energía nítida, el resultado deja de serlo.

**Teorema:** Sean dos operadores lineales y hermíticos que poseen un conjunto común y completo de autofunciones ortonormales, dichos operadores conmutan. Además, si dos operadores conmutan, poseen un conjunto completo de autofunciones ortonormales comunes.
##### Planteamiento del problema
![[Pasted image 20240520074343.png#center|400]]
![[Pasted image 20240520074421.png#center|400]]
![[Pasted image 20240520074453.png#center|400]]
##### Conclusiones
$$\Psi_{nlm_{l}}(r,\theta,\varphi,t)=\psi_{nlm_{l}}(r,\theta,\varphi)\cdot e^{-i\omega_{n}t}$$
Donde $\omega_{n}= \frac{E_{n}}{\hbar}$ que sale de los estados permitidos se Bohr (sin tener en cuenta ninguna de las correcciones).

Los subíndices de la función de onda simbolizan en función de que trabajan. Por lo que para la función de onda independiente del tiempo se pueden separar las variables de la siguiente forma: $\psi_{nlm_{l}}(r,\theta,\varphi)=R_{nl}(r)f_{lm_{l}}(\theta)g_{m_{l}}(\varphi)$.

![[Pasted image 20240520075323.png#center|300]]

Para normalizar la función, podemos hacerlo de forma tradicional:
$$\int_{0}^{\infty}dr\int_{0}^{\pi}d \theta \int_{0}^{2\pi}|R_{nl}(r)|^{2}|f_{lm_{l}}(\theta)|^{2}|g_{m_{l}}(\varphi)|^{2}\cdot r{^{2}}\cdot sen(\theta)~d\varphi=1$$
Alternativamente, podemos normalizar cada función por separado:
$$\begin{align*}
\int_{0}^{\infty}|R_{nl}(r)|^{2}\cdot r^{2}~dr=1 \\
\int_{0}^{\pi}|f_{lm_{l}}(\theta)|^{2}\cdot sen(\theta)~d \theta =1\\
\int_{0}^{2\pi}|g_{m_{l}}(\varphi)|^{2}~d\varphi=1
\end{align*}$$
**Obs:** Como el potencial $U$ sólo depende de $r$ ($U(r)$) → Sólo me importan las funciones $R_{nl}(r)$.

Se define la **probabilidad radial** ($|R_{nl}(r)|^{2}\cdot r^{2}~dr=P_{nl}(r)~dr$) como la probablidad de encontrar el electrón en una corteza esférica de radio comprendido entre $r$ y $r+dr$.

El valor medio de $r$ para ciertos $n, l$ será tal que:$$<r>_{nl}=\int_{0}^{\infty}r\cdot P_{nl}(r)~dr$$
Para un estado cualquiera($Z=1$): $<r>_{nl}=n^{2}a_{0}\left(1+ \frac{1}{2}\left(1- \frac{l(l+1)}{n^{2}}\right)\right)$. Podemos observar que es fuertemente dependiente de $n$, y débilmente dependiente de $l$.

**Observaciones:**
- $|g_{m_{l}}(\varphi)|^{2}= \frac{1}{2\pi}$
- $|f_{lm_{l}}(\theta)|^{2}\cdot sen(\theta)~d \theta= P_{lm_{l}}(\theta)~d\theta:$ Es la probabilidad de encontrar el electrón en el ángulo sólido comprendido entre $\theta$ y $\theta+d\theta$.

Mediante las observaciones hechas, podemos decir que la probabilidad de encontrar el electrón en un elemento de volumen $d\omega$ será:
$$|\Psi_{rlm_{l}}(r,\theta,\varphi,t)|^{2}d\omega=P_{nl}(r)\cdot P_{lm_{l}}(\theta)\cdot \frac{1}{2\pi}\cdot dr~d\theta~d\varphi$$
**Obs:** La probabilidad es independiente del tiempo y de $\varphi$.
###### Expresiones útiles
$$|\vec{L}|=\sqrt{l(l+1)}\cdot\hbar~;~L_{z}=m_{l}\hbar~;~L_{z}\leq |\vec{L}|\Rightarrow |m_{l}|\leq l$$
$$\text{Ec. radial}\qquad \left(- \frac{\hbar^{2}}{2m}\left(\frac{d^{2}}{dr^{2}}+ \frac{2}{r} \frac{d}{dr}\right)+ \frac{l(l+1)\hbar^{2}}{2mr^{2}}+U(r)\right)\cdot R(r)=E\cdot R(r)$$
Esta solución aparece tras trabajar con la ecuación de Schrödinger en coordenadas esféricas. Para una fuerza central ($U(\vec{r})=U(r)$). La ecuación me quedará una parte radial y otra las harmónicas esféricas.
$$- \frac{\hbar^{2}}{2m}\frac{d^{2}}{dr^{2}}(r\cdot R(r))+ \frac{l(l+1)\hbar^{2}}{2mr^{2}}r\cdot R(r)+U(r)\cdot r\cdot R(r)=E\cdot r\cdot R(r)$$
Llamo $g(r)=r\cdot R(r)$. Aparece $U_{eff}=\frac{l(l+1)\hbar^{2}}{2mr^{2}}+U(r)$.
###### Igualdades útiles
$$\begin{align}
&P(r)dr=4\pi r^{2}|\Psi|^{2}dr \qquad P(r)= |rR|^{2}=|g(r)|^{2}\\
&1=\int_{0}^{\infty}P(r)dr ~;~<r> =\int_{0}^{\infty}r\cdot P(r)dr ~;~<f> =\int_{0}^{\infty}f(r)\cdot P(r)dr
\end{align}$$
**Obs:** $\Psi_{nlm_{l}}(r,\theta,\varphi,t)=R_{nl}(r)f_{lm_{l}}(\theta)g_{m_{l}}(\varphi)e^{-i\omega t}$ son autofunciones de $\hat{H},~\hat{L^{2}}$ y $\hat{L_{z}}$.

**Obs:** Como $L_{z}$ es un observable nítido → $\Delta L_{z}=0$ → $<L_{x}> = <L_{y}> =0$.
##### Emisión de fotones
- $<r>_{nl}$ es independiente del tiempo (estado estacionario). El átomo en un estado estacionario no emite.
- $<r>_{ij}:$ Cuando el electrón pasa de un nivel de energía $i$ a otro nivel $j$ → Es dependiente del tiempo → El átomo emite un fotón: $hf = E_{i}-E_{j}$, con $E_{i}>E_{j}$.
- Se definen $\Delta l= \pm 1$ (*desexcitación espontánea*) y $\Delta m_{l}=0,~\pm 1$ las **transiciones permitidas**.
- Las transiciones con probabilidades despreciables son **prohibidas**.
![[Pasted image 20240527191935.png#center|350]]
**Obs:** El pasaje de $2s$ a $1s$ es prohibido, ya que $l$ puede aumentar o decrementar en uno, nunca permanecer igual.
#### Momento dipolar magnético orbital
![[Pasted image 20240527192259.png#center|100]]
$$\vec{\mu}= - \frac{e}{2m}\vec{L}$$
Definimos el **magnetón de Bohr** como $\mu_{B}= \frac{e\hbar}{2m}=9.274\cdot 10^{-24} \frac{J}{T}$. A partir de esta definición, describimos el momento dipolar magnético orbital:
$$\vec{\mu}_{L}= - \frac{\mu_{B}\vec{L}}{\hbar}$$
Y su operador cuántico:
$$\hat{\vec{\mu}}_{L}= - \frac{\mu_{B}\hat{\vec{L}}}{\hbar}$$
Al aplicar un campo magnético, aparece este momento dipolar magnético orbital que va a tender a girar (torque) para acercarse a la dirección del campo magnético (posición de equilibrio).

> Observación
> ![[Pasted image 20240527193105.png|450]]

$$U=\mu_{B}m_{l}B= \frac{e\hbar}{2m}m_{l}B=\hbar \omega_{L}m_{l}$$
Siendo $\omega_{L}= \frac{e\hbar}{2m}$ la frecuencia de Larmor.

Como aparece un campo magnético, por efecto Zeeman aparece una energía potencial $U$ que tenemos que considerar en nuestra expresión de energía. Por lo que la energía queda tal que:
$$E=- \frac{Z^{2}13.6~eV}{n^{2}}+U$$
Por lo que se rompe la degeneración.

**Obs:** En el estado fundamental no habrá efecto Zeeman, ya que $n=1 \to m_{l}=0$. No se verán otras líneas espectrales sin importar el campo magnético que aplique.

**Obs:** Por simetría, en el estado fundamental $<p> =0$.

Las líneas espectrales que vemos en el efecto Zeeman se deben a la desexcitación de un gas en presencia de un campo magnético uniforme. Las líneas espectrales que se vean serán acordes a $\Delta m_{l}= -1,~0,~1$. Por lo que la energía será distinta en los tres casos y la frecuencia del fotón emitido será también distinta.

#### Spin del electrón
##### Experimento de Stern-Gerlach
Ante un campo magnético uniforme: $\vec{F}=\vec{0}$. Pero para un campo magnético NO uniforme esto no se cumple, sino que la fuerza es tal que: $\vec{F}=-\nabla(-\vec{\mu}\cdot\vec{B})$.
Según el modelo de Schrödinger, que toma $\vec{\mu}=\vec{\mu}_{L}=- \frac{\mu_{B}}{\hbar}\vec{L}$, el haz debería desdoblar en $2l+1$ componentes. Pero en el experimento hay el doble. Por lo que nace el concepto de giro del electrón, y entiendo que el vector momento del electrón es la superposición del momento orbital, y el momento de spin del mismo. Esta explicación no es posible con el modelo clásico, ya que el electrón no tiene forma definida. Por lo tanto, ahora se define $\vec{\mu}=\vec{\mu}_{L}+\vec{\mu}_{S}$, y se conoce como efecto Zeeman anómalo.

Surgen las siguientes definiciones:
$$S^{2}=s(s+1)\hbar^{2}; s= \frac{1}{2} \Rightarrow S= \frac{\sqrt{3}}{2}\hbar$$
$$S_{z}=m_{s}\hbar \longrightarrow m_{s}= \pm \frac{1}{2} \quad \text{Precesión alrededor del eje z}$$
Además, se cumple que: $\varphi_{m_{s}}(S_{z})$ es autofunción de $\hat{S^{2}}$ y $\hat{S_{z}}$. La función de onda completa ($\Psi_{nlm_{l}m_{s}}(r, \theta, \phi, t)$) es autofunción de $\hat{L^{2}}, \hat{L_{z}}, \hat{S^{2}}$ y $\hat{S_{z}}$.

la energía potencial es: $U=-\vec{\mu}_{S}\cdot \vec{B}$, y $\vec{\mu}_{S}=- \frac{g_{s}\mu_{B}}{\hbar}\vec{S}$, siendo $g_{s}: \text{Factor g de spin} \to g_{s}\simeq 2$. Y además la fuerza en el eje z será: $F_{z}=\mu_{B}g_{s}m_{s} \frac{dB_{z}}{dz}$.

**Obs:** Para las capas completas: $\vec{\mu}_{L}=\vec{\mu}_{S}=\vec{0}$.

Para una estructura fina → Interacción spin/órbita (Problema relativista) → Duplicación de muchas líneas del espectro de emisión sin $\vec{B}_{ext}$.
##### Principio de exclusión de Pauli
No puede haber dos electrones con la misma configuración electrónica.

**Regla de Hund:** Cuando un átomo tiene orbitales de igual energía, el orden de llenado por electrones es tal que el máximo número de electrones quedan con espines desapareados.