La polarización se define como el lugar geométrico de la punta del vector campo eléctrico observado a lo largo del tiempo en un punto fijo en el espacio en un plano ortogonal a la normal de la onda.
![[Pasted image 20251104125017.png#center]]

El plano que contiene el campo eléctrico define la polarización de la onda electromagnética.

![[Pasted image 20251104125143.png]]

**Obs:**
- Plano de polarización $\perp$ Frente de onda.
- Las polarizaciones ortogonales no interfieren entre sí.
- La reflexión/transmisión en incidencia oblicua depende de la polarización de la onda incidente. 
- La polarización se vuelve crucial al analizar dispositivos a escala de longitud de onda.

Existen tres tipos de polarización:
![[Pasted image 20251104125436.png#center]]

#### Polarización lineal:
Una onda electromagnética cuyo lugar geométrico de la punta del vector de campo eléctrico es una línea recta en un plano ortogonal a la dirección de propagación de la onda. 
$$
\begin{split}
\text{Si } E_{0x} = 0 \to \begin{cases}
E_{y} = E_{0y}\cdot \cos(\omega t+\phi_{y})  \\
E_{x} = 0
\end{cases} \\
\text{Si } E_{0y} = 0 \to \begin{cases}
E_{y} = 0 \\
E_{x} = E_{0x}\cdot \cos(\omega t+\phi_{x})
\end{cases}
\end{split}
$$
![[Pasted image 20251104125806.png]]
#### Polarización lineal oblicua
Dos ondas planas armónicas ortogonales, con la misma frecuencia y diferencia de fase constante. Para este caso, se cumple que:
$$
\delta = \pm n\pi, \, n=0,1 \qquad E_{0x} \neq 0 \, \wedge \, E_{0y} \neq 0 \to \left( \frac{E_{x}}{E_{0x}} +\pm \frac{E_{y}}{E_{0y}} \right)^{2}=0 
$$
![[Pasted image 20251104145220.png]]
$$
E_{y} = \pm \frac{E_{0y}}{E_{0x}}E_{x} \qquad \psi = tg^{-1}\left( \frac{E_{0y}}{E_{0x}} \right)
 \quad \to \quad \vec{E}=E_{0}(\cos \theta \hat{x} + sen \theta \hat{y})\cdot e^{j(\omega t-kz)}
$$
#### Polarización circular
En este caso, se cumple que:
$$
\delta=\pm \frac{\pi}{2} \qquad E_{0x}=E_{0y}=E_{0}
$$
Donde $E_{x}^{2}+E_{y}^{2}=E_{0}^{2}$

Si se propaga en sentido horario:
$$
\delta = - \frac{\pi}{2} \to 
\begin{cases}
E_{x}=E_{0}\cos(\omega t)  \\
E_{y} = E_{0} \cos\left( \omega t- \frac{\pi}{2}\right) = E_{0} sen(\omega t)
\end{cases}
$$
![[Pasted image 20251106095153.png]]
$$
\vec{E} = E_{0} (\hat{x}-j\hat{y})e^{j(\omega t-\beta z)}
$$
Si se propaga en sentido antihorario:
$$
\delta = \frac{\pi}{2} \to 
\begin{cases}
E_{x}=E_{0}\cos(\omega t)  \\
E_{y} = E_{0} \cos\left( \omega t+ \frac{\pi}{2}\right) = -E_{0} sen(\omega t)
\end{cases}
$$
![[Pasted image 20251106095315.png]]
$$
\vec{E} = E_{0} (\hat{x}+j\hat{y})e^{j(\omega t-\beta z)}
$$
La condición necesaria y suficiente para polarización circular son: 
- El campo debe tener dos componentes ortogonales con polarización lineal. 
- Las dos componentes deben tener el mismo módulo. 
- Las dos componentes deben tener una diferencia de fase de múltiplos impares de 90°. 

Se define la razón axial como:
$$
RA = \pm \frac{E_{max}}{E_{min}}
$$
#### Polarización elíptica
Sea $\delta = \phi_{q}- \phi_{p}$ y $a_{p}$ y $a_{q}$ tal que su parte real es positiva o igual a cero:
$$
\vec{E} = (a_{p}\hat{p}e^{j\phi_{p}}+a_{q}\hat{q}e^{j\phi_{q}})\cdot e^{j(\omega t-\vec{k}\cdot \vec{r})}
$$
Con la dirección determinada por: $\hat{p}\times \hat{q}=\hat{k}$
$$
\begin{aligned}
\sin(\delta) > 0 &\Longrightarrow \frac{d\varphi}{dt} < 0 \Longrightarrow \varphi \text{ decrece} \Longrightarrow \boxed{\textbf{P.E. Izquierda}} \\[8pt]
\sin(\delta) < 0 &\Longrightarrow \frac{d\varphi}{dt} > 0 \Longrightarrow \varphi \text{ aumenta} \Longrightarrow \boxed{\textbf{P.E. Derecha}}
\end{aligned}
$$
### Esfera de Poincare
El estado de polarización (P) de una onda se puede representar como un punto sobre la superficie de una esfera.
- Las polarizaciones lineales se encuentran sobre el ecuador.
- Las polarizaciones circulares se encuentran en los polos.
- Las polarizaciones elípticas se encuentran entre los polos y el ecuador.
- Hemisferio Norte: izquierda. Hemisferio Sur: derecha. 

**Obs:** Una onda no polarizada es una onda donde todas las direcciones para el campo eléctrico $E$ son igualmente probables.