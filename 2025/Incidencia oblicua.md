El término de incidencia oblicua se utiliza para referirse al estudio de incidencia de ondas frente a una interfase, con un ángulo de inclinación con respecto al plano de interfase. Es más claro con la siguiente representación gráfica:
![[Pasted image 20251115102135.png]]
Donde el plano de interfase es el plano de sepación entre los dos medios, y el plano de incidencia es el plano que contiene al vector de onda incidente y es normal al plano de la interfase.

Debido a la geometría de la incidencia, se expresa el vector $\vec{k}$ tal que:
$$
\vec{k}= k_{x}\hat{x}+k_{y}\hat{y}+k_{z}\hat{z} \to |\vec{k}| = \sqrt{ k_{x}^{2}+k_{y}^{2}+k_{z}^{2} } = \frac{2\pi}{\lambda}= \omega \sqrt{ \mu\varepsilon }
$$
Sea $\phi$ el ángulo acimutal, y $\theta$ el ángulo de elevación:
$$
k_{x} = k~ sen\theta \cos \phi \quad k_{y} = k~ sen\theta ~sen \phi \quad k_{z} = k \cos \theta
$$
El estudio de los problemas de incidencia oblicua se pueden separar en dos polarizaciones básicas:
- El campo $E$ es perpendicular al plano de incidencia:
En este caso se cumple que $\hat{a}_{TE} = \frac{\hat{z}\times \vec{k}_{inc}}{|\hat{z}\times \vec{k}_{inc}|}$
![[Pasted image 20251115102949.png]]
- El campo $E$ es paralelo al plano de incidencia:
En este caso se cumple que $\hat{a}_{TM} = \frac{\hat{a}_{TE}\times \vec{k}_{inc}}{|\hat{a}_{TE}\times \vec{k}_{inc}|}$
![[Pasted image 20251115103124.png]]

Las ondas incidente, reflejada y transmitida se encuentran en el plano de incidencia.
![[Pasted image 20251115103232.png]]

Además, cualquier onda, con el campo $E$ en cualquier dirección, se puede descomponer en esta base vectorial → $(\hat{a}_{\perp}, \hat{a}_{\parallel})$, de modo que:
$$
\begin{split}
\vec{E} = (E_1 \hat{a}_{\perp} + E_2 \hat{a}_{\parallel})\cdot e^{{[j(\omega t - \vec{k}\cdot\vec{r})]}} \\ 
\vec{H} = \frac{1}{\eta_1} 
\left( \frac{\vec{k}}{|\vec{k}|} \right) \times (E_1 \hat{a}_{\perp} + E_2 \hat{a}_{\parallel})\cdot e^{j(\omega t - \vec{k}\cdot\vec{r})}
\end{split}
$$
A partir de las condiciones de contorno para este escenario, se deducen las leyes de Snell:
$$
\begin{align}
\text{Primera ley} \qquad & \theta_{i} = \theta_{r} \\
\text{Segunda ley} \qquad & n_{1}sen\theta_{1} = n_{2}sen\theta_{2} \to sen \theta_{t} = \frac{n_{1}}{n_{2}}sen\theta_{i}
\end{align}
$$
La segunda ley se puede reescribir a partir de la impedancia intrínseca del medio:
$$
sen\theta_{t} = \frac{\eta_{2}\mu_{1}}{\eta_{1}\mu_{2}} sen\theta_{i}
$$
### Fórmulas de Fresnel
$$
\begin{align}
%% s-polarización (perpendicular)
&\Gamma_{\perp}
\;=\;
\frac{\eta_2\cos\theta-\eta_1\cos\theta_t}
     {\eta_2\cos\theta+\eta_1\cos\theta_t}
\qquad
\;\tau_{\perp}
\;=\;
\frac{2\,\eta_2\cos\theta}
     {\eta_2\cos\theta+\eta_1\cos\theta_t}
\qquad \tau_{\perp}=\Gamma_{\perp}+1 \\
%% p-polarización (paralela)
&\Gamma_{\parallel}
\;=\;
\frac{\eta_2\cos\theta_t-\eta_1\cos\theta}
     {\eta_2\cos\theta_t+\eta_1\cos\theta}
\qquad
\tau_{\parallel}
\;=\;
\frac{2\,\eta_2\cos\theta}
     {\eta_2\cos\theta_t+\eta_1\cos\theta}
\qquad 1+\Gamma_{\parallel}
=\tau_{\parallel}\,\frac{\eta_2\cos\theta_t}{\eta_1\cos\theta}\\
\end{align}
$$
Si $\mu_{1}=\mu_{2}:$
$$
\begin{align}
& \Gamma_{\perp}
= \frac{\cos\theta - \sqrt{\frac{\varepsilon_2}{\varepsilon_1} - \sin^2\theta}}
       {\cos\theta + \sqrt{\frac{\varepsilon_2}{\varepsilon_1} - \sin^2\theta}} 
\qquad & \tau_{\perp}
= \frac{2\cos\theta}
       {\cos\theta + \sqrt{\frac{\varepsilon_2}{\varepsilon_1} - \sin^{2}\theta}} \qquad & \tau_{\perp}=\Gamma_{\perp}+1
