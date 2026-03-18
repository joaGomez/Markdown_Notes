Un circuito de corriente alterna cuenta con una fuente de tensión que va a variar en función del tiempo, con un valor $\Delta V_{max}$ (Valor pico), y en función de una senoidal, por lo que la tensión de la fuente en el circuito oscilará alrededor de ese valor pico.
$$\Delta V=\Delta V_{max}\ cos(\omega t+\phi)$$
Esto también se aplicará para la corriente, tal que:
$$I=I_{max}\ cos(\omega t+\phi)$$

**Obs.** Una regla memotécnica es CIVIL:
**C: Bobina capacitiva** → *I* (Corriente) adelanta la *V* (Tensión)
**L: Bobina inductiva** → *V* (Tensión) adelanta la *I* (Corriente)

### Valores eficaces
Los valores eficaces, o también llamados, valores **rms**, son el promedio del valor pico.
$$\begin{split}
& I_{ef}=\frac{I_{max}}{\sqrt{2}} \\
& \Delta V_{ef}=\frac{\Delta V_{max}}{\sqrt{2}}
\end{split}$$
### Impedancia
Se define la impedancia como:
$$Z=R+j\left(\omega L- \frac{1}{\omega C}\right)$$
Donde $X_{L}=\omega L$ es la **reactancia inductiva**. Y $X_{C}=\frac{1}{\omega C}$ es la **reactancia capacitiva**.
Con estas nuevas definiciones, podemos definir la impedancia de otra forma:
$$Z=\sqrt{R^{2}+(X_{L}-X_{C})^{2}}$$
Y a su vez:
$$\Delta V_{max}=Z\ .\ I_{max}$$
La expresión para el desfasaje será la siguiente:
$$\phi = atan(\frac{X_{L}-X_{C}}{R})$$
**Obs.**
- Cuando $X_{L} > X_{C}$ → $\phi > 0$ → El circuito es más **inductivo**.
- Cuando $X_{L} < X_{C}$ → $\phi < 0$ → El circuito es más **capacitivo**.
- Si $X_{L} = X_{C}$ → El circuito es más **puramente resistivo**.

### Potencia
- Potencia promedio: $P_{prom}=V_{ef}~I_{ef}~cos(\phi)$


### Factor de calidad
$$Q=\frac{\omega_{0}L}{R}$$
### Resonancia
Decimos que un circuito se encuentra en resonancia cuando éste es puramente resistivo, esto quiere decir que $Im(Z)=0$. En base a esto, llamamos $\omega_{0}$ a la **frecuencia de resonancia**.