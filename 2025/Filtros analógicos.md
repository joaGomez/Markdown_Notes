Un filtro es un sistema que permite atenuar frecuencias en un rango selectivo.

Se puede describir cualquier sistema con la siguiente expresión:
$$a_{0}V_{i}(s)+a_{1} \frac{dV_{i}(s)}{dt}+ a_{2} \frac{d^{2}V_{i}(s)}{dt^{2}}+...=b_{0}V_{o}(s)+b_{1} \frac{dV_{o}(s)}{dt}+ b_{2} \frac{d^{2}V_{o}(s)}{dt^{2}}+...$$
Por Laplace → Trabajo en el dominio de la frecuencia:
$$a_{0}V_{i}(s)+a_{1} V_{i}(s) \cdot s+ a_{2} a_{1} V_{i}(s) \cdot s^{2}+...=b_{0}V_{o}(s)+b_{1} V_{o}(s) \cdot s+ b_{2} V_{i}(s) \cdot s^{2}+...$$
Se define la ganancia ($G$) como:
$$G= \frac{V_{o}}{V_{i}}(s)= \frac{a_{0}+a_{1}+a_{2}+...}{b_{0}+b_{1}+b_{2}+...}$$
Propiedades:
- Linealidad: Hay R, C y OA (Coeficientes).
- Tiempo invariante: Los valores de los componentes no varian con el tiempo.
- Causalidad.
- Estabilidad: input acotado → Output acotado. $Re(Polos)<0$.
- La respuesta en frecuencia debe ser acotada. $$\begin{cases}  
\lim_{s\to 0} |G(s)|<\infty \quad \text{Acotado}\\
\lim_{s\to \infty} |G(s)|<\infty \quad \text{Acotado}\\   
\end{cases}$$
- Se debe cumplir: $G(s)_{j\omega}=G^{*}(-s)_{j\omega}$ → Coeficientes reales. $$\begin{split}
|G(s)|_{j\omega}=|G(-s)|_{j\omega} \qquad \text{Módulo par} \\
\angle G(s)_{j\omega} = - \angle G(-s)_{j\omega} \qquad \text{Fase impar}
\end{split}$$
**Obs:** Con estas observaciones, un pasabajos es como un pasabanda:
![[Pasted image 20240911213047.png#center]]

### Plantilla normalizada
![[Pasted image 20240911213203.png#center|400]]

Para utilizar funciones de aproximación, se propone $F^{2}(\omega)=|G(s)|^{2}_{j\omega}$. Donde $|G(s)|^{2}_{j\omega}\bigg{|}_{\omega = \frac{s}{j}}= H(s)$.
$$F{^{2}}(\omega)= \frac{1}{1+\xi^{2}y^{2}}$$
Donde $y$ será la función de aproximación utilizada.

![[Pasted image 20241002101030.png#center]]
Para este caso, $F(\omega) = |H_{1}(s)|_{j\omega}$ cumple con la plantilla.

La función de aproximación de Butterworth es $y{^{2}}=\omega^{n}$.

##### Ejercicio
![[Pasted image 20241002101448.png#center]]
![[Pasted image 20241002101518.png#center]]
### Desnormalización
Para desnortmalizar, se deben realizar transformaciones en el argumento de la función.

Si quiero un filtro pasabajos no normalizado, donde tenga $\omega_p$ y $\omega_a$ no normalizadas, la transformación será:
$$T(s) = \frac{s}{\omega_{p}} \Rightarrow H_{LP}(s)=H_{n}(T(s))=H_{n}\left(\frac{s}{\omega_{p}}\right) \qquad \text{Transformación pasabajos}$$
Donde $\omega_{an}=T(j\omega_{a})=j \frac{\omega_{a}}{\omega_{n}}$.
$$T(s) = \frac{\omega_{p}}{s} \Rightarrow H_{HP}(s)=H_{n}(T(s))=H_{n}\left(\frac{\omega_{p}}{s}\right) \qquad \text{Transformación pasaaltos}$$
$$T_{1}(s) = \frac{s}{B},~ T_{2}(s)= \frac{s^{2}+\omega^{2}_{0}}{s}\Rightarrow H_{BP}(s)=H_{n}(T_{1}(T_{2}(s))) = H_{n}\left(\frac{s^{2}+\omega^{2}_{0}}{B\cdot s}\right) \qquad \text{Transformación pasabanda}$$
$$T_{1}(s) = \frac{1}{s},~ T_{2}(s)= \frac{s^{2}+\omega^{2}_{0}}{B\cdot s}\Rightarrow H_{BP}(s)=H_{n}(T_{1}(T_{2}(s))) = H_{n}\left(\frac{B\cdot s}{s^{2}+\omega^{2}_{0}}\right) \qquad \text{Transformación rechazabanda}$$
#### Funciones de Chebyshev
##### Primera aproximación
$$F(\omega)=cos(N\cdot Arcos(\omega))$$
- Oscilaciones en banda pasante
- Mínimo orden
- Pendiente: $-20\cdot N~ dB/dec$
- Distorsión de fase en banda pasante
- Polos de alto Q
![[Pasted image 20241002104438.png#center]]
##### Segunda aproximación
$$H^{2}_{CH2}=1-H^{2}\left(\frac{1}{\omega}\right) = \frac{\xi^{2}T^{2}_{n}(\frac{1}{\omega})}{1+\xi^{2}T^{2}_{n}(\frac{1}{\omega})}$$
Donde $\xi^{2} = \frac{1}{G^{2}_{p}}$, y $T^{2}_{n}(\omega_{a})= \frac{\frac{1}{G^{2}_{a}}-1}{\frac{1}{G^{2}_{p}}-1}$ (Condición para que sirva un orden N).
![[Pasted image 20241002105510.png#center]]

**Obs:** Se puede demostrar que CH1 y CH2 son del mismo orden utilizando:
$${G'_{p}}{^{2}}= 1 - G^{2}_{a} \qquad \wedge \qquad {G'_{a}}{^{2}}= 1 - G^{2}_{p}$$
