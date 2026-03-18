### Conductores y dieléctricos
- Conductores perfectos: Hay cargas eléctricas que se pueden mover libremente, sin oposición (salvo en los límites físicos del medio).
- Dieléctricos ideales: Los electrones no pueden ser separados por la aplicación de un campo eléctrico (menor que el campo de ruptura).
### Equilibrio electroestático
Las cargas se encuentran en reposo. La condición de reposo implica que la fuerza neta sobre cada carga es nula.

La condición de equilibrio implica que en el material conductor $E=0$ en el interior.
##### Propiedades
- $\rho = 0$ en el interior del conductor.
- Cualquier carga neta en un conductor se encuentra sobre la superficie de este.
- El campo eléctrico justo fuera del consuctor es perpendicualr a la superficie.
- El módulo del campo exterior es proporcional a la densidad de carga superficial.
- Un conductor es un equipotencial. En todos los puntos de la superficie del conductor, el potencial es el mismo:
$$
\vec{E} \perp d\vec{l} \to \Delta V=V(B)-V(A) = - \int_{A}^{B} \vec{E}.d\vec{l} = 0 \to V(B)=V(A) 
$$
### Potencial y campo eléctrico generado por un dipolo
![[Pasted image 20250811092956.png#center|300]]
$$
V(\vec{r}) = \frac{q}{4\pi\varepsilon_{0}} \left( \frac{1}{|\vec{r}- \frac{\Delta \vec{r}}{2}|} - \frac{1}{|\vec{r} + \frac{\Delta \vec{r}}{2}|}\right)
$$
Si tomamos la distancia entre los dipolos como $d$, y la distancia entre O y P, como $\vec{r}$. Supongamos $r \gg d=|\Delta r|$, si desarrollamos en serie de Taylor de primer orden, obtenemos que:
$$
V(\vec{r}) \simeq \frac{1}{4\pi\varepsilon_{0}} \cdot \frac{\vec{p}\cdot\vec{r}}{|\vec{r}|^{3}} \qquad \qquad r \gg d
$$
El campo eléctrico generado será:
$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\varepsilon_{0}} \cdot \frac{[3(\vec{p}\cdot \hat{r})\hat{r}-\vec{p}]}{r^{3}} \qquad \qquad r\gg d
$$
**Observación:** El flujo de campo eléctrico a través de cualquier superficie cerrada que contiene un dipolo es cero. Las líneas de sampo que salen vuelven a entrar.

![[Pasted image 20250811101225.png#center|500]]
### Acciones del campo sobre el dipolo
$$
\vec{F}^{+} = q\vec{E}(P_{1}) \quad \vec{F}^{-} = -q\vec{E}(P_{2}) \qquad \text{Fuerza sobre las cargas debido al campo externo}
$$
$$
\vec{N}=\vec{r}\times \vec{F} = \vec{p}\times \vec{E} \qquad \text{Momento o cupla respectos del punto P}
$$
### Comportamiento dieléctrico
#### Sustancias polares
- Moléculas neutras con cargas ligadas: Asimetría en la distribución de carga → Momento dipolar permanente $p_{0} \neq 0$. 
![[Pasted image 20250811102026.png#center|450]]
#### Sustancias no polares
- Moléculas neutras con cargas ligadas: DIstribución simétrica de carga → Momento dipolar intrínseco nulo.
	Acción de un campo eléctrico: 
	![[Pasted image 20250811102559.png#center|300]]
	Induce un momento dipolar $p\neq 0:$
	![[Pasted image 20250811102752.png#center|300]]
### Vector polarización
$$
\begin{split}
& \vec{P} = \lim_{ \Delta \tau \to 0 } \frac{1}{\Delta \tau}\sum_{i=1}^{N} \vec{p}_{i} \\ 
& \vec{P}(\vec{r}') = \lim_{ \Delta \tau \to 0 } \frac{\Delta p}{\Delta \tau}\bigg{|}_{\vec{r}'} \quad \left[ \frac{C}{m{^2}} \right]
\end{split}
$$
Un medio está polarizado cuando $P(r')\neq 0$
#### Origen de la respuesta del dieléctrico
La polarizabilidad ($\alpha$) es la tendencia relativa de una distribución de cargas, tal como la nube electrónica de un átomo o molécula, a ser distorsionada de su forma normal por un campo eléctrico externo.
$$
\vec{p} = \alpha \vec{E} \longrightarrow \vec{P}=N\vec{p}=N\alpha \vec{E}
$$
1) Polarizabilidad electrónica ($\alpha_{e}$): En un átomo neutro, la nube electrónica se reorienta.
2) Polarizabilidad iónica ($\alpha_{i}$): Desplazamiento de los iones dentro de la molécula.
3) Polarizabilidad dipolar ($\alpha_{d}$): Reorientación de las moléculas polares.
4) Polarizabilidad de la carga espacial ($\alpha_{s}$): Migración de carga de largo alcance.
#### Campo generado por un material polarizado
Sea un material polarizado, el campo será el resultante de la superposición de los campos de todos los dipolos que contiene el material.

El potencial generado por un material polarizado de cierto volumen será:
$$
V(\vec{r}) = \frac{1}{4\pi\varepsilon_{0}} \cdot \int_{V'} \vec{P}(\vec{r}')\cdot \nabla'\left( \frac{1}{R} \right)\, d\tau' 
$$
Utilizando que $\vec{P}(\vec{r})\cdot \nabla'\left( \frac{1}{R} \right) = \nabla'\cdot\left( \frac{\vec{P}}{R} - \frac{1}{R}\nabla'\cdot \vec{P}\right)$
$$
V(\vec{r}) = \frac{1}{4\pi\varepsilon_{0}} \oint_{S'} \frac{\rho_{s}dS'}{R} + \frac{1}{4\pi\varepsilon_{0}} \oint_{V'} \frac{\rho}{R} \,d\tau'
$$
Donde se cumple que:
$$
\begin{cases}
\rho_{s}^{(p)} = \vec{P}\cdot \hat{n} \\
\rho^{(p)} = -\nabla\cdot \vec{P}
\end{cases}
$$
- $P$ uniforme:
	→ $\rho_{s}^{(+)}=\vec{P}\cdot \hat{n}>0$
	→ $\rho_{s}^{(-)}=\vec{P}\cdot \hat{n}<0$
	→ $\rho^{(p)}=0$
- $P$ no uniforme: Se mantienen las cargas de polarización (no nulas).
#### Cargas de polarización
Para calcular el campo eléctrico creado por el dieléctrico polarizado se pueden sustituir el dieléctrico por sus cargas de polarización. Se convierte en un problema de electrostática en el vacío. Se requiere conocer el vector polarización.
##### Carga total de polarización
$$
\begin{split}
& Q_{t} = \int_{S} \rho_{s}^{(p)} \, dS' + \int_{V} \rho^{(p)} \, dv' \\ 
& Q_{t} = \int_{S} \vec{P}\cdot \hat{n} \, dS' + \int_{V} \nabla\cdot \vec{P} \, dv' \\
& Q_{t} = \int_{S} \vec{P}\cdot \hat{n} \, dS' + \int_{S} \vec{P} \, dS' \\
& Q_{t} = 0
\end{split} \\ 
$$
La carga total de un dieléctrico polarizado es nula (salvo que se depositen cargas libres ).
### Vector densidad de flujo eléctrico
El campo eléctrico total es el producido por las cargas de polarización y las cargas libres ,se cumple la Ley de Gauss.
$$
\vec{D}=\varepsilon_{0}\vec{E}+\vec{P} \qquad \text{Vector desplazamiento o densidad de flujo eléctrico}
$$
Se puede utilizar para describir las expresiones de las cargas libres en modo diferencial o integral:
$$
\begin{split}
\nabla\cdot \vec{D}=\rho^{(l)} \\ 
∯_{S} \vec{D}\cdot d\vec{A}=Q^{(l)}
\end{split}
$$
Dado $\vec{D}=\varepsilon_{0}\vec{E}+\vec{P}:$
$$\nabla \times \vec{D}=\varepsilon_{0}\nabla \times \vec{E}+\nabla \times \vec{P}=
\begin{cases}
\nabla \times \vec{P} \quad \text{Estacionario} \\
0 \qquad ~ ~ ~ ~ ~  \text{Estacionario y P uniforme}
\end{cases}$$
Además,
$$
\nabla\cdot\vec{E}= \frac{\rho}{\varepsilon_{0}}=\frac{\rho^{(l)}+\rho^{(p)}}{\varepsilon_{0}}
$$
Por lo tanto, nos quedan las siguientes expresiones:
$$
\text{Para D}
\begin{cases}
\nabla\cdot \vec{D}=\rho^{(l)} \\
\nabla \times \vec{D}=\nabla \times \vec{P} \underset{\text{Con P uniforme}}{=} 0
\end{cases}
\qquad 
\text{Para E}
\begin{cases}
\varepsilon_{0}\nabla\cdot \vec{E}=\rho^{(l)}+\rho^{(p)} \\
\nabla \times \vec{E} = 0
\end{cases}
$$
En situaciones de alta simetría se cumple: $\nabla \times \vec{P}=0$, y se puede calcular el vector desplazamiento en función de las cargas libres utilizando la Ley de Gauss:
$$
\oint_{S}\vec{D}\cdot d\vec{S}=Q^{(l)}
$$
#### Relación constitutiva
- Un material se polariza como consecuencia de la existencia de un campo eléctrico. 
- En muchas sustancias la polarización es proporcional al campo eléctrico:
$$
\vec{P}=\varepsilon_{0} \mathcal{X}_{e}\vec{E} \qquad \text{Relación constitutiva lineal}
$$
Donde $\mathcal{X}_{e}$ es la susceptibilidad eléctrica, y en el vacío es nula, y $\vec{E}$ es el campo eléctrico total debido a las cargas libres y de polarización.

Al mismo tiempo:
$$
\vec{D}=\varepsilon_{0}\vec{E}+\vec{P}=\varepsilon_{0}\vec{E}+\varepsilon_{0}\mathcal{X}_{e}\vec{E} = \underbrace{\varepsilon_0\left(1+\mathcal{X}_e\right)}_{\varepsilon}\vec{E} = \varepsilon \vec{E}
$$
Donde $\varepsilon$ es la permitividad dieléctrica (absoluta) del material $\left[ \frac{F}{m} \right]$y $\varepsilon_{r}= \frac{\varepsilon}{\varepsilon_{0}}=1+\mathcal{X}_{e}$ es la permitividad dieléctrica relativa.

**Obs:** Dado $\vec{P}=\varepsilon_{0}\mathcal{X}_{e}\vec{E}=(\varepsilon-\varepsilon_{0})\vec{E}$, cuanto mayor sea $\varepsilon$, mayor será la polarización del medio.

**Obs:** Para los conductores $\mathcal{X}_{e}=0 \to \varepsilon_{r} \simeq 1$
### Condiciones de contorno para el campo electroestático
#### Propiedades integrales del campo electroestático
$$
∯_{S} = \vec{D}\cdot d\vec{A} = Q_{enc} \qquad \oint \vec{E}\cdot d\vec{l} = 0
$$
#### Condiciones de contorno
Sea S una superficie con una densidad de carga $\rho_{s}$ que separa la zona #1 con $\varepsilon_{1}$ y la zona #2 con $\varepsilon_{2}$.
![[Pasted image 20250811150306.png#center|200]]
$$
\begin{split}


& \oint_{S} \vec{D}\cdot d\vec{S}=Q \to 
\oint_{S} \vec{D}\cdot d\vec{S}= \oint_{S_{1}} \vec{D}\cdot d\vec{S} + \oint_{S_{2}} \vec{D}\cdot d\vec{S} + 
\underbrace{\oint_{S_{l}} \vec{D}\cdot d\vec{S}}_{=~0 ~ (\text{Si e → 0})} \\ 

& \oint_{S} \vec{D}\cdot d\vec{S} = (\vec{D}_{2}\cdot \hat{n}-\vec{D}_{1}\cdot \hat{n})\cdot\Delta S = Q = \rho_{s}\Delta S
\end{split}
$$
Teniendo en cuenta que $\oint \vec{E}.d\vec{l}=0$, para cualquier camino cerrado y que el campo $E$ se puede expresar como $\vec{E} = E_{t} \hat{t} + E_{n} \hat{n}$, entonces:
$$
\begin{split}


\oint \vec{E} . d\vec{l} & = \int_{l_{1}}\vec{E}.d\vec{l} + \int_{l_{2}}\vec{E}.d\vec{l} + \int_{l_{3}}\vec{E}.d\vec{l} + \int_{l_{4}}\vec{E}.d\vec{l} \\ 

0 & = E_{t_{2}}l_{1} - E_{n_{2}} \frac{l_{3}}{2} - E_{n_{1}} \frac{l_{3}}{2}
     - E_{t_{1}}l_{2} + E_{n_{1}} \frac{l_{4}}{2} + E_{n_{2}} \frac{l_{4}}{2} \\ \\
\text{Usando $l_{1}=l_{2}$} & \text{$=l$ y $l_{3}=l_{4}=h$, en el limite h $\to$ 0, la circulación resulta: } \\ \\

0 & = E_{t_{2}} l - E_{t_{1}}l \longrightarrow E_{t_{2}}=E_{t_{1}} \longrightarrow (\vec{E}_{2} - \vec{E}_{1})\times \hat{n} = 0
\end{split}
$$
![[Pasted image 20250813102058.png#center|300]]
##### Condición de contorno para el potencial
Se cumple que $E_{t_{1}}=E_{t_{2}}$ sobre la superficie de separación, entonces:
$$
\nabla V = \nabla_{t}V \hat{t} + \nabla_{n}V \hat{n} \longrightarrow -\nabla_{t} V_{1}\bigg{|}_{S} = -\nabla_{t} V_{2}\bigg{|}_{S} \longrightarrow \underset{\text{Sobre la superficie de separación}}{V_{1} = V_{2}}
$$
La función potencial es continua al atravesar la distribución superficial de carga $\rho_{s}$.
##### Interfase dieléctrico-conductor
![[Pasted image 20250813102930.png#center|250]]
En un conductor perfecto $E=D=0 \to E_{2}=D_{2}=0$.

Por condiciones de contorno:
$$
\begin{split}
E_{t_{1}}=E_{t_{2}} & \longrightarrow E_{t_{2}}=E_{t_{1}} = D_{t_{1}} = 0 \\
D_{n_{1}} - D_{n_{2}} = \rho_{s} &\longrightarrow D_{n_{1}} = \rho_{s} \\ 
\vec{D}_{1} = D_{n_{1}} = \varepsilon_{1} E_{n_{1}} \hat{n} = \rho_{s} & \Longrightarrow  |E_{n_{1}}|= \frac{\rho_{s}}{\varepsilon_{1}}
\end{split}
$$
##### Medio L.I.H
- **Lineal**: La polarización es proporcional al campo,  $P = \chi_e \, \varepsilon_0 \, E$, donde $\chi_e$ es independiente de $E$.

- **NO Lineal**: La polarización puede expresarse como una serie de potencias de $E:$    $$
  P(E) = \varepsilon_0 \left( \chi_1 E + \chi_2 E^2 + \dots + \chi_n E^n \right)
  $$
- **Isótropo**: La susceptibilidad eléctrica es un escalar $P // E$.

- **NO Isótropo**: La susceptibilidad ($\varepsilon$) eléctrica varía dependiendo de la dirección en la que se mida.
$$
\begin{bmatrix}
D_x(\vec{r}) \\
D_y(\vec{r}) \\
D_z(\vec{r})
\end{bmatrix}
=
\begin{bmatrix}
\varepsilon_{xx} & 0 & 0 \\
0 & \varepsilon_{yy} & 0 \\
0 & 0 & \varepsilon_{zz}
\end{bmatrix}
\begin{bmatrix}
E_x(\vec{r}) \\
E_y(\vec{r}) \\
E_z(\vec{r})
\end{bmatrix}
$$
- **Homogéneo:** La susceptibilidad eléctrica no depende de la posición.

- **Inhomogéneo:** La susceptibilidad eléctrica depende de la posición $\mathcal{X}_{e}(r)$.

La mayoría de los gases, líquidos, sustancias amorfas, cuerpos cristalinos y monocristales cúbicos presentan unas relaciones constitutivas del tipo $P=\mathcal{X}_{e}\varepsilon_{0}E$. Algunos medios que no cumple con esta relación son los materiales ferroeléctricos o los electretes.

Los electretes presentan polarización en ausencia de campo eléctrico externo $P=P_{0}$, y tienen un $\varepsilon_{r}$ muy elevado.