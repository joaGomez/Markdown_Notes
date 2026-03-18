Ecuaciones relacionadas:
$$V=\frac{d\phi}{dt}\qquad H.l_{e}=N.I \qquad B=\mu H \qquad \phi=B.A_{e}$$
A partir de estas ecuaciones podemos modelizar el coeficiente de autoinductancia:
$$V=\frac{N^{2}\mu A_{e}}{l_{e}}. \frac{dI}{dt}=L\frac{dI}{dt}$$
Como $V=L \frac{dI}{dt}$ → $P(t)=LI \frac{dI}{dt}$ → La energía que podrá almacenar un inductor será:
$$W=\int_{0}^{t}p(t')dt'=\frac{LI^{2}}{2}$$
Si el flujo entre dos espiras que generan una fem inducida $V_{1}, V_{2}$, con $N_{1},N_{2}$ espiras, son la misma: $\frac{d\phi_{1}}{dt}=\frac{d\phi_{2}}{dt}=\frac{d\phi}{dt}$ → Su **relación de transferencia** será tal que:$$\frac{V_{1}}{V_{2}}=\frac{N_{1}}{N_{2}}$$
La **inductancia mutua** es la equivalente a la inductancia generada entre las espiras la una a la otra, que será igual, por lo que nos queda:
$$M= \frac{N_{2}N_{1}\mu A_{e}}{l_{e}}$$
Las tensiones quedarán expresadas como:
$$\begin{split}
& V_{1}=L_{1} \frac{dI_{1}}{dt}+M \frac{dI_{2}}{dt} \\
& V_{2}=L_{2} \frac{dI_{2}}{dt}+M \frac{dI_{1}}{dt}
\end{split}$$
En este caso, los flujos son *aditivos*. En general, si los bornes son **homólogos** → Los flujos son aditivos.
![[Pasted image 20231027090247.png|200]]

					Los asteriscos indican que son homólogos

Si la homología es inversa, es decir, uno de los debanados tiene un asterisco arriba y el otro abajo, en este caso los flujos se restan. Entonces:
$$\begin{split}
& V_{1}=L_{1} \frac{dI_{1}}{dt}-M \frac{dI_{2}}{dt} \\
& V_{2}=L_{2} \frac{dI_{2}}{dt}-M \frac{dI_{1}}{dt}
\end{split}$$
Ejemplo para ver como afecta, no solo el borne homologo sino también la dirección de las corrientes:
![[Pasted image 20231027092932.png|250]]
Efectos en el circuito dependiendo de donde estén los bornes homólogos:
![[Pasted image 20231027094646.png]]
![[Pasted image 20231027095309.png|500]]
**Obs.** La tensión va a ser mayor cuando los bornes **NO** sean homólogos.
### Energía en acoplamiento magnético
$$W=\int_{0}^{T}p(t)dt=W_{R}+\int _{0}^{T} \frac{1}{2}(L_{1}- \frac{M^{2}}{L_{2}})I_{1}^{2}(t)~dt$$
**Obs.** Si $L_{1}- \frac{M^{2}}{L_{2}}=0$ → Se deja de almacenar energía en los inductores y se hace un corto.
**Def.** Sea $k^{2}= \frac{M^{2}}{L_{1}L_{2}}$ el **coeficiente de acoplamiento**.
- $k=0$ → Totalmente desacoplado. Los inductores no comparten flujo magnético.
- $k=1$ → Acoplamiento perfecto. Ningún flujo magnético escapa del núcleo. Comparten la totalidad de sus flujos. Todo el flujo de uno atraviesa al otro y viceversa.
![[Pasted image 20231102095123.png]]
**Ejemplo**
![[Pasted image 20231102175634.png]]
Transformadores ideales
![[Pasted image 20231102175708.png|500]]
![[Pasted image 20231102180142.png]]
**Observaciones de un transformador ideal**
- $\frac{V_{2}}{V_{1}}=n= \sqrt{\frac{L_{2}}{L_{1}}}$ → $\frac{I_{2}}{I_{1}}= \frac{1}{n}$
- $k=1,~\mu\to \infty \Rightarrow L_{1}\to \infty,L_{2}\to \infty$
![[Pasted image 20231102183510.png]]
![[Pasted image 20231102184643.png]]
La proxma clase vamos a ver las perdidas en un transformador y la modelizaremos como una resistencia $G_{0}$.
