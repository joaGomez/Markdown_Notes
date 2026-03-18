### Densidad de corriente de conducción y desplazamiento
Dado $\vec{J}_{c} = \sigma \vec{E}$, y $\vec{J}_{d}= \frac{\partial \vec{D}}{\partial t}$, por lo tanto:
$$
\frac{|\vec{J}_{c}|}{|\vec{J}_{d}|} = \frac{\sigma}{\omega \varepsilon} \qquad \text{Tangente del ángulo de pérdidas}
$$
Donde:
$$
\begin{align*}
&\frac{\sigma}{\omega\varepsilon} \gg 1 \to \text{Conductor}  \quad \wedge \quad \frac{\sigma}{\omega\varepsilon} = \infty \to \text{Conductor perfecto} \\ 
&0.01 < \frac{\sigma}{\omega\varepsilon} < 100 \to \text{Cuasiconductor} \\
& \frac{\sigma}{\omega\varepsilon} \ll 1 \to \text{Dieléctrico} \quad \wedge \quad \frac{\sigma}{\omega\varepsilon} = 0 \to \text{Dieléctrico perfecto}
\end{align*}
$$
### Variación temporal lenta
Si la excitación es armónica, todos los campos dependerán del tiempo como $e^{j\omega t}$
$$
\nabla \times B(\vec{r},t) = \mu_{0}\vec{J}(\vec{r},t)+j \frac{\omega}{c{^{2}}}\vec{E}(\vec{r},t)
$$
La variación temporal lenta implica un retardo despreciable, o sea, asumimos propagación instantánea: $c \to \infty$.

Esta restricción se puede cumplir si la dimensión lineal del circuito es mucho menor que la longitud de onda en el vacío asociada a la frecuencia de la fuente:
$$
L_{max} < \frac{\lambda}{10}
$$
El tiempo empleado en recorrer la mayor distancia sería $t_{max}= \frac{L_{max}}{c_{0}}$. La variación de fase de las fuentes en ese tiempo será $\omega t_{max} = \frac{\omega L_{max}}{c_{0}}$. Por lo tanto, se podrá despreciar el retardo si $\omega t_{max} \ll 2\pi$, es decir:
$$
L_{max} \ll \frac{c_{0}}{f} = \lambda_{0}
$$
Como el retardo es despreciable el campo varía instantáneamente de la misma forma que las fuentes.
$$
\begin{align}
& \vec{B}(\vec{r},t) = \frac{\mu_{0}}{4\pi} \int_{V'} \frac{\vec{J}(\vec{r}',t)\times (\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^{3}}  \, dv' \\ 
& \vec{E}(\vec{r},t) = \frac{1}{4\pi\varepsilon_{0}} \int_{V'} \frac{\rho(\vec{r}',t)\cdot(\vec{r}-\vec{r}')}{|\vec{r}-\vec{r}'|^{3}}  \, dv' 
\end{align}
$$
Como el rotor del campo eléctrico no es nulo, entonces:
$$
\vec{E}(\vec{r},t) = -\nabla V(\vec{r},t) - \frac{\partial \vec{A}(\vec{r},t)}{\partial t}
$$
#### Densidad de corriente de desplazamiento en conductores
En un conductor, se cumple que:
$$
\nabla \times \vec{H} \simeq \vec{J}
$$
Donde vale que $\nabla\cdot(\nabla \times \vec{H}) = \nabla\cdot \vec{J} = 0$. A partir de esta expresión, la ecuación general para la distribución de corriente variable con el tiempo en un material conductor queda tal que:
$$
\nabla^{2}\vec{J}=\sigma \mu  \frac{\partial \vec{J}}{\partial t}
$$
#### Ecuación de difusión
Sea $\vec{J}=\sigma \vec{E}$, entonces:
$$
\nabla^{2} \vec{E}= j\omega \sigma \mu_{0}\vec{E}
$$
#### Profundidad de penetración
Es la medida desde la superficie para la cual $J$ se reduce a $\frac{1}{e}$ de su valor en la superficie.

