### Sistemas de coordenadas

![[Pasted image 20250805100637.png#center|500]]

Ejemplo: Vector posición

![[Pasted image 20250805100754.png#center|500]]

**Definición:** Un campo es una función que asigna a cada punto del espacio un valor de una propiedad física o matemática.

- Campos escalares: Su dominio es $\mathcal{R}{^{3}\to}\mathcal{R}$, por lo que para cada punto, se le asigna un valor escalar.

![[Pasted image 20250805122313.png#center|200]]

- Campos vectoriales: Su dominio es $\mathcal{R}{^{3}\to}\mathcal{R}^{3}$, por lo que para cada punto, se le asigna un valor vectorial.

![[Pasted image 20250805122339.png#center|180]]

### Líneas de campo
Las líneas de campo se definen como las curvas tangentes a cada punto en un campo vectorial.


![[Pasted image 20250805122606.png#center|200]]

### Gradiente
Sea $f(r)$ un campo escalar diferenciable, el gradiente de $f(r)$ es un campo vectorial que se define a través del cambio de la función en un desplazamiento diferencial:
$$\vec{\nabla} = \frac{\partial}{\partial x}\hat{i} + \frac{\partial}{\partial y}\hat{j}+\frac{\partial}{\partial z}\hat{k} \Rightarrow grad(f)=\nabla f$$
El gradiente mide la tasa y la dirección del cambio en un campo escalar.
### Flujo de un campo vectorial
$$\text{Flujo elemental:} \qquad \qquad d\phi = \vec{A}(P).d \vec{S}=|\vec{A}(P) | ~dS \cos(\theta)$$
El flujo de un campo vectorial a través de una superficie (abierta o cerada) se define como la integral donde el integrando es la proyección del campo vectorial sobre la normal a la superficie punto a punto de la misma.
$$\phi_{\Sigma} = \int_{\Sigma} \, d\phi = \int_{\Sigma} |\vec{A}(P)|.d\vec{S} $$
### Divergencia
La divergencia de $A$ es el flujo de $A$ por unidad de volumen en torno del punto $P$.
$$div(\vec{A}(P)) = \lim_{ \Delta \tau \to 0}\frac{1}{\Delta \tau} ∯_{S(\Delta \tau)} \vec{A}.d\vec{S} $$
La divergencia mide la tendencia de un campo vectorial a originarse o converger hacia ciertos puntos. La divergencia de un campo vectorial es un campo escalar.

![[Pasted image 20250806120032.png#center|300]]
$$\text{Teorema de la divergencia:} \qquad \qquad ∯_{S} \vec{A} . d\vec{S} = \iiint_{\tau} (\nabla . \vec{A}) dV$$
### Circulación
La circulación de un campo vectorial a lo largo de una curva c (abierta o cerrada) en el espacio es una integral de línea cuyo integrando es la proyección del campo vectorial sobre el elemento de arco punto a punto a lo largo de la línea.
$$
\text{Sea C la curva que circula en sentido A → B:} \qquad \int_{C} \vec{F}.d\vec{l} 
$$
#### Curva cerrada
La circulación a lo largo de una curva cerrada es una medida de la rotación de un campo.
$$
C = \oint_{\Gamma} \vec{F}.d\vec{l}
$$
![[Pasted image 20250806120856.png#center|300]]
### Rotor
El rotor mide la tendencia de un campo vectorial a rotar alrededor de un punto. La dirección indica el eje de rotación.
$$
\nabla \times \vec{A}(P) = \lim_{ \Delta V \to 0 } \frac{1}{\Delta V} \left(\oint_{C}d\vec{S} \times \vec{A}\right)
$$
El rotor de un campo vectorial es otro campo vectorial.

![[Pasted image 20250806123909.png#center|400]]

Si el rotor es nulo en todo el dominio, el campo es **irrotacional**.
### Teorema de Stokes
Dada una superficie de borde C, la circulación de un campo a lo largo del borde es igual al flujo del rotor del campo a través de la superficie S.
$$
\iint_{S} (\nabla \times \vec{F}) . d\vec{S} = \oint_{C} \vec{F}.d\vec{l}
$$
*Donde S es un superficie abierta que se ‘apoya’ en C*.
#### Corolarios
- Solo depende del contorno y no de la superficie que se apoya sobre el mismo.
- Para una superficie cerrada: $∯_{S} (\nabla \times \vec{F}) . d\vec{S} = 0$
### Teorema de Helmholtz
Sea $F(r)$ un campo vectorial con fuentes escalares $g(r)$ y fuentes vatoriales $Z(r)$:
$$
\begin{split}
&\nabla.\vec{F} = g(\vec{r}) \qquad \qquad &\text{Fuentes escalares} \\ 
&\nabla \times \vec{F} = \vec{Z} (\vec{r})  & \text{Fuentes vectoriales} 
\end{split}
$$
Se deben cumplir las siguientes condiciones:
1) $F(r)$ tiende a cero en el infinito al menos como $\frac{1}{r{^2}}$
2) Las fuentes, son nulas fuera de un volumen V finito y contenido en una esfera, centrada en el origen, de radio finito $L=r_{max}$.

Si se conocen la divergencia y el rotor del campo vectorial $F(r)$, el campo queda unívocamente determinado.
$$
\text{La solución está dada por:} \quad \vec{F} = -\nabla \phi+\nabla \times \vec{A}  
$$
Donde:
$$
\begin{split}
\phi(\vec{r}) = \frac{1}{4\pi } \int _{esp} \frac{g(\vec{r})}{|\vec{r}-\vec{r}'|} \, dV'  \qquad \text{Potencial escalar} \\ 
\vec{A}(\vec{r}) = \frac{1}{4\pi } \int _{esp} \frac{\vec{Z}(\vec{r})}{|\vec{r}-\vec{r}'|} \, dV' \qquad \text{potencial vectorial}
\end{split}
$$


