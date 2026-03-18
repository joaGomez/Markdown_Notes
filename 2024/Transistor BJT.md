### Recta de carga
Mediante la superposición de las rectas características que definirán mi circuito o mi carga, puedo hallar el punto Q y saber fácilmente a que tensión y corriente funcionará el circuito.
![[Pasted image 20240824124656.png#center|400]]
### Curvas del BJT
![[Pasted image 20240824124857.png#center|400]]
### Polarización de un transistor
Para polarizar un transistor se debe conectar tensiones para lograr llevar al transistor a un entorno de trabajo Q.
![[Pasted image 20240824125107.png#center]]
La corriente de la malla de salida depende de la malla de entrada, esto se ve en la dependencia de las rectas de carga.
### Resolución de circuitos con transistores
- Circuito más básico: Dos fuentes y dos resistencias.
![[Pasted image 20240824195810.png#center|300]]
	Por la malla de entrada: $V_{BB}= i_{B}\cdot R_{B}+V_{BEon}$
	Por la malla de salida: $V_{CC}= i_{C}\cdot R_{C}+V_{CE}$
	Ec. del transistor: $i_{C}=i_{B}\cdot h_{FE}+ (h_{FE}+1)\cdot i_{cb0}$
	Al trabajor en el punto Q, nos quedarán las siguientes expresiones: $$\begin{split}
	&i_{Cq}= h_{FE}\cdot \frac{V_{BB}-V_{BEon}}{R_{B}} \\
	&V_{CEq}= V_{CC}-i_{C}\cdot R_{C}
	\end{split}$$
	**Obs:** Si vemos la expresión para la corriente de colector, ésta depende únicamente de la malla de entrada.
- Circuito de polarización con $R_{E}$:
![[Pasted image 20240824201355.png#center|300]]
	M.E) $V_{BB}= i_{B}\cdot R_{B}+V_{BEon}+R_{E}\cdot (i_{B}+i_{C})$
	M.S) $V_{CC}= i_{C}\cdot R_{C}+V_{CE}+R_{E}\cdot (i_{B}+i_{C})$
	*También se utiliza la ec del transistor.*
	Trabajamos en un punto Q:
	$$\begin{split}
	&i_{Cq}= h_{FE}\cdot \frac{V_{BB}-V_{BEon}}{R_{E}\cdot \frac{h_{FE}+1}{h_{FE}}  + \frac{R_{B}}{h_{FE}}} \simeq h_{FE}\cdot \frac{V_{BB}-V_{BEon}}{R_{E}+ \frac{R_{B}}{h_{FE}}}\\
	&V_{CEq}= V_{CC}-i_{C}\cdot (R_{C}+R_{E})
	\end{split}$$
- Circuito de autopolarización:
![[Pasted image 20240824202018.png#center|300]]
	Por Thevenin: $R_{TH}= \frac{R_{B1}\cdot R_{B2}}{R_{B1}+R_{B2}}=R_{B}$ y $V_{TH}= V_{CC}\cdot \frac{R_{B2}}{R_{B1}+R_{B2}}=V_{BB}$
	Podemos reemplazar estos valores en la ecuación de polarización anterior.
	$$\begin{split}
	&i_{Cq}= h_{FE}\cdot \frac{V_{TH}-V_{BEon}}{R_{E}\cdot \frac{h_{FE}+1}{h_{FE}}  + \frac{R_{TH}}{h_{FE}}} \simeq h_{FE}\cdot \frac{V_{BB}-V_{BEon}}{R_{E}+ \frac{R_{B}}{h_{FE}}}\\
	&V_{CEq}= V_{CC}-i_{C}\cdot (R_{C}+R_{E})
	\end{split}$$
**Obs:** El valor de $h_{FE}$ aumenta con la temperatura y varía con $i_{C}$
![[Pasted image 20240824202612.png#center|200]]
### Curvas características
![[Pasted image 20240824202656.png#center]]
### SOAR
SOAR es la región de operación segura de un transistor que opera en modo activo directo (MAD). Al trabajar en esta zona, se garantiza que el transistor no se dañe.
![[Pasted image 20240824202819.png#center|300]]
Si utilizamos una recta de carga para hallar el punto Q de trabajo, hay que ser cuidadosos por donde pasa la recta con respecta a SOAR.
![[Pasted image 20240824203019.png#center|300]]
Si utilizo inductores, debo tener cuidado debido a su particularidad en cuanto a la variación de corriente en el tiempo, ya que puedo salirme de la región de operación segura.
### Técnicas de compensación
El valor de $\beta/h_{FE}$ es muy disperso. Es común que en un transistor tenga una desviación del 200%/300%. Por lo tanto, esto afectará la dispersión de la corriente de colector en el punto Q. A su vez, la tensión de disparo de la base emisor varía con la temperatura (disminuye con T°), ya que se comporta como un diodo. También, $i_{CB0}$ aumenta muchísimo con la temperatura (x2/°C). Debido a esto, debo hallar la forma de ajustar $i_{Cq}$ para compensar la dispersión. Algunas de estas formas las trabajamos en la guía, como añadir un diodo en la malla de entrada.
### Modelos de alterna de pequeña señal en un BJT
#### Modelo de Giacoletto
Este modelo funciona tanto para npn como pnp, y se utiliza para transistores que trabajan en modo activo directo.
![[Pasted image 20240824213706.png#center|500]]
$$\begin{split}
&g_{m}= \frac{i_{Cq}}{V_{T}} \quad r_{\pi}= \frac{h_{FE}+1}{g_{m}}
\quad r_{0}= \frac{V_{A}}{i_{Cq}} \quad r_{\mu}=h_{FE}\cdot r_{0} \\
&h_{oe}= \frac{1}{r_{0}} \quad h_{FE}=\beta \quad h_{ie}=r_{\pi} \quad h_{re}=\mu \\
&C_{\pi}=C_{d_{BE}}+C_{j_{BE}} \quad \eta= \frac{V_{T}}{|V_{A}|} \quad C_{\mu}=\eta\cdot C_{d_{BC}}+C_{j_{BC}} 
\end{split}$$
**Obs:** Como $r_{0}$ está asociada a la tensión de Early, si no tengo valor de la tensión de Early, puedo tomar $r_{0}\to \infty$.

**Obs:** $r_{\mu}$ generalmente se toma como un cable abierto: $r_{\mu}\to \infty$.
#### Parámetros híbridos
$$h_{11}= \frac{V_{1}}{i_{1}}\bigg|_{V_{2}=0} \quad h_{12}= \frac{V_{1}}{V_{2}}\bigg|_{i_{1}=0} \quad h_{21}= \frac{i_{2}}{i_{1}}\bigg|_{V_{2}=0} \quad h_{22}= \frac{i_{2}}{V_{2}}\bigg|_{i_{1}=0}$$
Se puede utilizar el modelo de Giacoletto (sin los capacitores) con los parámetros híbridos:
![[Pasted image 20240824215551.png#center|500]]
$$\begin{rcases} h_{ie}=h_{11} \qquad \textit{Emisor común}\\
h_{ib}=h_{11} \qquad \textit{Base común}\\
h_{ic}=h_{11} \qquad \textit{Colector común}\\
\end{rcases}
\textit{Impedancias de entrada}$$
**Obs:** La segunda letra la usamos de referencia común en el transistor.

En emisor común (pero también para base común y colector común → Sólo debo reemplazar la segunda letra):
$$h_{11}=h_{ie}\quad h_{12}=h_{re}\quad h_{21}=h_{fe}\quad h_{22}=h_{oe}$$
KPI: Key performance indicator

Critical success factor: Caso de uso

![[Pasted image 20240904112231.png#center|500]]

**Obs:** Pasivar una fuente es reemplazarla por su resistencia interna. En una fuente de tensión ideal, su resistencia interna es cero. Mientras que para una fuente de corriente ideal, su resistencia interna es infinita.

|  Parámetros  |            Emisor común            |           Base común           |                Colector común                |
| :----------: | :--------------------------------: | :----------------------------: | :------------------------------------------: |
|  $\Delta V$  |             $-g_m R_d$             |           $g_m R_d$            |     $\frac{g_m R_d}{1+g_m R_d}\approx1$      |
|  $\Delta I$  |    $-h_{fe}\frac{R_c}{R_c+R_L}$    |          $\approx 1$           |                   $h_{fe}$                   |
|    $R_i$     |              $h_{ie}$              |    $\approx \frac{1}{g_m}$     |            $h_{ie}+R_d(1+h_{fe})$            |
|    $R_0$     |       $r_0=\frac{1}{h_{oe}}$       | $h_{ie}^{*}+r_0(1+h_{fe}^{*})$ | $\frac{h_{ie}}{h_{fe}}\approx \frac{1}{g_m}$ |
| $\Delta V_s$ | $-g_mR_d\frac{R_{ia}}{R_{ia}+R_s}$ |       $\frac{R_d}{R_s}$        |         $\frac{R_{ia}}{R_{ia}+R_s}$          |

