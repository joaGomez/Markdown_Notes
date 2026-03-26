Cantidades fundamentales:

- Sin definición precisa.
- Aparecen en cada campo para describir el universo. (en nuestra percepción de este).
- Masa, longitud, tiempo, carga, temperatura.

Campo: El concepto de campo se puede definir como una región del espacio que comparten propiedades en cada punto de este, como tratamos a las partículas.

Los campos pueden ser escalares, o vectoriales.

Permitividad y permeabilidad: Ambas son propiedades del medio. Cuando el medio es el vacío:
$$
\mu=\mu_{0}=4\pi\cdot10^{-7} \frac{H}{m} (\text{magnetismo}) \qquad 
\varepsilon=\varepsilon_{0}=8.85\cdot 10^{-12} \frac{F}{m} (\text{Electricidad})
$$
Maxwell, a partir de sus ecuaciones, pudo predecir que la velocidad del campo electromagnético en el vacío es igual a $c$ (velocidad de la luz).
$$
c = \frac{1}{\sqrt{ \mu_{0}\varepsilon_{0} }} \left[ \frac{m}{s} \right]
$$
En el estudio del electromagnetismo de desarrollan/trabajan con expresiones en forma diferencial e integral.

**Forma diferencial:** Mayor practicidad/facilidad a la hora de resolver las ecuaciones -> Formamos sistemas de ecuaciones mediante los operadores -> Solución más directa.
$$
Ej. \quad \nabla\cdot \vec{J} = - \frac{\partial p}{\partial t}
$$
**Forma integral:** Mayor facilidad para entender el significado físico de la expresión.
$$
Ej. \quad \oint_{S}\vec{J}\cdot \vec{dS} = - \frac{\partial}{\partial t} \int_{v} \rho \, dv
$$
El pasaje entre una forma a la otra se logra a partir de los teoremas conocidos/trabajados en otros cursos, como el teorema de la divergencia, el teorema de Stokes, entre otros.
### Campo electrostático
$$
\text{Propiedades} 
\begin{cases}
\to \text{Todas las cargas seencuentran fijas en el espacio }v=0 \\
\to \text{Todas las densidades de carga } (\rho) \text{ son ctes en el tiempo } \left( \rho \text{ invariante en el tiempo}: \frac{\partial p}{\partial t}=0 \right) \\
\to \text{Las cargas son las fuentes del campo eléctrico}
\end{cases}
$$
$$

\text{Intereses} 
\begin{cases} 
\to \text{Intensidad del campo eléctrico en cualquier punto} \\
\to \text{Distribución del potencial } \vec{V} \\
\to \text{Fuerza que actúa en una carga por otra carga} \\
\to \text{La distribución de energía electrostática en una región}
\end{cases}
$$
#### Expresiones del campo electrostático
$$
\begin{align}
\vec{F} = q \vec{E} \quad &\text{Ley de Coulomb} \\
\vec{E} = \frac{1}{4\pi\varepsilon} \int_{v} \frac{\rho}{R^{2}\cdot \vec{a}_{R}} dv \quad &\text{Campo eléctrico} \\
\nabla\cdot \vec{D}=\rho \, \vee \, \oint_{S}\vec{D}\cdot \vec{dS} = Q \quad &\text{Ley de Gauss} \\
\nabla \times \vec{E} = 0 \, \vee \, \oint_{c} \vec{E}\cdot \vec{dl} = 0 \quad &\text{Conservación del campo eléctrico} \\
\vec{E}=-\nabla V \, \vee \, V_{ba}=-\int_{a}^{b}\vec{E}\cdot \vec{dl} \quad &\text{Potencial eléctrico} \\
\nabla^{2}V= -\frac{\rho}{\varepsilon} \quad &\text{Ec. de Poisson} \\
\nabla^{2}V=0 \quad &\text{Ec. de Laplace} \\
\vec{D}=\varepsilon \vec{E} \quad &\text{Relación constitutiva} \\
\omega_{e}= \frac{1}{2}\vec{D}\cdot \vec{E}= \frac{\varepsilon}{2}|\vec{E}|^{2} \quad &\text{Densidad de energía eléctrica} \\
\vec{J} = \sigma \vec{E} \quad &\text{Ley de Ohm}
\end{align}
$$

### Campo magnetostático
A diferencia del campo eléctrico, este es producido por corriente cte.
$$

\text{Intereses} 
\begin{cases}
\to \text{Intensidad de campo magnético}  \\
\to \text{Densidad de flujo magnético}  \\
\to \text{Energía almacenada en un campo magnético}
\end{cases}
$$
#### Expresiones del campo magnetostático
$$
\begin{align}
\vec{F}=q\vec{v}\times \vec{B} \, \wedge \, \vec{dF}= i \vec{dl} \times \vec{B} \quad &\text{Ec. de la fuerza magnética} \\
\vec{dB} = \frac{\mu}{4\pi} \frac{i\cdot \vec{dl}\times \vec{a}_{r}}{r^{2}} \quad &\text{Ley de Biot-Savart} \\
\nabla \times \vec{H} = \vec{J} \, \vee \, \oint_{c} = \vec{H}\cdot \vec{dl} = i \quad &\text{Ley de Ampère} \\
\nabla\cdot B=0 \, \vee \, \oint_{S}\vec{B}\cdot \vec{dS} = 0 \quad &\text{Ley de Gauss del magnetismo} \\
\vec{B}=\nabla \times \vec{A} \, \vee \, \vec{A}= \frac{\mu}{4\pi} \int_{c}  \frac{i\cdot\vec{dl}}{r} \quad &\text{Vector de potencial magnético} \\
\Phi = \int_{S} \vec{B}\cdot \vec{dS} = \oint_{c} \vec{A}\cdot \vec{dl} \quad &\text{Flujo magnético} \\
\vec{B} = \mu \vec{H} \quad &\text{Relación constitutiva}  \\
\omega_{m} = \frac{1}{2} \vec{B}\cdot \vec{H}= \frac{\mu}{2} |\vec{H}|^{2} \quad &\text{Densidad de energía magnética} \\
\nabla^{2}\vec{A}=-\mu \vec{J} \quad &\text{Ec. de Poisson}
\end{align}
$$
