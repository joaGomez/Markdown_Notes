![[Pasted image 20241025111300.png#center]]
$$V_{d}= V_{a}-V_{b} = Vs\cdot \frac{z_{3}}{z_{1}+z_{3}}-Vs\cdot \frac{z_{4}}{z_{2}+z_{4}}$$
Si $V_{d}=0 \to z_{1}z_{4}=z_{2}z_{3}$.
### Sensibilidad
Se define el comportamiento de la salida del puente al variar una de sus impedancias:
$$v_{d}+ \Delta v_{d}= \frac{z_{2}(z_{3}+\Delta z_{3})-z_{1}z_{4}}{(z_{1}+z_{3}+\Delta z_{3})(z_{2}+z_{4})}\cdot v_{s} \Rightarrow \Delta v_{d} = \frac{1}{(\frac{z_{1}}{z_{3}}+1)(\frac{z_{4}}{z_{2}}+1)}\cdot \frac{\Delta z_{3}}{z_{3}}\cdot v_{s}$$
Asumí $\Delta z_{3} << z_{3} \to z_{3}+ \Delta z_{3} \approx z_{3}$.
### Factor cabeza de puente
Asumo $z_{2}$ y $z_{4}$ constantes durante la medición → Se define cabeza de puente: $A = \frac{z_{4}}{z_{2}}$.

Por el equilibrio ($v_{d}=0$): $z_{1}z_{4}=z_{2}z_{3}$. Teniendo en cuenta la expresión de cabeza de puente:
$$A= \frac{z_{4}}{z_{2}}= \frac{z_{3}}{z_{1}} \longrightarrow \Delta v_{d} = \frac{1}{(\frac{1}{A}+1)(A+1)}\cdot \frac{\Delta z_{3}}{z_{3}}\cdot v_{s} = \frac{A}{(1+A)^{2}}\cdot \frac{\Delta z_{3}}{z_{3}}\cdot v_{s}= F\cdot \frac{\Delta z_{3}}{z_{3}}\cdot v_{s}$$
Donde $F= \frac{A}{(1+A)^{2}}$ es el **factor cabeza de puente**.

Considerando $\epsilon_{z_{3}} = \frac{\Delta z_{3}}{z_{3}} \to \Delta v_{d}= |F|\epsilon_{z_{3}}v_{s}$. La sensibilidad es proporcional a la entrada.

![[Pasted image 20241025112911.png#center]]

![[Pasted image 20241025112933.png#center]]
#### Puente de Maxwells (L)
![[Pasted image 20241025113059.png#center]]
#### Puente de Hay (L)
![[Pasted image 20241025113130.png#center]]
#### Puente C serie
![[Pasted image 20241025113158.png#center]]
#### Puente C paralelo
![[Pasted image 20241025113230.png#center]]
#### Puente Schearing
![[Pasted image 20241025113300.png#center]]
#### Puente de Wien
![[Pasted image 20241025113430.png#center]]