Para un conductor, la profundidad de penetración está dada por:
$$
\delta = \frac{1}{\sqrt{ \pi f\mu \sigma }}
$$
### Impedancia
Se define la impedancia como:
$$
Z = \frac{\Delta V}{I} = \frac{\int\vec{E}\cdot d\vec{l}}{I}
$$
En cambio, la impedancia por unidad de longitud será:
$$
Z_{l} = \frac{\Delta V}{I} = \frac{E(a)}{I} = \frac{E_{z}(a)}{I_{0}} = \frac{k}{2\pi a\sigma} \frac{J_{0}(ka)}{J_{1}(ka)} = R+jX
$$
#### Resistencia
- En CC: $\omega\to 0 \, , \, k\to 0 \, , \, J_{0}(0)=1 \, , \, J_{1}(ka)= \frac{ka}{2}$
$$
\frac{R}{l} = \frac{1}{(\pi a{^{2}})\sigma}
$$
- En alta frecuencia: $\omega\to \infty \, , \, |k|a\to \infty$
$$
\frac{R}{l} = \frac{1}{(2\pi a\delta)\sigma} \qquad a\gg \delta
$$
#### Impedancia interna y externa

Sea $Z = Z_i + Z_e \quad\quad Z_i : \text{impedancia interna} \quad Z_e : \text{impedancia externa}$
$$Z_i = R_{cc}\, \frac{\tfrac{ka}{2} J_0(ka)}{J_1(ka)} = R + jX 
\quad\quad ka = j^{3/2}\sqrt{2}\frac{a}{\delta} 
\quad\quad \delta = \frac{1}{\sqrt{\pi f \mu \sigma}}
$$
$$Z_e = jX_{ext} = j 2 \pi f L_{ext}$$
Para **baja frecuencia**, los 3 primeros términos del desarrollo de $Z_i$:
$$\frac{ka}{2} \frac{J_0(ka)}{J_1(ka)} = 1 - \tfrac{1}{8}(ka)^2 - \tfrac{1}{192}(ka)^4
= 1 - \tfrac{j}{4}\left(\tfrac{a}{\delta}\right)^2 - \tfrac{1}{192}\left(\tfrac{a}{\delta}\right)^4
$$
$$Z_i = R_{cc} \left( 1 + \tfrac{j}{4}\left(\tfrac{a}{\delta}\right)^2 + \tfrac{1}{48}\left(\tfrac{a}{\delta}\right)^4 \right)
\quad \begin{cases} 
R_{bf} = R_{cc} \left( 1 + \tfrac{1}{48}\left(\tfrac{a}{\delta}\right)^4 \right) \propto f^2 \\[1em] 
L_i = \frac{\text{Im}(Z_i)}{\omega} = \frac{\mu_0}{8\pi} l = 50 \, \text{nH}\cdot l 
\end{cases}$$
$$\frac{J_0(ka)}{J_1(ka)} = -j 
\quad\quad 
ka = j^{3/2}\sqrt{2}\frac{a}{\delta} 
\quad\quad 
\delta = \frac{1}{\sqrt{\pi f \mu \sigma}}$$
$$Z_i = R_{cc}\, \frac{\tfrac{ka}{2} J_0(ka)}{J_1(ka)} 
\;\;\longrightarrow\;\; 
\frac{R_{cc}}{2} \frac{a}{\delta} (1 + j) \quad \begin{cases} 
R_{af} = \frac{R_{cc}}{2}\frac{a}{\delta} = \frac{l}{2 \pi a \delta \sigma} \;\;\propto \sqrt{f} \\[1em] 
L_i = \frac{R_{cc}\,a}{2 \omega \delta} \;\;\propto \frac{1}{\sqrt{f}} \quad;\;\; X \propto \sqrt{f} 
\end{cases}$$
$$\text{Generalmente } L_{ext} \gg L_i \;\;\therefore\; X \propto f$$
### Método de las aproximaciones sucesivas
Cuando los campo EM varían lentamente en el tiempo, las derivadas temporales son pequeñas. Por lo tanto, se pueden desarrollar los campos en serie de potencias de $\omega$, tal que:
$$
\vec{E}=\vec{E}^{(0)} + \vec{E}^{(1)} + \vec{E}^{(2)} + \dots
$$
- Aproximación a orden 0:
Cuando se desprecian las derivadas temporales se tienen los casos estacionarios:
$$
\begin{split}
&\nabla \times \vec{E}^{(0)} = 0 \\ 
&\nabla \times \vec{H}^{(0)} = \vec{J}^{(0)} \\ 
&\nabla \cdot \vec{D}^{(0)} = \rho^{(0)} \\
&\nabla \cdot \vec{B}^{(0)} = 0
\end{split}
$$
- Generalizando para orden n:
$$
\begin{split}
&\nabla \times \vec{E}^{(n)} = -\frac{\partial \vec{B}^{(n-1)}}{\partial t} \\ 
&\nabla \times \vec{H}^{(n)} = \vec{J}^{(n)} + \frac{\partial \vec{D}^{(n-1)}}{\partial t} \\ 
&\nabla \cdot \vec{D}^{(n)} = \rho^{(n)} \\
&\nabla \cdot \vec{B}^{(n)} = 0
\end{split}
$$
Los campos exactos son la suma de los campos correspondientes a cada aproximación:
$$
\vec{E}(\vec{r},t) = \sum_{i=1}^{n} \vec{E}^{(i)}(\vec{r}) e^{j\omega t} \quad
\vec{H}(\vec{r},t) = \sum_{i=1}^{n} \vec{H}^{(i)}(\vec{r}) e^{j\omega t} \quad
\vec{J}(\vec{r},t) = \sum_{i=1}^{n} \vec{J}^{(i)}(\vec{r}) e^{j\omega t} \quad
\rho(\vec{r},t) = \sum_{i=1}^{n} \rho^{(i)}(\vec{r}) e^{j\omega t}
$$
Las condiciones de contorno se deben cumplir para cada orden de la aproximación correspondiente:
$$
D_{2n}^{(k)} - D_{1n}^{(k)} = \rho_{s}^{(k)}
$$
#### Aproximación electrocuasiestática y magnetocuasiestática
Por aproximacón electrocuasiestática:
$$
\text{ECE: } \qquad \frac{\partial \mu_{0}H(\vec{r},t)}{\partial t} \simeq 0 \to \nabla \times \vec{E}(\vec{r},t) = 0
$$
Por aproximacón magnetoestática:
$$
\text{MCE: } \qquad \frac{\partial \varepsilon_{0}\vec{E}}{\partial t} \ll \vec{J}(\vec{r},t) \to \nabla \times \vec{H}(\vec{r},t) = \vec{J}(\vec{r},t) 
$$
Las leyes cuasiestáticas se obtienen de las ec. de Maxwell, despreciando la inducción magnética ($\frac{\partial B}{\partial t}$), o las corrientes de desplazamiento ($\frac{\partial D}{\partial t}$), pero no las dos al miemo tiempo.

