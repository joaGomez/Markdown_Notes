### Ecuaciones de Maxwell en el vacío
En el vacío, las fuentes $\vec{J}$ y $\rho$ no son consideradas. Buscamos estudiar las propiedades de los campos lejos de las fuentes:
$$
\begin{split}
& \nabla\cdot \vec{E} = \frac{\cancel{\rho}}{\varepsilon_{0}} = 0 \\ 
& \nabla\cdot \vec{B} = 0 \\
& \nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t} \\
& \nabla \times \vec{B} = \mu_{0}\cancel{\vec{J}}+\mu_{0}\varepsilon_{0} \frac{\partial \vec{E}}{\partial t} = \mu_{0}\varepsilon_{0} \frac{\partial \vec{E}}{\partial t}  
\end{split}
$$
### Ecuación de onda en el vacío
$$
\begin{split}
\nabla^{2}\vec{E} = \mu_{0} \varepsilon_{0} \frac{\partial^{2} \vec{E}}{\partial t^{2}} \\ 
\nabla^{2}\vec{H} = \mu_{0} \varepsilon_{0} \frac{\partial^{2} \vec{H}}{\partial t^{2}}
\end{split}
$$
**Observaciones:**
- Las ecuaciones de onda no son independientes, porque se obtuvieron a partir de la ley de Faraday y la ley de Ampere-Maxwell.
- Generalmente se resuelve la ecuación de onda para $E$ y a partir de la ley de Faraday se obtiene $H$.
- Para O. Jefimenko, la propagación de una onda electromagnética es la manifestación de la propagación de los campos eléctricos y magnéticos, ambos originados simultáneamente por cargas y corrientes variables en el tiempo, y cuyas interacciones en el espacio dan lugar al fenómeno ondulatorio que observamos. 
#### Ondas planas
Por simplicidad, sólo se considera una dirección de propagación ($z$) → Un campo $E$ es únicamente función de la coordenada de propagación y del tiempo → **Onda plana**.
$$
E_{x} (z,t) = f(z-ct) + f(z+ct) \quad \text{Sol. de la ec. de onda}
$$
Donde $f$ es una función determinada por la fuente y las condiciones de contorno.

#### Transversalidad
Dada la divergencia de un campo eléctrico:
$$
\nabla\cdot \vec{E}(z,t) = 0 \to \cancel{\frac{\partial E_{x}}{\partial x}} + \cancel{\frac{\partial E_{y}}{\partial y}} + \frac{\partial E_{z}}{\partial z} = 0 \to \frac{\partial E_{z}}{\partial z} = 0
$$
En consecuencia, la componente del campo eléctrico en $z$ depende únicamente del tiempo.

Como esta solución debe cumplir con la ec. de onda, la única forma que se cumpla matemáticamente es que $E_{z}$ crezca indefinidamente en el tiempo, lo cual es físicamente imposible. Por lo tanto, vamos a considerar que la componente del campo eléctrico en la dirección de propagación es nula.

Se obtiene el mismo resultando partiendo de la ec. de la divergencia de $H$, entonces, sienfo $z$ la dirección de propagación:
$$
E_{z} = 0 \quad \wedge \quad H_{z} = 0
$$

#### Ondas monocromáticas o armónicas
Dada la solución para la ec. de onda, se propone una solución armónica en el tiempo, tal que:
$$
\vec{E}(z,t) = \vec{E}(z)e^{j\omega t}
$$
Para un oscilador armónico, donde $k = \frac{\omega}{c}:$
$$
\begin{split}
& \text{Sol. espacial: } \quad & \vec{E}(z) = \vec{E}_{0} e^{\mp jkz}\\
& \text{Sol. total: } & \vec{E}(z,t) = \vec{E}_{0} e^{j(\omega t\mp kz)}
\end{split}
$$
Un caso particular de funciones que satisfacen la ec. de ondas son las funciones armónicas:
$$
f(z\mp ct) = A \cos (k(z\mp ct)) \quad \vee \quad  f(z\mp ct) = A\, sen (k(z\mp ct))
$$
- Período espacial:
$$
f(z\mp ct) = A \cos(k(z+\lambda\mp ct))
$$
Donde $k= \frac{2\pi}{\lambda}$ es el número de onda.
- Período temporal:
$$
f(z\mp ct) = A \cos(k(z\mp c(t+T)))
$$
Donde $T = \frac{2\pi}{kc}= \frac{\lambda}{c}$ es el período.
#### Planos de fase constante
La representación fasorial de un campo está dada por:
$$
\vec{E}(z,t) = \mathrm{Re}(E_{0}\hat{a}_{0}e^{j(\omega t-kz)})
$$
Donde la fase será constante si:
$$
\omega t-kz = cte \to z = \frac{\omega t-cte}{k}
$$
Se puede demostrar, derivando la expresión en función del tiempo, que la velocidad de fase está dada por:
$$
v_{p} = \frac{dz}{dt} = \frac{\omega}{k} = \frac{1}{\sqrt{ \mu_{0}\varepsilon_{0} }}
$$
### Ondas en medios materiales
En un dieléctrico perfecto, si el medio es L.I.H, se reemplaza la permeabilidad y la permitividad en el vacío por la del medio, tal que:
$$
\begin{split}
& k = \omega \sqrt{ \mu\varepsilon } \\ 
& v= \frac{c_{0}}{\sqrt{ \varepsilon_{r}\mu_{r} }} \simeq \frac{c_{0}}{\sqrt{ \varepsilon_{r} }}
\end{split}
$$
