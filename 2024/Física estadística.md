Se define $U$ como la energía total del sistema. Si se supone que las partículas interaccionan entre sí (solo lo hacen ligeramente), la energía a cada partícula se le atribuye por otras características, como coordenadas o temperatura.

Sea $N$ el número de partículas en total del sistema, tal que $N= \sum\limits_{i}n_{i}$, donde $n_{i}$ es el número de partículas asociadas a la energía i-ésima.

La energía total del sistema: $U=\sum\limits_{i}n_{i}E_{i}$. Y si el sistema está aislado entonces $U=cte$.

**Obs:** Si hay interacción entre partículas, ésta se da de a pares, y se asocia a una energía $E_{ij}$.

En un sistema de partículas, las partículas siempre interaccionan, por lo que $U$ no cambia. Pero si cambia la distribución de partículas entre los estados de energía.

**Obs:** Hay una distribución de las $N$ partículas que es más probable que cualquier otra. Cuando el sistema alcanza esta distribución, se dice que el sistema está en equilibrio estadístico. Además, $n_{i}$ pueden fluctuar alrededor de los valores que corresponden a la distribución más probable.

La probabilidad de que una partícula tenga una energía $E_{i}$ a la temperatura $T$ es $f_{mb}=Ae^{\frac{-E_{i}}{k_{B}T}}$.

Además, $g_{i}$ es el número de estados con la misma energía, por lo que puedo expresar que: $n_{i}=g_{i}f_{mb}$. Y se define $g(E)$
como la densidad de estados, es decir, la cantidad de estados con la misma energía en el intervalo $E$ y $E+dE$. A su vez, de la misma forma, podemos definir $n(E)dE$ como el número de partículas por unidad de volumen con energía comprendida en el mismo intervalo de energía más un diferencial.

Por lo tanto, se deduce la siguiente expresión: $n(E)dE=g(E)f_{mb}(E)dE$. Y si integramos en el intervalo correspondiente de energías nos queda:
$$\frac{N}{V}=\int_{0}^{\infty}n(E)dE=\int_{0}^{\infty}g(E)f_{mb}(E)dE$$
![[Pasted image 20240715174910.png#center]]

$$\bar{v}=<v>=\sqrt{\frac{8k_{B}T}{\pi m}} \qquad v_{rms}=\sqrt{\bar{v^{2}}}=\sqrt{\frac{3k_{B}T}{ m}} \qquad \tilde{v}=v_{np}=\sqrt{\frac{2k_{B}T}{m}} \qquad \frac{dn(v)}{dv}=0$$
$$\bar{E^{2}}=\frac{\int_{0}^{\infty}E^{2}n(E)dE}{\frac{N}{V}} \qquad \bar{E}=\frac{1}{2}m\bar{v^{2}}=\frac{3}{2}k_{B}T$$
### Modelo clásico de la conducción eléctrica
Se define la densidad de corriente eléctrica como: $\vec{J}=nq\hat{v_{d}}$, y por la ley puntual de Ohm $\vec{J}=\sigma \vec{E}$.

Luego, definimos $L$ como el camino libre medio entre colisiones consecutivas. Y $\tau$ como el tiempo libre medio respectivo, tal que $L=v_{rms}\tau$.

Además, $v_{d}=a\tau = \frac{eE}{m} \frac{L}{v_{rms}}$ → $J=nev_{d}=\frac{ne^{2}L}{mv_{rms}}E$ → $\sigma=\frac{ne^{2}L}{mv_{rms}}=\frac{ne^{2}L}{m\sqrt{\frac{3K_{B}T}{m}}}$.
**Obs:**
![[Pasted image 20240715181957.png#center]]

**Ejercicio:**
![[Pasted image 20240715182024.png#center]]

### Elementos de estadística cuántica

**Estadística de Fermi Dirac:** $n(E)dE=g(E)f_{fd}(E)dE$, tal que $g(E)= \frac{8\sqrt{2}\pi m^{\frac{3}{2}}E^{\frac{1}{2}}}{h^{3}}$, y $f_{fd}=\frac{1}{e^{\frac{E-E_{F}}{K_{B}T}}+1}$.
![[Pasted image 20240716152548.png#center]]
**Obs:**
- Todos los elementos de energía están ocupados si $E<E_{F}$.
- Todos los estados de energía están vacíos si $E>E_{F}$.

Según Maxwell y Boltzman, desde el punto de vista clásico, todos los electrones están en reposo a $0°K$. Hay un estado condensado de energía cero. Esto viola el principio de exclsión de Pauli.

Para Fermi y Dirac, con una perspectiva en relación a la física moderna, los electrones libres (o de conducción) se mueven.

![[Pasted image 20240716152943.png#center]]
![[Pasted image 20240716153051.png#center]]
#### Modelo cuántico de la conducción eléctrica en los metales
La conductividad eléctrica está asociada a la distribución de los electrones libres en diferentes niveles de energía que pueden ocupar en un sólido.
#### Correcciones a realizar en el modelo clásico
- $v_{rms}\to v_{F}$
- $\sigma = \frac{ne^{2}L}{mv_{rms}}\to \sigma = \frac{ne^{2}L}{mv_{F}}$
- El electrón no es una bolita que choca con los átomos, sino que es un objeto cuántico.
- Los valores de $\sigma$ y $\rho$ dependen de la temperatura. Clásicamente, si aumenta $T$, aumentan las vibraciones de la red. A nivel cuántico, hay las vibraciones de la red, hay niveles de energía, y la energía está cuantizada → Emisión de fonones.
#### Teoría de bandas
Entender la diferencia entre un sólido conductor/dieléctrico/semiconductor sin tener que resolver la ecuación de Schrödinger en los potenciales periódicos.

- Estructura de los niveles en energía en un átomo aislado.
- Dos átomos se aproximan → Extenderlo a muchos.

