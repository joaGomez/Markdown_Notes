----
Circuitos en tiempo:
- Transitorio
- Permanente

### Régimen Permanente
---
Tomo la polaridad de la batería en un instante, asociado al momento en el que di inicio al circuito.
Cada componente del circuito van a estar asociados a una forma senoidal o cosenoidal, llamado excitación del circuito.

$$V_{F}(t)=V_{Max}\ cos(\omega t+\phi_{V})$$

$$I(t)=I_{Max}\ cos(\omega t+\phi_{I})$$
Para que sea mucho más simple resolver las ecuaciones integro-diferenciales que van a aparecer por analizar circuitos con inductores y capacitores → Utilizo números complejos:
$$V_{F}(t)=V_{Max}.e^{j(\omega t+\phi_{V})}=V_{Max}(cos(\omega t+\phi_{V})+j.sen(\omega t+\phi_{V}))$$

$$I(t)=I_{Max}.e^{j(\omega t+\phi_{I})}=I_{Max}(cos(\omega t+\phi_{I})+j.sen(\omega t+\phi_{I}))$$
###### Impedancia
$$Z=R+jX=R+j\left(\omega L-\frac{1}{\omega C}\right)\to Z=\frac{V_{R}}{I_{R}}$$
###### Valores eficaces
$$V_{ef}=\frac{V_{Max}}{\sqrt{2}}$$

$$I_{ef}=\frac{I_{Max}}{\sqrt{2}}$$

![[Pasted image 20230817175535.png|300]]
El ángulo de desfasaje queda expresado por la siguiente fórmula:
$$\phi=tg^{-1}(\frac{\omega L}{R})$$
## Potencia
---
### Potencia instantánea
$$p(t)=i(t)v(t) \quad [Watt]$$
								
												Se distingue escribiendola en minúscula

La potencia instantánea es la potencia en cada instante, por lo que ya **no** será *cte* en el tiempo.

> Ya que esta regida por la corriente y la tensión en el tiempo, cuando estas se anulen, la potencia se anulará y valdrá 0. De la misma forma, la polaridad de la potencia estará asociada a la polaridad de la tensión y la corriente en el tiempo.

$$\begin{split}
&p(t)=i(t)v(t)=V_{m}I_{m}cos(\omega t+ \theta_{v})cos(\omega t+ \theta_{i})
\\& p(t)= \frac{1}{2}V_{m}I_{m}cos(\theta_{v}-\theta_{i})+\frac{1}{2}V_{m}I_{m}cos(2\omega t+\theta_{v} +\theta_{i})
\end{split}$$

### Potencia promedio (Activa)
Proviene de calcular el promedio de la potencia instantánea a lo largo de un período (de la señal): $P=\frac{1}{T}\int_{0}^{T}p(t)dt$
$$\begin{split}
& P =\frac{1}{2}V_{m}I_{m}cos(\theta_{v}-\theta_{i})=\frac{1}{2}Re(VI^{*})\\
& P =(\frac{V_{m}}{\sqrt {2} })(\frac{I_{m}}{{\sqrt {2}}})cos(\theta_{v}-\theta_{i})\\
& P =V_{ef}I_{ef}cos(\theta_{v}-\theta_{i})

\end{split}$$
![[Pasted image 20230824173117.png|300]]
							
													 Se la conoce como potencia activa.

###### [[Casos particulares de la potencia promedio]]

###### [[Regla memotécnica]]
### Valor eficaz
La idea del valor eficaz surge de la necesidad de medir la eficacia de una fuente de tensión o de corriente en el suministro de potencia a una carga resistiva.

![[Valor eficaz]]

### Potencia aparente
$$|S|=V_{ef}I_{ef} \qquad [VA]$$
### Potencia reactiva
$$Q=V_{ef}I_{ef}sen(\phi) \qquad [VAR]$$
El valor medio en un período es igual a cero, pero para poder dimensionar la misma se adopta:
![[Pasted image 20230824183759.png|350]]
### Potencia compleja
$$S=P+jQ=\frac{V_{ef}^{2}}{Z^*}$$
### Factor de potencia
$$cos(\theta_{v}-\theta_{i})=cos(\phi)=\frac{P}{S}=\frac{R}{Z}$$
### Triángulo de potencias
![[Pasted image 20230824184101.png|400]]
![[Pasted image 20230824184244.png|400]]
**X**: Parte reactiva (*Imaginaria*)
**R**: Parte resistiva (*Real*)

#### Aumentar el factor de potencia
Para aumentar el valor de del factor de potencia, hay que achicar el valor de $\varphi$. Para esto, lo que se hace es conectar un capacitor en paralelo a la carga. 
![[Pasted image 20230831224158.png|300]]
De este modo se consigue un $Q_{c}$ (Potencia reactiva de la capacitancia) que reduce el valor de $\varphi$ ya que ahora $Q' = Q - Q_{c}$.
![[Pasted image 20230831224253.png|200]]
Donde en módulo:
$$\begin{split}
& Q_{c}= X_{c}I_{c}^{2}=\frac{V^{2}}{X_{c}}=\frac{V^{2}}{\frac{1}{\omega C}} \\
& Q_{c}= \omega C V^{2} \\
& C =\frac{Q_{c}}{\omega V^{2}} = \frac{Q_{c}}{(2\pi f)V^{2}}
\end{split}$$
Además:
$$
\begin{split}

& Q_{c}= Q - Q' = P ~ (tg(\varphi) \ - \ tg(\varphi '))

\end{split}
$$
Por lo que podemos deducir la expresión:
$$C = \frac{P ~ (tg(\varphi) \ - \ tg(\varphi '))}{2\pi f V^{2}}$$

### Máxima transferencia de potencia
![[Pasted image 20230831231705.png|500]]
![[Pasted image 20230831231810.png|500]]
Y se deben cumplir la siguiente condición:
$$X_{L}=-X_{Th} \qquad R_{Th}=R_{L} \qquad Z_{L}=Z_{Th}^{*}$$
![[Pasted image 20230831232107.png|300]]
Y para tener la máxma transferencia de potencia:
$$\frac{dP_{L}}{dR_{L}}=0$$
Donde para este circuito en particular se debe cumplir que:
$$R_{L}= \sqrt{ R_{Th}^{2} +X_{Th}^{2}}$$