Para determinar si un sistema es ECE o MCE, se debe hacer tender $\omega\to 0:$
- Si $B\to 0$ en el limite, el sistema es ECE.
- Si $E\to 0$ en el limite, el sistema es MCE.

![[Pasted image 20250915175325.png#center]]
#### Error en emplear la aproximación cuasiestática
$$
\text{ECE: } \qquad \int_{C} \vec{E}_{error}\cdot d\vec{l} = - \frac{d}{dt} \left(  \int_{S} \vec{B}\cdot d\vec{A} \right) \to \frac{E_{error}}{E} = \omega{^{2}}\mu \varepsilon L^{2} 
$$
$$
\text{MCE: } \qquad \int_{C} \vec{H}_{error}\cdot d\vec{l} = - \frac{d}{dt} \left(  \int_{S} \varepsilon\vec{E}\cdot d\vec{A} \right) \to \frac{H_{error}}{H} = \omega{^{2}}\mu \varepsilon L^{2} 
$$
Para que el error en utilizar cualquiera de las aproximaciones sea pequeño, se requiere:
$$
\omega^{2}\mu\varepsilon L^{2} \ll 1 \to \omega L \ll \frac{1}{\sqrt{ \mu\varepsilon }}
$$
Sea $c= \frac{1}{\sqrt{ \mu\varepsilon }}$, $\frac{L}{c}$ es el tiempo que demora una onda EM que se propaga con velocidad $c$ en recorrer la distancia $L$. Se debe cumplir que:
$$
\frac{L}{c} \ll T \quad \wedge \quad T_{onda \, EM} \ll T
$$
### Corrientes de Foucault
Las corrientes inducidas son generadas en un conductor por un campo magnético variable en el tiempo.

**Obs:** Las corrientes de Foucault generan un campo magnético “secundario” que tiende a oponerse al campo magnético generado por la bobina (“primario”) *Ley de Lenz*.

**Ventajas:** 
- No requiere el uso de líquidos de acoplamiento. 
- Además de encontrar las grietas, las corrientes de Foucault también se pueden utilizar para comprobar: 
	- Dureza del metal 
	- Conductividad. 
**Desventajas:** 
- Los ensayos por corrientes de Foucault se limitan a los materiales conductores y por tanto no puede ser empleados en plásticos.

