### Corriente eléctrica
Se define como la cantidad de carga que atraviesa una sección del conductor ($\Delta S$) por unidad de tiempo:
$$
\Delta Q=\rho \Delta l~ d S = \rho(\vec{v}\cdot \hat{n}\cdot\Delta t) dS
$$
Se define el diferencial de corriente como $dI= \frac{\Delta Q}{\Delta t}=\rho \vec{v}\cdot \hat{n}~dS$
$$\text{Densidad de corriente: } \qquad \vec{J}=\rho \cdot \vec{v} = (nq)\vec{v}$$
Donde $n$ es el número de cargas por unidad de volumen.
$$
\text{Intensidad de corriente: } \qquad I=\int_{S} \vec{J}\cdot \hat{n} \, dS 
$$
#### Movimiento de electrones en un conductor
Dado que ahora tenemos en cuenta el movimiento de los portadores de carga en el interior del conductor → $E_{int}\neq 0$
#### Modelo de Drude
En el modelo de Drude, se trata el movimiento de los e- como el de una partícula clásica. Donde $\tau$ (tiempo de relajación) es el tempo promedio entre colisiones.

Surge una nueva definición para la densidad de corriente:
$$
|\vec{J}| = nev_{d} \Rightarrow I=nev_{d}A
$$
Donde $v_{d}$ es la velocidad media de los electrones (velocidad de deriva).
$$
\vec{v}_{d} = \lim_{ t \to \infty } \vec{v}(t) = -\frac{e \tau}{m_{e}}\vec{E} 
$$
Sea $\mu= \frac{e\tau}{m_{e}}$ la movilidad de los e- en el metal → $I=neA \mu E$.
#### Relación entre J y E
La relación entre el campo eléctrico y la densidad de corriente en un conductor está dada por la siguiente relación:
$$
\vec{J}=\sigma \vec{E}
$$
Esta relación fue hallada por Ohm, que también definió:
$$
\rho = \frac{1}{\sigma}
$$
#### Ecuación de continuidad de la carga
El principio de conservación de la carga eléctrica es un principio general de la física, y estipula que la carga no se crea ni se destruye.

Toda la variación de la carga dentro de un recinto cerrado implica que hay un flujo de carga (una corriente) a través de la superficie de la frontera.
$$
\text{Ec. de continuidad: } \qquad \nabla\cdot \vec{J}+ \frac{\partial \rho}{\partial t} = 0
$$
Cuando la densidad de carga es independiente del tiempo → La densidad de corriente tampoco depende del tiempo → $\nabla\cdot \vec{J}=0$ → El vector $J$ no tiene fuentes ni sumderos en el recinto.

Para **corriente estacionaria** → No hay acumulación de carga dentro de una superficie cerrada:
$$
\nabla\cdot \vec{J}=\sigma \nabla\cdot \vec{E} = \frac{\rho}{\varepsilon_{0}} = 0 \to \rho = 0
$$
A partir de este principio surge la primera ley de Kirchoff, donde en un nodo de un circuito con corriente estacionaria → La suma de las corrientes que concurren a ese nodo es cero.
### Generador
Un generador es un dispositivo en cuyo interior los portadores de carga libre se ven sometidos a fuerzas de origen no electrostático ($E_{nc}$), dando lugar a separación de carga.
#### FEM
En un circuito cerrado C, donde circula una corriente estacionaria $I:$
$$
\oint_{C} \vec{E}\cdot d\vec{l} = \oint_{C} \frac{\vec{J}}{\sigma}\cdot d\vec{l} \neq 0
$$
Este resutado sugiere que $\vec{E}$ no es conservativo.

La circulación del campo a lo largo del circuito, se denomina **fuerza electromotriz** o **fem**.

El campo eléctrico que produce circulación de corriente estacionaria en un circuito no es un campo electrostático.

En general, podemos decir que el campo eléctrico dentro del circuito que transporta una corriente estacionaria es la suma de un campo conservativo, generado por distribuciones estáticas de carga (Coulomb) y un campo no conservativo:
$$
\vec{E}=\vec{E}_{c} + \vec{E}_{nc}
$$
Donde para el campo conservativo se cumplen las expresiones del campo electroestático.
$$
fem = \int_{B}^{A} \vec{E}_{nc}\cdot d\vec{l} + \cancel{\oint_{C} \vec{E}_{c}\cdot d\vec{l}}= \int_{B}^{A} \vec{E}_{nc}\cdot d\vec{l}
$$
$$
\text{Segunda ley de Kirchoff: } \qquad fem-\sum_{j}\Delta V_{j} = 0
$$
#### Efecto Joule
El trabajo realizado por el campo E sobre las cargas en movimiento que constituyen una corriente se transfiere a la estructura cristalina del cuerpo conductor en forma de calor.
$$
\begin{split}
\text{Potencia disipada por unidad de volumen: } \qquad &\frac{dW}{dt dV} = \vec{J}\cdot \vec{E} \\ 
\text{Potencia disipada: } \qquad & P=\int_{V} \vec{J}\cdot \vec{E} \, dV 
\end{split}
$$
Si el medio es Óhmico → $P=\int_{V} \sigma |\vec{E}|^{2} \, dV$
### Ley de Faraday
Un campo magnético variable en el tiempo induce un campo eléctrico.
$$
fem = - \frac{d\phi}{dt} = -\frac{d}{dt}\left( \int_{S} \vec{B}\cdot d\vec{S}  \right)
$$
Se puede hallar la forma diferencial de esta ley.:
$$
\text{Tercer ec. de Maxwell: } \qquad  \nabla \times \vec{E}(\vec{r},t) = - \frac{\partial\vec{B}(\vec{r},t)}{\partial t}
$$
### Ley de Lenz
La fem y las corrientes inducidas tienen la dirección y sentido tal que se oponen a la variación que las induce.
### FEM por movimiento
La fuerza de Lorentz sobre las cargas produce la fem. Con un sistema en movimiento entrando o saluiendo de un medio en presencia de campo magnético, debo tener en cuenta la sección del sistema que se encuentra dentro de la región con campo, e integrar el desplazamiento con respecto a esta región.
### Inducción por movimiento
El diferencial de superficie lateral puede definirse como $d\vec{S}=(\vec{v}dt) \times d\vec{l}$
$$
d\phi=\int_{SL} \vec{B}\cdot d\vec{S} = \left(\oint_{C} \vec{B}\cdot(\vec{v}\times d\vec{l})\right)dt  = -\left( \oint_{C}(\vec{v}\times \vec{B})\cdot d\vec{l}  \right) dt
$$
Por lo tanto:
$$
fem= -\frac{d\phi}{dt}\bigg{|}_{\frac{\partial B}{\partial t}=0} 
= \oint_{C} (\vec{v}\times \vec{B})\cdot d\vec{l}
$$
Se define $\vec{E}_{mov}= \vec{v}\times \vec{B}$ como **campo electromotor**.

