A partir de la ecuación de Helmholtz $\nabla^{2}\vec{E}-\mu_{0}\varepsilon_{0} \frac{\partial \vec{E}}{\partial t^{2}}=0$, la solución con funciones armónicas será:
$$
\vec{E}(\vec{r},t)=\vec{E}_{0}e^{-j\vec{k}\cdot \vec{r}}\cdot e^{j\omega t} = \vec{E}_{0}e^{j(\omega t-\vec{k}\cdot \vec{r})}
$$
Donde $E_{0} = E_{0x}\hat{x}+E_{0y}\hat{y}+E_{0z}\hat{z}$, y $\vec{k}=k_{x}\hat{x}+k_{y}\hat{y}+k_{z}\hat{z}$, denominado el vector de onda. Esta expresión es general para describir el campo para una onda que se aleja del origen en dirección $\vec{k}$.

Las superficies de fase constante están dadas por:
$$
\omega t-\vec{k}\cdot \vec{r}=cte
$$
### Onda plana uniforme
Si los planos equifásicos son paralelos se dice que los campos forman una onda plana. Además, si las superficies de amplitud constante son planos, la onda se denomina una onda plana uniforme, los campos no son función de las coordenadas que forman los planos equifásicos y los planos de igual amplitud.

![[Pasted image 20251102200112.png#center|400]]

### Transversalidad de la onda
A partir del teromea de Gauss, se puede demostrar que:
$$
\nabla\cdot \vec{E}= \vec{k}\cdot \vec{E}=0 \to \vec{E} \perp \vec{k}
\qquad 
\nabla\cdot \vec{B}= \vec{k}\cdot \vec{B}=0 \to \vec{B} \perp \vec{k}
$$
Los campos en la dirección de propagación son nulos, ya que los campos son perpendiculares a la dirección de propagación.
### Ondas planas
Sabemos que el campos $\vec{E}$ es perpendicular a $\vec{H}$. Supongamos un caso donde los campos sólo dependen de $z$, y el campo eléctrico $\vec{E}$ sólo existe en la componente $\hat{x}$. En este escenario, se puede demostrar que la relación entre camnpo eléctrico y campo magnético está dado por:
$$
\vec{H} = H_{y}^{+} + H_{y}^{-} =\frac{1}{\sqrt{ \frac{\mu_{0}}{\varepsilon_{0}} }}(E_{x}^{+}-E_{x}^{-}) \,\hat{y}
$$
A partir de esta relación, aparece el término de impedancia intrínseca:
$$
\eta_{0}= \frac{E_{x}^{+}}{H_{y}^{+}} = - \frac{E_{x}^{-}}{H_{y}^{-}} = \sqrt{ \frac{\mu_{0}}{\varepsilon_{0}} } = 376.73 \ohm \qquad \text{Impedancía intrínseca del vacío}
$$
Hay muchas formas de relacionar estos parámetros, y dependerá del caso cual sea el más conveniente:
$$
\vec{H}(z,t) = \frac{\hat{z}\times \vec{E}(z,t)}{\eta_{0}}
$$
Esta definición es más general, donde $\hat{z}$ viene dado por la dirección en la que se desplaza la onda electromagnética.

**Obs:** $E$ y $H$ son perpendiculares entre sí, y perpendiculares a la dirección de propagación ,y además están en fase en el vacío.

**Obs:** El signo se considera a partir del versor de la dirección de propagación de la onda.

La relación entre los módulos será:
$$
|\vec{H}| = \frac{|\vec{E}|}{\eta_{0}} \qquad |\vec{B}| = \frac{|\vec{E}|}{c_{0}}
$$
#### Velocidad de fase y relación de dispersión
Se define el frente de onda como una superficie de fase constante de una onda.

A partir de esto:
$$
\omega t-kz = \phi_{0} \to z = \frac{wt-\phi_{0}}{k} \to v_{p} = \frac{dz}{dt} = \frac{\omega}{k} = \frac{1}{\sqrt{ \mu_{0}\varepsilon_{0} }} \quad \text{Velocidad de fase}
$$
Donde $k= \frac{2\pi}{\lambda} = \frac{\omega}{c_{0}} \to \omega=c_{0}\cdot k$ es la **relación de dispersión**.
#### Vector de Poynting
El cálculo del vector de Poynting instantáneo viene dado por la expresión de los campos en su forma verdadera, es decir, su parte real.
$$
\vec{S}(\vec{r}, t) = \vec{E}\times \vec{H} = \frac{E_{0}^{2}}{\eta_{0}}\cdot \cos^{2}(\omega t-kz+\phi_{0}) \, \hat{z}
$$
**Obs:** La contribución de la densidad de energía eléctrica y magnética son iguales en una onda electromagnética.
$$
\mu=\varepsilon_{0}E^{2}= \frac{B^{2}}{\mu_{0}} \to |\vec{S}|=\mu\cdot c_{0}
$$
El valor medio temporal del vector de Poynting está dado por:
$$
\langle\vec{S}(\vec{r},t)\rangle = \frac{1}{T} \int_{0}^{T} \vec{E}(\vec{r},t)\times \vec{H}(\vec{r},t) \, dt = \frac{1}{2}\cdot \mathcal{Re}\left( \vec{E}_{0}\times \vec{H}_{0}^{*} \right) = \frac{1}{2}\cdot \mathcal{Re}\left( \frac{E_{0}^{2}}{\eta_{0}} \right)  
$$
El promedio temporal del vector de Poynting de una onda representa la potencia media temporal que la onda transporta por unidad de área transversal a la dirección de propagación, se conoce como **intensidad de la radiación** en las aplicaciones ópticas → $I = \langle|\vec{S}|\rangle = \frac{1}{2}\cdot \mathcal{Re}\left( \frac{E_{0}^{2}}{\eta_{0}} \right)$

**Obs:** Una onda plana sólo puede ser generada por una fuente de extensión infinita. En cambio, una fuente puntual genera una onda esférica.

Para una onda esférica, el frente de onda es esférico, puesto que la velocidad es la misma en todas las direcciones. Además, a grandes distancias ($R\gg \lambda$) con respecto a la fuente. se puede considerar al frente de onda como localmente plano.

La solución a la ecuación de Helmholtz en coordenadas esféricas es:
$$
E_{\theta} = \frac{E_{0}}{r}\cdot e^{j(\omega t-\vec{k}\cdot \vec{r})}
$$
Es fácil ver mediante esta expresión que la amplitud disminuye con la distancia a la fuente.

![[Pasted image 20251102204051.png#center|300]]
La relación entre los campos está dada por:
$$
\vec{H}(\vec{r},t) = \frac{\hat{r}\times \vec{E}(\vec{r},t)}{\eta_{0}}
$$
**Obs:** Se cumple la condición de transversalidad → $E_{r}= H_{r} = 0$
#### Ondas en medios materiales
**DIELÉCTRICO PERFECTO**
En la ec. de onda si el medio es LIH, se reemplaza $\varepsilon_{0}$ y $\mu_{0}$ por $\varepsilon$ y $\mu$ (Teorema de Extinción de Ewald-Oseen). De esta forma, se reescriben las siguientes expresiones:
$$
\beta=\omega \sqrt{ \mu\varepsilon } \quad \eta=\sqrt{ \frac{\mu}{\varepsilon} } \quad v = \frac{c_{0}}{\sqrt{ \varepsilon_{r} \mu_{r} }} \simeq \frac{c_{0}}{\sqrt{ \varepsilon_{r} }}
$$
En medios no magnéticos: $\mu_{r} = 1$

Se define el **índice de refracción** como:
$$
n = \frac{c_{0}}{v} = \sqrt{\varepsilon_{r} \mu_{r} } \underbrace{\to}_{\text{medio no magnético}} n=\sqrt{ \varepsilon_{r} }
$$
Dado que no hay cargas libres, pero si conductividad en el material:
$$
\nabla \times \vec{H} = \varepsilon  \frac{\partial \vec{E}}{\partial t} = (\sigma + j\omega\varepsilon)\vec{E} = j\omega \underbrace{\left( \varepsilon+ \frac{\sigma}{j\omega} \right)}_{\varepsilon_{c}}\vec{E}
$$
Donde $\varepsilon_{c} = \varepsilon - j \frac{\sigma}{\omega} = \varepsilon' - j\varepsilon''$. A partir de esta relación, se puede interpretar un comportamiento como en las líneas de transmisión, donde aparece una reflexión y transmisión de las ondas.
$$
\vec{E}(\vec{r}) = \vec{E}_{1} e^{-\gamma z} + \vec{E}_{2}e^{\gamma z}
$$
Donde $\gamma= j\omega \sqrt{ \mu\varepsilon_{c} }= \sqrt{ j\omega \mu(\sigma+j\omega\varepsilon) } = \alpha + j\beta$

**Interpretación gráfica**
![[Pasted image 20251102210028.png#center|350]]
![[Pasted image 20251102210812.png#center|350]]
Donde se cumple que:
$$
\alpha^{2}-\beta^{2}= -\omega^{2}\mu\varepsilon \quad \wedge \quad 2 \alpha \beta = \omega \mu \sigma \to \begin{cases}
\alpha = \omega \sqrt{ \frac{\mu\varepsilon}{2} }\sqrt{\sqrt{ 1+ \left( \frac{\sigma}{\omega\varepsilon} \right)^{2} } -1} \quad \left[ \frac{Np}{m} \right] \\
\beta = \omega \sqrt{ \frac{\mu\varepsilon}{2} }\sqrt{\sqrt{ 1+ \left( \frac{\sigma}{\omega\varepsilon} \right)^{2} } +1} \quad \left[ \frac{rad}{m} \right]
\end{cases}
$$
Se cumple que: $\lambda = \frac{v_{p}}{f} = \frac{2\pi}{\beta}$

Ahora, la relación entre los campos será:
$$
\vec{H}(z) = \frac{\gamma}{j\omega \mu} \hat{z}\times \vec{E}(z)
$$
Por lo tanto, la impedancia intrínseca será:
$$
\eta = \frac{j\omega \mu}{\gamma}
$$
Esta definición conduce a un índice de refracción complejo → $n_{c} = n - jk$

**Obs:** En un medio con pérdidas, los campos $E$ y $H$ están desfasados.

**DIELÉCTRICO DE BAJAS PÉRDIDAS**
Las pérdidas en el dieléctrico se deben a las fuerzas moleculares que el campo eléctrico debe superar para polarizar el dieléctrico.

En este caso, reaparece el concepto de la tangente del ángulo de pérdidas: $\tan(\delta_{c}) = \frac{\varepsilon''}{\varepsilon'}$. Se supone que este valor debe ser pequeño, por lo que $\tan(\delta_{c})\ll 1$

Los parámetros para este caso serán:
$$
\alpha \simeq \omega \sqrt{ \mu\varepsilon' } \frac{\tan(\delta_{c})}{2} = \frac{\omega\varepsilon''}{2}\sqrt{ \frac{\mu}{\varepsilon'} } \quad \beta \simeq \omega \sqrt{ \mu\varepsilon' } = \sqrt{ \varepsilon_{r} } k_{0}=k \quad v_{p} = \frac{\omega}{\beta} \simeq \frac{c_{0}}{\sqrt{ \varepsilon_{r} }}
$$
La impedancia intrínseca resulta:
$$
\eta \simeq \frac{\eta_{0}}{\sqrt{ \varepsilon_{r} }} e^{\frac{j \tan(\delta_{c})}{2}}
$$
Se define la profundidad de penetración en un material, como la distancia a la que una onda plana sufre una atenuación de $\frac{1}{e}$.
$$
e^{-\alpha z} = e^{-\alpha \delta} \to \alpha \delta=1 \to \delta = \frac{1}{\alpha}
$$
En un conductor perfecto $\sigma\to \infty$. En cambio, en un buen conductor existe algo de atenuación:
$$
\frac{\sigma}{\omega\varepsilon'}\gg 1 \to \varepsilon_{c} = \left( \varepsilon'-j \frac{\sigma}{\omega} \right) \simeq - j \frac{\sigma}{\omega}
$$
En un buen conductor, la velocidad de fase será:
$$
v_{p} = \frac{\omega}{\beta} \simeq \sqrt{ \frac{2\omega}{\mu \sigma} }\ll c_{0} \to \lambda= 2\sqrt{ \frac{\pi}{f\mu \sigma} }
$$
Y la impedancia intrínseca
$$
\eta \simeq \sqrt{ \frac{j\omega \mu_{0}}{\sigma} }
$$