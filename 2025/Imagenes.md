Dado un campo eléctrico, vale que $\vec{E}=-\nabla V(\vec{r})$, y $\nabla\cdot \vec{E} = \frac{\rho}{\varepsilon_{0}}$, por lo tanto, se cumple que:
$$
-\nabla\cdot(\nabla V(\vec{r})) = \frac{\rho}{\varepsilon_{0}} \to 

\begin{cases}
\nabla^{2}V(\vec{r})= -\frac{\rho}{\varepsilon_{0}}  \qquad \text{Ecuación de Poisson} \\
\nabla^{2}V(\vec{r}) = 0 \qquad \quad ~  \text{Ecuación de Laplace}
\end{cases}
$$
#### Relaciones electroestáticas

![[Pasted image 20250815104532.png#center|500]]
### Teorema de la unicidad
Dado un problema general del potencial ($\nabla^{2}V(\vec{r})= -\frac{\rho}{\varepsilon_{0}}$), puede demostrarse que existe solución $V(r)$ con $V \to 0$ para $r\to \infty$ y que esta solución es única.

El teorema de la unicidad permite encontrar soluciones por analogías con problemas conocidos. Por lo tanto, planteo un problema equivalente. Un problema es equivalente a otro si:
- Satisface la misma ecuación de Poisson.
- Satisface las mismas condiciones de contorno.
![[Pasted image 20250815113811.png#center]]

Los dos problemas serán equivalentes mientras que se restrinja el dominio para $z>0$. En ese caso, ambos cumplirán las siguiente ecuación de Poisson:
$$
\nabla^{2}V= -\frac{q}{\varepsilon_{0}} \delta(x)\delta(y)\delta(z-d) \qquad z>0
$$
**Obs:** Se utilizan deltas para describir una ‘densidad volumétrica’ en una partícula.

Al mismo tiempo, el potencial generado por dos cargas está dado por:
$$
V(x,y,z) = \frac{1}{4\pi\varepsilon_{0}}\left[ \frac{q}{\sqrt{ x{^{2}}+y{^{2}}+ (z-d){^{2}} }} + \frac{q'}{\sqrt{ x{^{2}}+y{^{2}}+ (z-d){^{2}} }} \right]
$$
Para que se cumpla la condición de contorno:
$$
V\bigg{|}_{z=0} = 0 \longrightarrow q' = -q
$$
**Observaciones:**
- Por encima del plano V se comporta como si tras el plano hubiera una carga puntual de signo opuesto situada simétricamente (carga imagen).
- La carga imagen NO existe. Son las cargas de la superficie del plano las que producen el campo equivalente al de una carga puntual.
### Densidad superficial de carga
La densidad de carga del plano no va a ser uniforme, ya que la establece/aporta la carga.

Utilizando las condiciones de contorno, $D_{2n}-D_{1n}= \rho_{s}$, y como el plano actúa como ‘conductor cerrado’ (no tiene campo eléctrico debajo), puedo decir que $D_{1n}=0$, por lo tanto:
$$
D_{2n}=\rho_{s} \to \varepsilon_{0}E_{n}=\rho_{s} \to \rho_{s}=E_{n}(x,y,0)\varepsilon_{0} \longrightarrow \rho_{s} = - \varepsilon_{0} \frac{\partial V}{\partial z}\bigg{|}_{z=0} = \frac{-qd}{2\pi(x{^2}+y{^2}+d{^2})^{3/2}} 
$$
