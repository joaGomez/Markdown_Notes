### Estructuras cristalinas

Estas estructuras se pueden clasificar de las siguientes maneras:
- Amorfos: Elementos no ordenados.
- Policristalino: Elementos ordenados en grupos.
- Cristalino: Elementos ordenados a lo largo del material.

#### Celda unitaria
Es una sección del cristal que podamos utilizar para replicar el material. Esta celda se repite a lo largo de todo el sólido. No necesita ser primitiva(la más pequeña), ni tampoco única.

##### Formas
El siguiente cuadro muestra el total de átomos en las celdas unitarias básicas:

**Obs:** Esquinas → $1/8$, Caras → $1/2$, para saber cuantos átomos tienen en esa parte solo debo multplicar estas fracciones por la cantidad en cada caso.

|  Nombre  | Esquinas | Centro | Caras | Interior | Total |
| :------: | :------: | :----: | :---: | :------: | :---: |
|  Cúbica  |    8     |   0    |   0   |    0     |   1   |
|   BCC    |    8     |   1    |   0   |    0     |   2   |
|   FCC    |    8     |   0    |   6   |    0     |   4   |
| Diamante |    8     |   0    |   6   |    4     |   8   |

![[Pasted image 20240307190132.png#center]]

#### Indices de Miller
Con los valores $x,y,z$ donde el plano corta los ejes de coordenadas, por ej ($x_{0}, y_{0}, z_{0}$) → Invierto sus valores, ($\frac{1}{x_{0}}, \frac{1}{y_{0}}, \frac{1}{z_{0}}$) y busco el minimo común múltiplo de los denominadores y los múltiplico por ese número, dandome como resultado el índice de Miller.

![[Pasted image 20240307190720.png#center|100]]
#### Átomo de silicio
Ventajas del silicio:
- Abundante → Proviene de la arena
- Facilidad para generar dióxido de silicio(aislante) → Muy utilizado para semiconductores

#### Diagrama de bandas
La energía está cuantizada (sólo toma valores discretos), y mediante los diagramas de banda, podemos ver la energía que necesitan los electrones para saltar entre bandas.

![[Pasted image 20240307193234.png#center]]

A medida que los átomos se acercan, los niveles empiezan a formar bandas de energía permitidas(banda de conducción/valencia) o prohibidas(gap).
Dentro de la banda de conducción, los electrones pueden moverse libremente y generar corriente frente a la aplicación de un campo eléctrico.

![[Pasted image 20240307193458.png#center|300]]
								*A menor gap, el material va a ser más conductor.*
##### Casos

![[Pasted image 20240307194828.png#center|600]]
#### Portadores de carga

![[Pasted image 20240308092154.png#center|300]]
Cuando un $e^{-}$ gana suficiente energía, puede romper el enlace covalente que lo une al núcleo, y pasar a la banda de conducción → Deja una carga positiva, denominada **hueco**, que puede ser ocupada por otro $e^{-}$. Este *hueco* puede entenderse como una carga positiva en movimiento. 
###### Tipos de portadores de carga:
- Electrones en la banda de conducción
- Huecos en la banda de valencia
*Ambos contribuirán a la circulación de corriente*.

Los **semiconductores intrínsecos** son los SC en los cuales por cada $e{^{-}}$ que pasa a la zona de conducción, se genera un hueco en la banda de valencia.

Se denominan **semiconductores extrínsecos**, a los semiconductores dopados. Este proceso se consigue inyectando átomos 'a la fuerza', a modo de aumentar la concentración, ya sea de electrones o de huecos.

Los **semiconductores de tipo-n** son semiconductores los cuales se los dopa con *donantes*, átomos con 5 $e^{-}$ de valencia, algunos ejemplos son el fósforo o el arsénico. De los 5 $e^{-}$, 4 participan en los enlaces covalentes con los átomos de silicio, y el restante queda débilmente atado al núcleo, y para romper este enlace se necesita menos energía que para romper los enlaces entre los átomos de silicio. Se genera un $e^{-}$ en la banda de conducción sin generar un hueco en la banda de valencia.

![[Pasted image 20240313125447.png#center|400]]

Los **semiconductores de tipo-p** son semiconductores los cuales se los dopa con *receptores*, átomos con 3 $e^{-}$ de valencia, como el boro. Al romperse un enlace Si-Si el $e^{-}$ liberado va a ir a ocupar ese hueco ya que requiere menos energía que la necesaria para saltar hacia la banda de conducción. Se genera un hueco en la banda de valencia sin generar un electrón en la banda de conducción.

![[Pasted image 20240313125408.png#center|400]]

#### Diagrama de bandas para dopantes
Orden de nivel de energía requerida (menos <<< mayor):
- un átomo donante pase a la banda de conducción <<< Un electrón rompa un enlace covalente y salte desde la banda de valencia.
- Un electrón rompa un enlace covalente y ocupe un hueco de un átomo receptor <<< Ese electrón salte a la banda de conducción.
Las impurezas generan nuevos estados permitidos dentro de la banda prohibida.

#### Masa efectiva
Esta masa toma en cuenta las colisiones que sufren los $e^{-}$ de una red cristalina y que provoca que desaceleren y cambien su trayectoria. Este concepto permite relacionar la mecánica cuántica con la mecánica clásica y permite poder aplicar la ley de Newton para describir el movimiento en una red.
$$\vec{F}=m_{n}^{*}\times \frac{\partial \vec{v_{n}}}{\partial t}=m_{p}^{*}\times \frac{\partial \vec{v_{p}}}{\partial t}$$
#### Mecánica estadística
Las características eléctricas se determinan por el **comportamiento estadístico** de un gran número de portadores.

Un estado cuántico se define como un estado posible dentro de un sistema cuántico caracterizado por determinadas propiedades (momento angular, nivel de energía, etc.). 

El principio de exclusión de Pauli menciona que un estado cuántico puede estar ocupado únicamente por una sola partícula.

![[Pasted image 20240307201641.png#center|200]]

Los estados cuánticos se distribuyen dentro de cada nivel de energía, y las partículas tienden a ocupar primero los niveles más bajos.

**Obs:** La densidad de estados en el gap es 0, ya que no hay posibilidad de que ocupen los electrones en ese estado.

> Cuando un sólido está en condición de equilibrio, tiene neutralidad de cargas

La unidad que usamos para medir la densidad de estados es $[g(E)]= \frac{n_{estados}\cdot  cm^{-3}}{eV}$

> Funciones de distribución de probabilidad
>    • Función de Maxwell – Boltzmann: describe el comportamiento de moléculas en un gas. Considera que las partículas son distinguibles (partícula A están en el estado 1 y la B en el estado 2 es una distribución diferente a B en estado 1 y A en estado 2). No hay límite en el número de partículas por estado cuántico.
>
>    • Función de Bose – Einstein: describe el comportamiento de fotones. Considera que las partículas son indistinguibles y no hay límite para el número de partículas por estado cuántico. 
>
      • Función de Fermi – Dirac: describe el comportamiento de electrones en un cristal. Considera que las partículas son indistinguibles y sólo se permite una partícula por estado cuántico.


Función de Fermi-Dirac
$$f_{F}(E)= \frac{1}{1+e^{\frac{E-E_{F}}{kT}}}$$
![[Pasted image 20240307203002.png#center|250]]
Como está función describe la probabilidad de encontrar un electrón en un estado → la probalidad de que un estado no sea ocupado es de $P=1-f_{F}(E)$

![[Pasted image 20240307203024.png#center|250]]

Para la aproximación de Boltzman, consideramos $E-E_{F}>>kT \to 1+e^{\frac{E-E_{F}}{kT}}\sim e^{\frac{E-E_{F}}{kT}}$. Esta aproximación se considera válida a partir de $E-E_{F}>3kT$ (electrones) y $E_{F}-E>3kT$ (huecos)

![[Pasted image 20240307203610.png#center|450]]

**Obs:** En la región válida para $E_{F}$ se encuentra el material no degenerado.
#### Distribución de los portadores en equilibrio
La densidad(concentración) de portadores se puede obtener a través de la densidad de estados y la probabilidad de que un estado sea ocupado:
$$n(E)=g_{c}(E).f_{F}(E) \qquad p(E)=g_{v}(E).[1-f_{F}(E)]$$
#### Concentración de portadores en equilibrio
$$n_{0}=N_{c}.e^{\frac{E_{F}-E_{C}}{kT}}, \qquad [n_{0}]=\frac{n_{electrones}}{cm^{3}}$$
Donde $N_{c}=2(\frac{2.\pi . m_{n}^{*}.k.T}{h^{2}}){^\frac{3}{2}}$ es la **densidad de estados en la banda de conducción**.
$$p_{0}=N_{v}.e^{\frac{E_{V}-E_{F}}{kT}}, \qquad [p_{0}]=\frac{n_{huecos}}{cm^{3}}$$
Donde $N_{v}=2(\frac{2.\pi . m_{p}^{*}.k.T}{h^{2}}){^\frac{3}{2}}$ es la **densidad de estados en la banda de valencia**.

#### Concentración en un SC intrínseco en equilibrio
En un semiconductor intrínseco los electrones libres en la banda de conducción ($n_{0}$) y los huecos en la banda de valencia ($p_{0}$) se generan de a pares.

$$\begin{align}
& n_0 = n_{i} = N_{c}.e^{ \frac{-(E_{c}-E_{Fi})}{kT}} \qquad
 p_{0} = n_{i} = N_{v}.e^{ \frac{-(E_{Fi}-E_{v})}{kT}} \qquad \begin{cases} n_{0} = n_{i} = p \end{cases} \\ 
& n_{i}^{2} = n_{0}.p_{0} = N_{c}.N_{v}.e^{\frac{-E_{gap}}{kT}} \Rightarrow n_{i}=\sqrt{N_{c}.N_{v}} .e^{\frac{-E_{gap}}{2kT}} \\
& E_{gap}=E_{c}-E_{v}
\end{align}$$
#### Neutralidad de carga en equilibrio
- Electrones $n \to q^{-}$
- Huecos $p \to q^{+}$
- Impurezas donoras ionizadas $N_{D}^{+} \to q^{+}$
- Impurezas aceptoras ionizadas $N_{A}^{-} \to q^{-}$
$$p+N_{D}^{+}=n+N_{A}^{-}$$
A temperatura ambiente, se puede considerar que todas las impurezas están ionizadas, es decir: $N_{D}^{+}=N_{D}$ y $N_{A}^{-}=N_{A}$
$$relación\ de \ neutralidad \ de \ carga \qquad
p-n+N_{D}-N_{A}=0$$ **Útil:** $np=n_{i}^{2}$
#### Concentración en un SC extrínseco en equilibrio
Los parámetros de un SC extrínseco se pueden relacionar con los de un SC intrínseco:
$$\begin{rcases}
& n_0 = N_{c}.e^{ \frac{-(E_{c}-E_{F})}{kT}} \\
& n_{i} = N_{c}.e^{ \frac{-(E_{c}-E_{Fi})}{kT}} \\\end{rcases} \quad n_{0}=n_{i}.e^{\frac{E_{F}-E_{Fi}}{kT}}
\begin{rcases} 
& p_0 = N_{v}.e^{ \frac{-(E_{F}-E_{v})}{kT}} \\
& n_{i} = N_{v}.e^{ \frac{-(E_{Fi}-E_{v})}{kT}} \\\end{rcases} \quad p_{0}=n_{i}.e^{\frac{-(E_{F}-E_{Fi})}{kT}}$$

> Observaciones de los SC
> 1. SC intrínseco: $N_{A}=0, N_D =0 \to n=n_{i},~ p=n_{i} \Rightarrow n=p=n_{i}$
> 2. SC extrínseco:  - Tal que $N_{D}-N_{A} \simeq N_{D} >> n_{i}: n\simeq N_{D}\to p\simeq \frac{n_{i}^{2}}{N_{D}}$ $\lor$ $N_{A}-N_{D} \simeq N_{A} >> n_{i}: p\simeq N_{A}\to n\simeq \frac{n_{i}^{2}}{N_{A}}$  
> 						  - Si está a una temperatura lo suficientemente elevada, $n_{i}>>|N_{D}-N_{A}| \to$ Se comporta como un SC intrínseco ($n=n_{i}=p$)
> 3. SC compensados: $|N_{D}-N_{A}|\sim n_{i}$

#### Energía de Fermi en un SC extrínseco
Utilizando las expresiones anteriores:
$$\begin{split}
E_{F}-E_{Fi}= k T \cdot ln\left(\frac{n_{0}}{n_{i}}\right) \\
E_{Fi}-E_{F}= k T \cdot ln\left(\frac{p_{0}}{n_{i}}\right)
\end{split}$$
#### Energía de Fermi en un SC intrínseco
La energía de Fermi se puede derivar sabiendo que en un SC intrínseco $n_{0}=p_{0}$.
$$E_{Fi}= \frac{E_{c}-E_{v}}{2}+ \frac{1}{2}\cdot k\ \cdot T\ \cdot ln(\frac{N_{v}}{N_{c}})=\frac{E_{c}-E_{v}}{2}+ \frac{3}{4}\cdot k\ \cdot T\ \cdot ln(\frac{m_{p}^{*}}{m_{n}^{*}})$$
**Obs:** 
- El átomo de Silicio posee cuatro electrones de Valencia que participarán en los enlaces covalentes con átomos vecinos 
- La energía está cuantizada (sólo puede tomar valores discretos) 
- Al unirse los átomos de Si crean bandas de energías permitidas (conducción y valencia) y prohibidas 
- Un SC en el cual un electrón que salta a la banda de conducción deja un hueco en la banda de valencia se denomina intrínseco 
- Las propiedades de un SC se pueden modificar a través del agregado de impurezas. Este proceso se denomina dopaje 
- Un dopaje con átomos con 5 electrones de valencia crea electrones en la banda de conducción sin crear huecos en la banda de valencia. A este SC se lo denomina tipo-n 
- Un dopaje con átomos con 3 electrones de valencia crea huecos en la banda de valencia sin crear electrones en la banda de conducción. A este SC se lo denomina tipo-p 
- La masa efectiva permite considerar las colisiones de los electrones con átomos vecinos y aplicar la Ley de Newton para analizar su movimiento
- A muy altas temperaturas un semiconductor dopado actúa como un semiconductor dopado.
- Para cuantificar los portadores en un semiconductor es necesario utilizar la Mecánica Estadística 
- La densidad de estados nos permite conocer cómo se van a distribuir los estados disponibles en función de la Energía 
- La función de probabilidad de Fermi-Dirac nos dice cuál es la probabilidad de que un estado sea ocupado 
- Para los casos que se van a estudiar es posible utilizar la aproximación de Boltzmann 
- La Energía (Nivel) de Fermi representa el nivel energético más alto que puede tener un sistema a 𝑇 = 0𝐾 
- La Energía de Fermi está por encima de la Energía de Fermi Intrínseca para un SC tipo-n y debajo para un SC tipo-p 