\\
& \Gamma_{\parallel}
= \frac{
-\left( \frac{\varepsilon_2}{\varepsilon_1} \right)\cos\theta
    + \sqrt{ \left( \frac{\varepsilon_2}{\varepsilon_1} \right) - \sin^2\theta}
}{
 \left( \frac{\varepsilon_2}{\varepsilon_1} \right)\cos\theta
    + \sqrt{ \left( \frac{\varepsilon_2}{\varepsilon_1} \right) - \sin^2\theta}
} & \tau_{\parallel} = \frac{2 \sqrt{\frac{\varepsilon_1}{\varepsilon_2}} \cos\theta
}{\cos\theta + \sqrt{\frac{\varepsilon_1}{\varepsilon_2}}\,
 \sqrt{1 - \frac{\varepsilon_1}{\varepsilon_2}\sin^{2}\theta}} \qquad & 1 + \Gamma_{\parallel}
= \tau_{\parallel}\,\frac{\cos\theta_t}{\cos\theta}
\end{align}
$$
Siendo $\theta$ el ángulo de incidencia.
#### Ángulo de Brewster
Para la polarización de $E$ paralelo al plano de incidencia, existe la posibilidad que para un determinado ángulo el coeficiente de reflexión sea nulo.
$$
\theta_{B} = \arctan\left( \sqrt{ \frac{\varepsilon_{2}}{\varepsilon_{1}} } \right)
$$
Si $\theta_{i}= \theta_{B} \to \theta_{i}+\theta_{t}= \frac{\pi}{2} \Rightarrow \Gamma_{\parallel}=0$.
Si incide luz no polarizada con el ángulo de Brewster, la luz reflejada está polarizada con $E_{\perp}$ al plano de incidencia.
### Reflexión total interna
Si $\varepsilon_{2}>\varepsilon_{1}$, la onda va de un medio ópticamente menos denso, hacia uno más denso, por lo que la ley de Snell se cumple para todos los ángulos de incidencia.

En cambio, si la relación es al revés, es decir, incide desde un medio ópticamente más denso, hacia uno menos denso ($\varepsilon_{1}>\varepsilon_{2}$), la ley se Snell se cumple hasta un ángulo crítico, tal que $sen^{2}(\theta_{c})= \frac{\varepsilon_{2}}{\varepsilon_{1}}$

Cuando el ángulo de incidencia es el ángulo crítico, el coeficiente de reflexión es máximo → $\Gamma_{\perp}=1$

**Obs:** No existe transferencia de densidad de potencia, en la dirección normal a la interfase.

Si el ángulo de incidencia es mayor al ángulo crítico, no sólo hay reflexión total, sino que el ángulo transmitido se puede expresar como un valor complejo, tal que:
$$
\cos \theta_{t} = \sqrt{ 1-sen^{2}\theta_{t} } = - j A= -j\sqrt{ \frac{\varepsilon_{1}}{\varepsilon_{2}}sen^{2}\theta_{i}-1 }
$$
**Obs:** Las OEM que se propagan con un ángulo complejo son ondas planas no uniformes.
### Reflectividad y transmitividad
$$
\begin{align}
& \text{Reflectividad} \qquad & R= \frac{\langle P^{r} \rangle}{\langle P^{i}\rangle} = |\Gamma|^{2}  \\
& \text{transmitividad} \qquad & T= \frac{\langle P^{t} \rangle}{\langle P^{i}\rangle} = |\tau|^{2} \frac{\eta_{1}\cos \theta_{t}}{\eta_{2}\cos \theta_{i}} 
\end{align}
$$
Se cumple que $R+T=1$.

Para una interfase aire-vidrio:
![[Pasted image 20251115124927.png]]
### Reflexión de una onda no polarizada
Cuando una onda no polarizada se refleja en una superficie no metálica (arena, agua, nieve o el asfalto), la onda reflejada está parcialmente polarizada con $E_{\perp}$ al plano de incidencia. El grado de polarización depende del ángulo de incidencia.
$$
R_{\text{no polarizada}} = \frac{1}{2} (R_{\perp}+R_{\parallel}) \qquad  \wedge \qquad R_{\perp}>R_{\parallel} \qquad \text{Dependen de } \theta
$$
### Interfase dieléctrico-dieléctrico con pérdidas
En este caso, los coeficientes de reflexión serán complejos, debido a las pérdidas en el dieléctrico. Por lo tanto, el coeficiente de reflexión dependerá de lña frecuencia.

**Obs:** En polarización vertical ($TM$), para el ángulo de Brewster, $\Gamma_{TM}$ tiene un mínimo en lugar de un cero.

$$
\text{Ley de Snell:} \qquad \gamma_{1}sen\theta_{i} = \gamma_{2}sen\theta_{t}
$$
### Interfase dieléctrico-conductor
Siempre se cumple que:
$$
\Gamma_{\perp} \simeq -1 \quad \wedge \quad \Gamma_{\parallel} \simeq -1
$$
### Reflexión especular y difusa
**Reflexión especular:** Los rayos inciden sobre una superficie lisa, por lo que los rayos incidentes son paralelos entre sí, y ocurre lo mismo con los rayos reflejados.

**Reflexión difusa:** La superficie no es lisa, por lo que los rayos, tanto incidentes como reflejados, no son paralelos entre sí.

![[Pasted image 20251115130002.png]]
### Cambio de polarización por reflexión y refracción
| Polarización incidente | Polarización reflejada $\theta<\theta_{B}$ | Polarización reflejada $\theta>\theta_{B}$ |
| ---------------------- | ------------------------------------------ | ------------------------------------------ |
| Circular derecha       | Elíptica izquierda                         | Elíptica derecha                           |
| Circular izquierda     | Elíptica derecha                           | Elíptica izquierda                         |
| Elíptica derecha       | Elíptica izquierda                         | Elíptica derecha                           |
| Elíptica izquierda     | Elíptica derecha                           | Elíptica izquierda                         |