**Obs:** El origen de la fem inducida por movimiento es consecuencia directa de la fuerza magnética que actúa sobre las cargas en movimiento.
### Caso general
$$
fem = - \frac{d\phi}{dt} = - \frac{\partial \phi}{\partial t}\bigg{|}_{v=0} - \frac{\partial \phi}{\partial t}\bigg{|}_{\frac{\partial B}{\partial t}=0} = - \int_{S} \frac{\partial \vec{B}}{\partial t}\cdot d\vec{S} + \oint_{C}(\vec{v}\times \vec{B})\cdot d\vec{l}
$$
### Generalización de la ley de Faraday
Para un circuito formado por una espira conductora $\Gamma$, un generador $G$, y un elemento $\Omega$, donde circula corriente y hay un campo variable $B(r,t)$, entonces:
$$
fem = \int \vec{E}'_{g}\cdot d\vec{l} + \oint_{\Gamma} (\vec{E}+\vec{v}\times \vec{B})\cdot d\vec{l} = fem_{gen} + fem_{inducida} = (R_{\Gamma}+R_{g}+R)\cdot I(t)
$$
### Densidad de corriente de desplazamiento
$$
\text{Ley de Ampère-Maxwell } \qquad \nabla \times \vec{B} = \mu_{0}\vec{J}+\mu_{0}\varepsilon_{0} \frac{\partial \vec{E}}{\partial t} 
$$
*Esta expresión cumple con la ec. de continuidad.*

Se define la densidad de corriente de desplazamiento como:
$$
\vec{J}_{d} = \varepsilon_{0} \frac{\partial \vec{E}}{\partial t}
$$
**Obs:** No es una carga real → No describe el movimiento de cargas.
### Ecuaciones de Maxwell
$$
\begin{split}
&\text{Ley de Gauss} & \nabla\cdot \vec{E} = \frac{\rho}{\varepsilon_{0}} \qquad & \iint_{S} \vec{E}\cdot d\vec{S} = \iiint_{V} \frac{\rho}{\varepsilon_{0}}dV = \frac{Q}{\varepsilon_{0}} \\ 
&\text{Ley de Gauss para el magnetismo} & \nabla\cdot \vec{B} = 0 \qquad & ∯_{S} \vec{B}\cdot d\vec{S}=0\\
& \text{Ley de Faraday}  & \nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t} \qquad & \oint_{C}\vec{E}\cdot d\vec{l} = - \frac{d}{dt}\left(\iint_{S}\vec{B}\cdot d\vec{S}\right)  \\
&\text{Ley de Ampère-Maxwell} & \nabla \times \vec{B} = \mu_{0}\vec{J}+\mu_{0}\varepsilon_{0} \frac{\partial \vec{E}}{\partial t} \qquad & \oint_{C} \vec{B}\cdot d\vec{l} = \mu_{0} \iint_{S}\vec{J}\cdot d\vec{S} + \mu_{0}\varepsilon_{0} \frac{d}{dt}\left(\iint_{S} \vec{E}\cdot d\vec{S} \right)
\end{split}
$$
**Obs:** Los campos ($E$ o $B$) no pueden ser fuentes de otros campos ($E$ o $B$), porque $\frac{\partial B}{\partial t}$ y $\frac{\partial E}{\partial t}$ se deben a cargas y corrientes. 
#### Ec. de Maxwell en presencia de medios materiales
Dado la polarización de un dieléctrico, donde su densidad de corriente de polarización está dada por $\vec{J}_{p} = \frac{\partial \vec{P}}{\partial t}$. A su vez, a partir de la magnetización de un medio, su densidad de corriente de magnetización es $\vec{J}_{m} = \nabla \times \vec{M}$. En estas condiciones, la densidad de corriente total será:
$$
\vec{J}=\vec{J}_{l} + \vec{J}_{m} + \vec{J}_{p} = \vec{J}_{l} + \nabla \times \vec{M} + \frac{\partial\vec{P}}{\partial t}
$$
Teniendo en cuenta las definiciones de $H$ y $D$, nos queda que:
$$
\nabla \times \vec{H}=\vec{J}+ \frac{\partial\vec{D}}{\partial t}  \quad \wedge \quad \nabla\cdot \vec{D}= \rho 
$$