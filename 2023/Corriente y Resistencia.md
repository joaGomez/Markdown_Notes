##### Def
La **corriente** se define como la cantidad a la cual circula la carga a través de una superficie. Se llama $I_{promedio}$ a la carga que pasa a traves de A (área de la superficie) en un intervalo de tiempo.
$$I_{promedio}=\frac{\Delta Q}{\Delta t}[A]$$
Si la tasa a la que circula la carga varía con el tiempo → Se define la *corriente instantánea* $I$ como el límite de la corriente promedio cuando $\Delta t\to 0$.
$$I\equiv  \frac{dQ}{dt} [A]$$
### Modelo microscópico de la corriente
Mediante la descripción de un modelo microscópico de la conducción en un metal, se puede relacionar la corriente con el movimiento de los portadores de carga. Siendo $n$ la *cantidad de portadores*, $\Delta x$ la *longitud del segmento del conductor*, $A$ el *área transversal del segmento del conductor* y $q$ la *la carga del portador* → La carga total $\Delta Q$ que pasa por la sección es:
$$\Delta Q=(nA\Delta x)q$$
Además, la magnitud del desplazamiento que experimentan en la dirección $x$ en un intervalo $\Delta t$ es $\Delta x=v_{d}\Delta t$, siendo $v_{d}$ la **rápidez de arrastre**. Por lo que la expresión nos queda:
$$\Delta Q=(nAv_{d}\Delta t)q 
\to I_{promedio}= \frac{\Delta Q}{\Delta t}=nqv_{d}A$$
## Resistencia
 **Densidad de corriente**
 $$J=\frac{I}{A}=nqv_{d}=\sigma E$$
Siendo $\sigma$ la *conductividad* del conductor. Los materiales que obedecen esta ecuación se los llama **Materiales ohmicos**.
Sea $\Delta V = V_{b}-V_{a}$
 $$\Delta V=El=\frac{lJ}{\sigma}=(\frac{l}{\sigma A})I=RI$$**Resistividad**
$$\rho = \frac{1}{\sigma} \to R=\rho \frac{l}{A}$$
### Resistencia y temperatura
En un intervalo limitado de temperatura, la resistividad de un conductor varía prácticamente de manera lineal con la temperatura:
$$
\begin{split}
&\rho = \rho_{0}[1+\alpha(T-T_{0})] \qquad (Resistividad) \\
&\alpha = \frac{\Delta \rho /  \rho_{0}}{\Delta T} \qquad (Coeficiente~de~ temperatura~de~resistividad)
\end{split}$$
Donde, $\Delta \rho = \rho - \rho_{0}$ y $\Delta T = T - T_{0}$
Se cumple que:
$$R = R_{0}[1+\alpha(T-T_{0})]$$
### Resistencias en paralelo
$$\begin{split}
& I=I_{1}=I_{2} \\
& \Delta V = \Delta V_{1} + \Delta V_{2} \\
& R_{eq} = R_{1} + R_{2}
\end{split}$$
### Resistencias en serie
$$\begin{split}
& I=I_{1} + I_{2} \\
& \Delta V = \Delta V_{1} = \Delta V_{2} \\
& \frac{1}{R_{eq}} = \frac{1}{R_{1}} + \frac{1}{R_{2}}
\end{split}$$
### Leyes de Kirchoff
- Ley de nodos: $\quad \sum\limits I=0$
- Ley de mallas: $\quad \sum\limits \Delta V = 0$
### Circuitos RC
##### Carga de un capacitor
$$\begin{split}
& q(t)=Q_{max}\left(1-e^{\frac{-t}{RC}}\right) \\
& i(t)=\frac{V}{R}e^{\frac{-t}{RC}}
\end{split}$$
##### Descarga de un capacitor
$$\begin{split}
& q(t)=Q_{i}e^{\frac{-t}{RC}} \\
& i(t)=-\frac{Q_{i}}{RC}e^{\frac{-t}{RC}}
\end{split}$$
