#### Juntura en equilibrio
Al poner en contacto un SC tipo-p con uno tipo-n se va a producir difusión de los electrones del lado n hacia el lado p y de huecos del lado p hacia el lado n. Este proceso se denomina **inyección de minoritarios**. Los electrones que se difunden del lado n hacia el lado p dejan atrás impurezas ionizadas con carga positiva. Los huecos que se difunden del lado p hacia el lado n dejan atrás impurezas ionizadas con carga negativa. Las impurezas ionizadas están fijas y no pueden moverse y forman lo que se denomina zona desierta. Las áreas con portadores móviles se denominan zonas neutrales.
![[Pasted image 20240327184121.png#center]]
**Obs:** Las cargas en la zona desierta generan un campo eléctrico el cual es el responsable de la corriente de drift. Una vez que esta corriente iguala a la de difusión se llega al equilibrio.

Mediante este esquema surgen las igualdades:
$$\begin{split}
\vec{J}_{e|diff}=-\vec{J}_{e|drift} \\
\vec{J}_{h|diff}=-\vec{J}_{h|drift}
\end{split}$$
###### Diagrama de bandas
Para una juntura en equilibrio la energía de Fermi se mantiene cte. Esto produce que las bandas se doblen.

A su vez, aparece una barrera de potencial $qV_{bi}$ que impide que los electrones y los huecos sigan difundiéndose.

![[Pasted image 20240327185025.png#center]]

Donde $V_{bi}= V_{T}\cdot ln(\frac{N_{A}N_{D}}{n_{i}^{2}})$ y $V_{T}= \frac{kT}{q}$ (voltage térmico).
Además, $(E_{i}-E_{F})_{p-side}= kT\cdot ln(\frac{N_{A}}{n_{i}})$ y $(E_{F}-E_{i})_{n-side}= kT\cdot ln(\frac{N_{D}}{n_{i}})$.
#### Electroestática de la zona desierta
Asumimos juntura abrupta, es decir, la zona desierta del lado $n$ termina en $x_{n}$ y del lado $p$ en $x_{p}$.

![[Pasted image 20240327185436.png#center]]

$$\rho(x)= \begin{cases}
qN_{A} \qquad -x_{p}<x<0 \\ 
qN_{D} \qquad 0<x<x_{n} \\
0 \qquad x>x_{n} \lor x< -x_{p}
\end{cases}$$
![[Pasted image 20240327185734.png#center]]
$$E(x)= \begin{cases}
\frac{-qN_{A}}{\varepsilon_{s}}(x+x_{p}) \qquad -x_{p}\leq x\leq 0 \\ 
\frac{-qN_{D}}{\varepsilon_{s}}(x_{n}-x) \qquad 0\leq x\leq x_{n} \\
0 \qquad x>x_{n} \lor x< -x_{p}
\end{cases} → ~E_{MAX}=\frac{-qN_{D}}{K_{s}\epsilon_{0}}x_{n}=\frac{-qN_{A}}{K_{s}\epsilon_{0}}x_{p}$$
![[Pasted image 20240327190835.png#center]]
$$V_{bi}(x=x_{n})= \frac{q}{2\varepsilon_{s}}(N_{D}x_{n}^{2}+N_{A}x_{p}^{2})$$
![[Pasted image 20240327191019.png#center]]
Donde se define la **permitividad del silicio** como:
$$\varepsilon_{s}= \varepsilon_{r}\cdot \varepsilon_{0}= 1.04*10^{-14} \frac{F}{cm}$$
El ancho de la zona desierta se encuentra dado por las siguientes expresiones:
$$x_{p}=\sqrt{\frac{2\varepsilon_{s}V_{bi}}{q}(\frac{N_{D}}{N_{A}(N_A +N_{D})})} \qquad x_{n}=\sqrt{\frac{2\varepsilon_{s}V_{bi}}{q}(\frac{N_{A}}{N_{D}(N_A +N_{D})})} \qquad W=\sqrt{\frac{2\varepsilon_{s}V_{bi}}{q}(\frac{1}{N_{A}}+\frac{1}{N_{B}})}$$
- En una juntura con el lado $p$ más dopado que el lado $n$ ($p^{+}n$) → $N_{A}>>N_{D} -> x_{n}>>x_{p}$.
- En una juntura con el lado $n$ más dopado que el lado $p$ ($pn^{+}$) → $N_{D}>>N_{A} -> x_{p}>>x_{n}$.
*La zona desierta es mayor del lado menos dopado.*
#### Juntura en directa
La polarización en directa permite disminuir la barrera de potencial favoreciendo la difusión de mayoritarios (electrones del lado n y huecos del lado p). Los mayoritarios difundidos pasan a ser minoritarios en el lado opuesto (los electrones del lado p y los huecos del lado n). Aparece una corriente de difusión Las energías de Fermi ya no son iguales (𝐸𝐹 será menor en el lado con tensión positiva). Lejos de la zona desierta, los minoritarios van a terminar recombinándose con los mayoritarios. El campo eléctrico aplicado es opuesto al generado dentro de la zona desierta, por lo tanto el campo eléctrico resultante será menor al de equilibrio. La corriente de drift disminuye. La zona desierta debe disminuir en relación al equilibrio ya que el campo eléctrico es menor. Se asume baja inyección, es decir, la concentración de mayoritarios no cambia: la concentración de electrones del lado n y hueco del lado p no cambia con respecto al equilibrio.
![[Pasted image 20240327193157.png#center]]

|     Notación      |                    Significado                     |
| :---------------: | :------------------------------------------------: |
|     $n_{n0}$      | Electrones de lado n en equilibrio (Mayoritarios)  |
|     $p_{p0}$      |   Huecos del lado p en equilibrio (Mayoritarios)   |
|     $p_{n0}$      |   Huecos del lado n en equilibrio (Minoritarios)   |
|     $n_{p0}$      | Electrones del lado p en equilibrio (Minoritarios) |
|    $p_{n}(x)$     |    Huecos del lado n en función de la distancia    |
|    $n_{p}(x)$     |  Electrones del lado p en función de la distancia  |
| $\Delta p_{n}(x)$ |    Exceso de huecos (minoritarios) en el lado n    |
| $\Delta n_{p}(x)$ |  Exceso de electrones (minoritarios) en el lado p  |
#### Concentración de minoritarios
- Lado p:
$$p_{p0}\sim N_{A} \quad n_{p0}=n_{n0}\cdot e^{\frac{V_{bi}}{V_{T}}}\quad n_{p}(-x_{p})=n_{p0}\cdot e^{\frac{V_{a}}{V_{T}}}\quad \Delta n_{p}=n_{p}(x)-n_{p0}$$
- Lado n:
$$n_{n0}\sim N_{D} \quad p_{n0}=p_{p0}\cdot e^{\frac{V_{bi}}{V_{T}}}\quad p_{n}(x_{n})=p_{n0}\cdot e^{\frac{V_{a}}{V_{T}}}\quad \Delta p_{n}=p_{n}(x)-p_{n0}$$
#### Distribución de minoritarios
Se utilizará la distribución mediante las siguientes aproximaciones:
- El campo eléctrico es cero fuera de la zona desierta.
- La generación es cero $GL = 0$.
- Estado estacionario $\frac{\partial\Delta p_{n}}{\partial t} = 0$.
- El ancho de la zona neutral ≫ longitud de difusión. Esto se conoce como **juntura larga**
Además, las condiciones de contorno son:
- $p_{n}(x_{n})=p_{n0}\cdot e^{\frac{V_{a}}{V_{T}}},x\to \infty: p_{n}=p_{n0}$
- $n_{p}(-x_{p})=n_{p0}\cdot e^\frac{V_{a}}{V_{T}},x\to -\infty: n_{p}=n_{p0}$
$$\begin{split}
\frac{\partial^{2}(\Delta p_{n})}{\partial x^{2}} - \frac{\Delta p_{n}}{L_{p}^{2}}=0  \longrightarrow \Delta p_{n}(x)=p_{n0}\cdot (e^{\frac{V_{a}}{V_{T}}}-1)\cdot e^{\frac{x_{n}-x}{L_{p}}} \qquad x\geq x_{n} \\
\frac{\partial^{2}(\Delta n_{p})}{\partial x^{2}} - \frac{\Delta n_{p}}{L_{n}^{2}}=0  \longrightarrow \Delta n_{p}(x)=n_{p0}\cdot (e^{\frac{V_{a}}{V_{T}}}-1)\cdot e^{\frac{x_{p}+x}{L_{p}}} \qquad x\leq x_{p}
\end{split}$$
#### Corriente de juntura
Al no haber recombinación en la zona desierta, los portadores que lleguen a $x_{n}$ y $−x_{p}$ van a pasar del otro lado → **La corriente en todo el diodo es constante**.
$$\begin{split}
J_{p}(x_{n})= \frac{qD_{p}p_{n0}}{L_{p}}\cdot (e^{\frac{V_{a}}{V_{T}}-1)}\\
J_{n}(-x_{p})= \frac{qD_{n}n_{p0}}{L_{n}}\cdot (e^{\frac{V_{a}}{V_{T}}-1)}
\end{split}
\begin{cases} 
J_{total}= J_{0}\cdot (e^\frac{V_{a}}{V_{T}}-1) \\
J_{0}= \frac{qD_{p}p_{n0}}{L_{p}}+\frac{qD_{n}n_{p0}}{L_{n}}
\end{cases}$$
Donde $I= I_{0}\cdot (e^{\frac{V_{a}}{V_{T}}}-1)$ y $I_{0}=~Área \cdot J_{0}$
![[Pasted image 20240327203640.png#center]]
#### Juntura en inversa
La polarización en inversa aumenta la barrera de potencial con respecto a su valor en equilibrio, bloqueando aún más la difusión de portadores. El campo eléctrico aplicado tiene el mismo sentido al generado dentro de la zona desierta, por lo tanto el campo eléctrico resultante será mayor al de equilibrio. Esto hará que portadores cerca de la zona desierta sean acelerados hacia el lado opuesto. La corriente en inversa está dada por el drift de minoritarios. Al tener un campo eléctrico mayor, la zona desierta debe aumentar en relación al equilibrio. Las energías de Fermi no son iguales (𝐸𝐹 será menor en el lado con tensión positiva). Las ecuaciones que describen la concentración de portadores en polarización directa siguen siendo válidas, sólo que la tensión aplicada ahora será negativa. La ecuación del diodo ideal sigue siendo válida, pero al ser el exponente negativo, la parte exponencial tiene rápidamente a cero para bajos valores de polarización. Por lo tanto, en polarización inversa resulta $I\sim -I_{0}$.
![[Pasted image 20240327203836.png#center]]
#### Breakdown
Si la tensión en inversa sigue aumentando se puede llegar a la ruptura del diodo. Esta tensión se denomina **tensión de breakdown**. Una vez que se llega a la tensión de ruptura la corriente aumenta drásticamente. No es necesariamente destructivo. De hecho hay diodos diseñados especialmente para trabajar en esa zona, por ejemplo el diodo zenner. 

![[Pasted image 20240327204014.png#center]]

Hay dos mecanismos principales de breakdown: 
- Zener Breakdown: Se basan en el efecto túnel (tunneling): al aplicar una tensión en inversa suficiente, la banda de conducción del lado n se encuentra por debajo de la banda de valencia del lado p. Los electrones en la banda de valencia del lado p “ven” estados permitidos del lado n con bajo nivel energético para volverse electrones libre y atraviesan la barrera de potencial. Ocurre en diodos muy dopados (para disminuir el ancho de la zona desierta) y con una tensión en inversa moderada.
![[Pasted image 20240327204052.png#center]]
- Avalanche Breakdown: Ocurre en diodos poco dopados y se necesita mucha tensión en inversa. El campo eléctrico en la zona desierta es tan grande que ocurre el impacto iónico: un electrón libre (minoritario) de la zona p es acelerado fuertemente por el campo eléctrico hacia el otro lado y colisiona con átomos de la red. Esta colisión ioniza al átomo, generando un par electrón-hueco. A su vez, estos son acelerados, creando nuevos pares electrón-hueco. Este proceso continúa provocando un efecto avalancha que hace que la corriente crezca rápidamente.
#### Conclusiones
- Al juntar un material tipo-p con uno tipo-n se produce difusión de electrones hacia el lado p y de huecos hacia el lado n.
- La difusión genera una zona desierta en la cual aparece un campo eléctrico y una barrera de potencial que impiden que la difusión continue en equilibrio.
- Si se aplica una tensión positiva del lado p y una negativa del lado n se dice que la juntura está en directa.
- La juntura en directa disminuye la barrera de potencial y favorece la aparición de una corriente de difusión.
- Si se aplica una tensión positiva del lado n y negativa del lado p se dice que la juntura está en inversa.
- La juntura en inversa aumenta la barrera de potencial y aumenta el campo eléctrico en la zona desierta.
- La corriente en inversa es muy pequeña y está dada por el drift de minoritarios.
- Aumentar la tensión en inversa produce la ruptura del diodo, ya sea por efecto túnel o por avalancha.
#### Modelo circuital del diodo
Planteo 3 escenarios(modelos): Cuando el diodo no conduce (Circuito abierto, hasta que consiga la tensión que me pide el diodo). Cuando el diodo conduce y actúa como caída de tensión, esto funcionará hasta que la tensión de la senoidal sea negativa, en ese instante el diodo rectifica la tensión y actúa como circuito abierto nuevamente. El último modelo surge de entender que el diodo tiene una resistencia interna, por lo que actúa como el modelo anterior pero la caída de tensión no es tan abrupta. El problema de esto es que obtengo un comportamiento alineal.

![[Pasted image 20240404190334.png#center|350]]
$$I=I_{0}(e^{\frac{V_{D}}{V_{T}}}-1)\to R=r_{e}=\frac{V_{T}}{I}=\frac{V_{T}}{I_{0}(e^{\frac{V_{D}}{V_{T}}}-1)}\qquad Ec.~del~diodo$$
**Obs:** $r_{e}$ es la resistencia estática, y tiene un comportamiento alineal.

**Punto DC:** En este punto me muevo de a pasos muy pequeños, y mediante esto, puedo asumir un comportamiento lineal. Es decir, si limito el desplazamiento de la curva $I-V$ alrededor de un punto de polarización $Q$ (limitando el rango de la señal alterna), la resistencia se va a poder linearizar usando la serie de Taylor
$$r_{d}= \frac{V_{T}}{I_{o}\cdot e^{\frac{V_{Q}}{V_{T}}}}=\frac{V_{T}}{I_{Q}}$$
**Obs:** Esta expresión valdrá en el rango que se cumpla $V_{D} - V_{Q} << 2V_{T}$.

**Recuerdo:** $V_{T}= \frac{kT}{q} \simeq 26mV$.
### Capacidades
La capacidad está definida como el cambio de carga almacenada debido a un cambio en la tensión: $C = \frac{\partial Q}{\partial V}$

**Obs:** El hecho de tener carga almacenada y sus variaciones con la tensión definirán la máxima velocidad a la cual puede operar la juntura.
##### Capacidad de juntura
Al variar la tensión de polarización varía el ancho de la zona desierta. La zona desierta acumula cargas cuya cantidad variará en función de la tensión. La capacidad en la zona desierta puede aproximarse como un capacitor de placas paralelas $C= \frac{\varepsilon \cdot A}{d}$
![[Pasted image 20240404192412.png#center|400]]
$$\begin{split}
d=W=Ancho~de~la~zona~desierta \\
C_{j}= \frac{C_{j0}}{\sqrt{1- \frac{V_{A}}{V_{bi}}}} \\
C_{j0}= \frac{\varepsilon_{s} \cdot A}{\sqrt{\frac{2\cdot \varepsilon_{s}\cdot V_{bi}}{q}(\frac{1}{N_{A}}+\frac{1}{N_{D}})}}
\end{split}$$
##### Capacidad de difusión
Ocurre debido a las cargas de minoritarios presentes cerca de la zona desierta. Al variar la tensión de polarización, varía la cantidad de portadores difundidos. Este cambio en la carga da origen a la capacidad de difusión.
$$C_{d}= \frac{q\cdot A}{V_{T}}\left(L_{n}n_{p0}+L_{p}p_{n0}\right) \cdot e^{\frac{V_{A}}{V_{T}}}$$
![[Pasted image 20240404193140.png#center]]
##### Capacidad total
La capacidad total estará dada por la suma de la capacidad de juntura y la de difusión. En inversa domina la capacidad de juntura mientras que en directa domina la capacidad de difusión. El modelo del diodo planteado anteriormente puede completarse incluyendo estas capacidades.
![[Pasted image 20240404193253.png#center|400]]
