### Radiopropagación troposférica
Tanto la presión como la temperatura decrecen con la altura. A la hora de aplicar las leyes de Snell, se debe tener en cuenta como varía el coeficiente de reflexión ante estos cambios en la atmósfera.

Dado que n decrece con la altura, la velocidad aumenta, y el frente de onda se curva debido a esto. Por ello, la trayectoria del rayo entre antenas es curva debido a que el índice de refracción varía con la altura. La curvatura del rayo está determinada por el gradiente vertical del índice de refracción.
![[Pasted image 20251115195832.png#center|300]]
Al aumentar la frecuencia, estas condiciones se hacen más notorias con la distancia.
### TART
#### Dieléctrico
Se considera un índice de refracción complejo, tal que:
$$
n_{c} = n -jk \qquad \frac{\varepsilon'}{\varepsilon_{0}} = n^{2}-k^{2} \qquad \frac{\varepsilon''}{\varepsilon_{0}}=2nk
$$
Por lo tanto
$$
n = \frac{1}{\sqrt{ 2 }} \sqrt{ \varepsilon'+\sqrt{ \varepsilon'^{2}+\varepsilon''^{2} } } \qquad k= \frac{1}{\sqrt{ 2 }}\sqrt{ -\varepsilon'+\sqrt{ \varepsilon'^{2}+\varepsilon''^{2} } }
$$
El campo será
$$
\vec{E} = \vec{E}_{0}e^{-\alpha z}e^{j(\omega t-\beta z)}
$$
Donde $\alpha=k_{0}k$, y $\beta=k_{0}n$.

Según Lorentz, este problema puede ser análogo a un oscilador armónico, donde dependiendo del valor de la frecuencia, el dieléctrico se comportará distinto, debido a su índice de refracción complejo:
$$
\begin{align}
& \text{Transmisión} \qquad & \omega<\omega_{0}- \frac{\Gamma}{2} \\
& \text{Absorción} & \omega_{0}-\frac{\Gamma}{2} <\omega <\omega_{0}+\frac{\Gamma}{2} \\
&\text{Reflexión} & \omega_{0}+\frac{\Gamma}{2}<\omega<\omega_{p}  \\
& \text{Transmisión} & \omega>\omega_{p}
\end{align}
$$
#### Metales
Dado las pérdidas → $\Gamma \neq 0$.
$$
\begin{align}
& \text{Absorción} & 0 <\omega < \Gamma \\
&\text{Reflexión} & \Gamma < \omega < \omega_{p}  \\
& \text{Transmisión} & \omega>\omega_{p}
\end{align}
$$
#### Plasma
El plasma es un gas ionizado que consiste en iones y electrones libres de moverse. Generalmente es de interés el movimiento electrónico y entonces un plasma se puede modelar como ($B_{ext}=0$):
$$
\frac{d^{2}x}{dt} + \Gamma  \frac{dx}{dt} = \frac{e}{m}E(t)
$$
El factor $\Gamma$ tiene en cuenta la pérdida de energía de los electrones móviles por radiación electromagnética o colisiones con los iones positivos del gas.

Se denomina **frecuencia del plasma** → $\omega_{p}^{2} = \frac{Ne^{2}}{\varepsilon_{0}m_{e}} = 3170\cdot N$, donde $N$ es la densidad electrónica por unidad de volumen.

Si $\omega \gg \Gamma$ se considera plasma frío, y no existen pérdidas → $\varepsilon_{p} = \varepsilon_{0}\left( 1-\left( \frac{\omega_{p}}{\omega} \right)^{2} \right)$, y $k=\omega \sqrt{ \mu_{0}\varepsilon_{p} } = \frac{\omega}{v_{p}} = \frac{\omega}{c_{0}}n_{p} = k_{0}n_{p}$

Si $\omega<\omega_{p}$ → $\varepsilon < 0 :n_{rp}=-jk$ → Hay reflexión total interna → Onda evanescente.

Si $\omega>\omega_{p}$ → $\varepsilon>0:n_{p} =n$ → Hay propagación a través del plasma.
### Radiopropagación ionosférica
Es un medio muy inestable → No se puede utilizar la misma frecuencia a lo largo del año, ni a lo largo del día
#### Velocidad de fase y grupo
La ionosfera se comporta como un medio de propagación dispersivo. Las velocidades de fase y de grupo son funciones de la frecuencia y la altura, ya que el índice de refracción lo es: 
$$
v_{p} = \frac{c_{0}}{n} \geq c_{0} \qquad v_{g} = c_{0}n_{i} \leq c_{0}
$$
#### Refracción ionosférica
Se alcanza una trayectoria horizontal (retorno a Tierra) cuando $\phi_{i}=90°$ (reflexión total interna), altura máxima:
$$
n_{i} = sen\phi_{0} = \sqrt{ 1 - \frac{f_{p}^{2}}{f^{2}} } \to \frac{f_{p}}{f} = \cos \phi_{0}
$$
MUF es la frecuencia más elevada en que una onda radioeléctrica puede propagarse entre determinadas estaciones terminales, en un momento dado, mediante refracción ionosférica solamente:
$$
MUF_{i} = f_{max,i} = f_{p}\,sec(\phi_{0})
$$
Cuanto mayor sea el ángulo de disparo, menor es la MUF.
#### Trazado de rayos
Los electrones libres en la ionosfera provocan la refracción de las señales en la banda de HF y eventualmente las refractan hacia la superficie terrestre. 