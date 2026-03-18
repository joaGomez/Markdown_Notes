Una línea de transmisión es un dispositivo utilizado para transferir energía electromagnética de un punto a otro en forma eficiente.

![[Pasted image 20250930171509.png#center|250]]

- Balanceadas: Ambos conductores presentan la misma diferencia de potencial con respecto a un tercer conductor que hace de referencia (tierra).
- Desbalanceadas: Uno de los conductores es la referencia.

**Circuito de parámetros concentrados:** Cuando se aplica una tensión o corriente en un punto del circuito, las V e I del circuito reaccionan instantáneamente, es decir, se puede ignorar el tiempo de tránsito de la señal de un punto a otro. Además, no hay variación de tensión a lo largo de los cables de conexión entre elementos concentrados, se consideran volúmenes equipotenciales.
$$
t_{p} \ll T \to \frac{l}{c} \ll \frac{1}{f} \to l \ll \frac{c}{f}= \lambda
$$

**Circuito de parámetros distribuidos:** En una línea de transmisión ,la corriente que cruza secciones transversales a la línea y la tensión entre los conductores medida sobre una sección transversal dependen de la posición. En consecuencia, no se cumple Kirchhoff → No se pueden ignorar el tiempo de tránsito de la señal de un punto a otro.
$$
t_{p} > T \to \frac{l}{c} > \frac{1}{f} \to l > \frac{c}{f}= \lambda
$$
Si se cumple esta condición, puede considerar como línea de transmisión.

Aún así, el sistema debe considerarse como concentrado si $t_{p}<0.01T:$
$$
\begin{split}
&\frac{l}{\lambda}< 0.01 \qquad \text{Parámetros concentrados} \\
&\frac{l}{\lambda}\geq 0.01 \qquad \text{Parámetros distribuidos}
\end{split}
$$
**Obs:** A $50Hz$, $l>60km$ para ser considerado como línea de transmisión.
### Postulados de Heaviside y Kelvin
1) **Primer postulado:** Una línea uniforme, consiste en dos conductores rectos y paralelos, que mantienen la misma sección geométrica a lo largo de la LT.
2) **Segundo Postulado:** Las corrientes en los conductores de la línea, fluyen únicamente en la dirección de la longitud de la línea.
3) **Tercer Postulado:** En la intersección de cualquier plano transversal a la línea con sus conductores, las corrientes instantáneas totales en los dos conductores son iguales en magnitud, pero fluyen en direcciones opuestas. 
4) **Cuarto Postulado:** En la intersección de cualquier plano transversal a la línea de transmisión con sus dos conductores, hay un valor de diferencia de potencial única entre los conductores, en cualquier instante. 
5) **Quinto Postulado:** El comportamiento eléctrico de la línea, se describe completamente por cuatro coeficientes de circuito eléctrico distribuido, cuyos valores por unidad de longitud, son constantes en cualquier parte de la línea.
$$
\begin{split}
& R = \text{Resistencia total en serie / unidad de longitud} \\
& G = \text{Conductancia paralela / unidad de longitud} \\
& L = \text{Inductancia total en serie / unidad de longitud} \\
& C = \text{Capacidad en paralelo / unidad de longitud} \\
\end{split}
$$
#### Modelo de Heaviside
Para cada sección diferencial de la línea se cumplen las leyes de Kirchhoff:
![[Pasted image 20251001102024.png#center|250]]
Donde se debe cumplir que $\Delta z\ll \lambda$.
Los elementos del cuadripolo cuentan con las siguientes representaciones físicas:
- $R\left( \frac{\Omega}{m} \right):$ Resistencia de los conductores. Pérdida por efecto Joule.
- $L\left( \frac{H}{m} \right):$ Eneregía magnética almacenada alrededor de la línea.
- $G\left( \frac{1}{(\Omega m)} \right):$ Conductividad en el dieléctrico que separa los conductores.
- $C\left( \frac{F}{m} \right):$ Energía eléctrica almacenada entre los conductores.
### Parámetros y soluciones para una LT
Se define la impedancia característica como:
$$
Z_{o} = \frac{V_{o}^{+}}{I_{o}^{+}} = - \frac{V_{o}^{-}}{I_{o}^{-}}
$$
Se define el factor de velocidad como:
$$
K = \frac{v}{c_{0}}
$$
#### Sin pérdidas
**Parámetros:**
$$
\begin{split}
& v = \frac{\omega}{\beta} = \frac{1}{\sqrt{ LC }} = \frac{c_{0}}{\sqrt{ \varepsilon_{r} }}\\
& k = j\omega \sqrt{ LC } = j\beta \\
& Z_{o} = \sqrt{ \frac{L}{C} }
\end{split}
$$
**Soluciones:**
$$
\begin{split}
&V(z) = V_{o}{^{+}}e^{-j\beta z} + V_{o}{^{-}}e^{j\beta z} \\ 
&I(z) = \frac{1}{Z_{o}}(V_{o}{^{+}}e^{-j\beta z} - V_{o}{^{-}}e^{j\beta z})
\end{split}
$$

#### Con pérdidas
**Parámetros:**
$$
\begin{split}
& \gamma = \alpha +j\beta = \sqrt{ (R+j\omega L)(G+j\omega C) } \\ 
& v = \frac{\omega}{\beta} = \frac{1}{\sqrt{ LC }}\\
& Z_{o} = \sqrt{ \frac{R+j\omega L}{G+j\omega C} }
\end{split}
$$
**Soluciones:**
$$
\begin{split}
& V(z) = V_{o}{^{+}}e^{-\gamma z} + V_{o}{^{-}}e^{\gamma z} \\ 
& I(z) = \frac{1}{Z_{o}}(V_{o}{^{+}}e^{-\gamma z} - V_{o}{^{-}}e^{\gamma z})
\end{split}
$$
Las pérdidas en una LT se deben a:
- Pérdidas en el cobre:
	- Efecto Joule
	- Efecto skin
	- Cristalización
- Pérdidas en el dieléctrico → Efecto Joule
- Pérdidas por radiación:
	- La línea actua como antena
	- Depende de la separación entre los componentes
#### Bajas pérdidas
L y C dominan el comportamiento de la línea, pero no se puede despreciar R y G, lo que equivale a decir que:
$$
P_{\text{pérdidas}} \ll \langle P_{\text{almacenada en la línea}}\rangle \to \omega L\gg R \quad \omega C\gg G \quad G\simeq 0
$$
Con estas consideraciones, se cumple que:
$$
\gamma = \frac{1}{2} \left( R\sqrt{ \frac{C}{L} } + G \sqrt{ \frac{L}{C} } \right) + j\omega \sqrt{ LC } \Rightarrow
\begin{cases}
\alpha \simeq \frac{R}{2}\sqrt{ \frac{C}{L} } \\
\beta = \omega \sqrt{ LC }
\end{cases}
$$
**Impedancia característica:**
$$
Z_{o} = Z_{o}' + jZ_{o}''
$$
Donde $Z_{o}'= \sqrt{ \frac{L}{C} }$ y $Z_{o}'' = \frac{Z_{o}'}{2}\left( \frac{G}{\omega C} - \frac{R}{\omega L} \right)$, que si $\frac{G}{\omega C}\ll 1 \to Z_{o}''=- \frac{RZ_{o}'}{2\omega L}$. Además, para $f>50MHz: \frac{G}{\omega C}-\frac{R}{\omega L}$ es despreciable.

Debido a la velocidad finita de propagación, existe un retardo de las señales al atravesar la línea. Este retardo de propagación se define como:
$$
\tau = \frac{1}{v} = \sqrt{ LC }
$$
### Líneas sin distorsión
Con la condición $RC=GL$, queda que:
$$
\alpha = R\sqrt{ \frac{C}{L} }= \frac{R}{Z_{o}} \quad \beta = \omega \sqrt{ LC }
$$
![[Pasted image 20251001134248.png#center|350]]
### Sistema de referencia
Tomando el sistema de referencia de la siguiente forma:
![[Pasted image 20251001135718.png#center|350]]
Las soluciones quedan tal que:
$$
\begin{split}
& \text{Línea sin pérdidas} \begin{cases}
V(l) = V_{o}^{+}e^{j\beta l} + V_{o}^{-}e^{-j\beta l} \\
I(l) = \frac{1}{Z_{o}} (V_{o}^{+}e^{j\beta l} - V_{o}^{-}e^{-j\beta l})
\end{cases} \\
& \text{Línea con pérdidas} \begin{cases}
V(l) = V_{o}^{+}e^{\gamma l} + V_{o}^{-}e^{-\gamma l} \\
I(l) = \frac{1}{Z_{o}} (V_{o}^{+}e^{\gamma l} - V_{o}^{-}e^{-\gamma l})
\end{cases}
\end{split}
$$
### Coeficiente de reflexión
$$
\Gamma = \frac{V_{o}^{-}}{V_{o}^{+}} = \frac{Z_{L}-Z_{o}}{Z_{L}+Z_{o}}
$$
El coeficiente de reflexión es un número complejo, y se puede determinar su valor en cualquier punto de la línea como:
$$
\Gamma(z) = \frac{\Gamma V_{o}^{+}e^{j\beta z}}{V_{o}^{+}e^{-j\beta z}} = \Gamma e^{2j\beta z} = |\Gamma|e^{j(\phi-2\beta z)}
$$
### Coeficiente de transimisión
$$
\tau = \frac{V_{L}}{V_{o}^{+}} = 1 + \Gamma = \frac{2Z_{L}}{Z_{o}+Z_{L}}
$$
### Onda estacionaria
La onda estacionaria es el resultado de la interferencia entre la onda directa y la reflejada, y se expresa como:
$$
|V(z)| = |V_{o}^{+}|\sqrt{ 1+|\Gamma|^{2} + 2|\Gamma|\cos(2\beta z+\phi)}
$$
**Obs:** El período de repetición espacial para la O.E es $\frac{\lambda}{2}$, mientras que el período de repetición para la directa y la reflejada es $\lambda$.

Se define su valor instantáneo como:
$$
\text{Valor instantáneo} \qquad V(z,t) = Re(V(z)\cdot e^{j\omega t})
$$
$$V(z,t)=\underbrace{|V_0^+|(1 - |\Gamma|)\cos(\omega t - \beta z)}_{\text{Onda viajera}}
\quad + \quad
\underbrace{2|V_0^+||\Gamma|\cos\!\left(\beta z + \tfrac{\phi}{2}\right)\cos\!\left(\omega t + \tfrac{\phi}{2}\right)}_{\text{Onda estacionaria}}
$$
El máximo será con la suma de las dos ondas → $|V_{max}|= |V_{o}^{+}|(1+|\Gamma|)$, y el mínimo será cuando la onda estacionaria es nula → $|V_{min}| = |V_{o}^{+}|(1-|\Gamma|)$
#### Relación de onda estacionaria
$$
ROE = \rho = \frac{|V_{max}|}{|V_{min}|} = \frac{1+|\Gamma|}{1-|\Gamma|}
$$
Se define la **pérdida de retorno** como $RL(dB) = -20\log(|\Gamma|)$

A partir de la definición de ROE, también se puede obtener el coeficiente de reflexión:
$$
|\Gamma| = \frac{ROE-1}{ROE+1}
$$
### Impedancia de entrada
Tomando con la referencia del 0 donde está la carga, la impedancia de entrada será evaluada en $z=-l$, por lo tanto:
$$
Z_{in}= Z_{o}\cdot \frac{Z_{L}+Z_{o}\tanh(\gamma l)}{Z_{o}+Z_{L}\tanh(\gamma l)}
$$
**Obs:** Si la línea es muy larga ($l\to \infty$) entonces $Z_{in}\to Z_{o}$.
#### A circuito abierto
Se toma $Z_{L}=\infty$ e $I_{L}=0$ → Sin pérdida: $Z_{CA} = Z_{o}\coth(\gamma l)$
#### A cortocircuito
Se toma $Z_{L}=0$ e $I_{L}=0$ → Sin pérdida: $Z_{CC} = Z_{o}\tanh(\gamma l)$

A partir de estos ensayos, obtenemos:
$$
\begin{split}
& Z_{o} = \sqrt{ Z_{CC}\cdot Z_{CA} } \\ 
& \beta = - \frac{1}{l} tg^{-1}\left( \sqrt{ \frac{Z_{CC}}{Z_{CA}} } \right) \\
& \gamma = \frac{1}{l} \tanh^{-1}\left( \sqrt{ \frac{Z_{CC}}{Z_{CA}} } \right)
\end{split}
$$
En particular,  para una LT sin pérdidas de longitud de un cuarto de longitud de onda, la impedancia de entrada será:
$$
Z_{in}\left( \frac{\lambda}{4} \right) = \frac{Z_{o}^{2}}{Z_{L}}
$$
**Obs:** Los casos analizados de CA y CC, son casos especiales de líneas de longitud de un cuarto de longitud de onda.
### Potencia media temporal
La potencia media temporal está dada por:
$$
\langle P(z)\rangle = \frac{1}{T}\int_{0}^{T} V_{i}(z,t)\cdot I_{i}(z,t)  \, dt \underbrace{\longrightarrow}_{\text{funciones armónicas}} \langle P(z)\rangle = \frac{1}{2} Re(V(z)\cdot I^{*}(z))
$$
Además:
$$
\begin{split}
& \langle P^{+} \rangle = \frac{|V_{o}^{+}|^{2}}{2Z_{o}} \\
& \langle P^{-} \rangle = -|\Gamma|^{2}\frac{|V_{o}^{+}|^{2}}{2Z_{o}}
\end{split}
\quad \to \quad \langle P \rangle = \langle P^{+} \rangle + \langle P^{-} \rangle = \frac{|V_{o}^{+}|^{2}}{2Z_{o}} (1-|\Gamma|^{2})
$$
Si la línea no tiene pérdidas → $\langle P_{\text{línea}} \rangle = 0 \to \langle P_{L} \rangle = \langle P \rangle$
$$
\begin{split}
& \text{Fracción de potencia reflejada} \qquad \qquad \qquad  p=|\Gamma|^{2} & \\
& \text{Fracción de potencia entregada a la carga} \quad  p_{L} = 1-|\Gamma|^{2}= \frac{4\cdot ROE}{(1+ROE)^{2}} &
\end{split}
$$
#### Bajas pérdidas
$$
\langle P(z) \rangle = \frac{|V_{o}^{+}|^{2}}{2Z_{o}} e^{-2\alpha z} - |\Gamma|^{2}\frac{|V_{o}^{+}|^{2}}{2Z_{o}} e^{2\alpha z}
$$
### Discontinuidad
Dos líneas de impedancias características $Z_{o1}$ y $Z_{o2}$ conectadas en serie, siendo la segunda de ellas terminada en una carga adaptada.
$$
\frac{V_{o}^{++}}{Z_{o2}} = \frac{V_{o}^{+}}{Z_{o1}} - \frac{V_{o}^{-}}{Z_{o1}}
$$Al tener un cambio de impedancia, va a haber una onda reflejada y otra transmitda.
$$
\Gamma_{12} = \frac{Z_{o_{2}}-Z_{o_{1}}}{Z_{o_{1}}+Z_{o_{2}}} \quad \wedge \quad \tau_{12} = 1 + \Gamma_{12}
$$
Entpnces, se cumplirá que:
$$
\begin{split}
& V(z) = V_{o}^{+} (e^{-\gamma_{1}z}+ \Gamma_{12}e^{\gamma_{1}z}) \quad & \text{para } z<0 \\ 
& V (z) = \tau_{12}V_{o}^{+} e^{-\gamma_{2}z} \qquad & \text{para } z>0
\end{split}
$$
#### Adaptación de impedancias
El objetivo de la adaptación es no tener reflexión.

Tomando $l= \frac{\lambda}{4}$, la impedancia vista al final de la linea $Z_{o}$ será:
$$
Z_{ in } = \frac{Z_{o}^{2}}{Z_{L}} = \frac{Z_{o_{1}}^{2}}{Z_{o_{2}}}
$$
![[Pasted image 20251002193120.png#center|150]]
La adaptación entonces ocurre si:
$$
Z_{ in } = Z_{o} \quad \longrightarrow  \quad Z_{o_{1}} = \sqrt{ Z_{o_{2}} Z_{o}}
$$
Por lo tanto, lo que ocurrirá será:
1. No existirá onda estacionaria en la línea $Z_{o}$ , pero sí en $Z_{o_{1}}$ . 
2. La condición de adaptación se repite cada $(2n+1)\lambda/4$. 
3. La adaptación es dependiente de la frecuencia (a través de $\lambda$). 
4. El método sólo adapta cargas reales (o líneas sin pérdidas).
### Transitorio
Para estos casos, se considera la linea desconectada en un instante inicial, y partir del cierre de una llave se conecta la linea y se observa el comportamiento.

Una vez cerrada la llave, la señal comienza a avanzar por el circuito, pero hasta no llegar a la carga (fisicamente), esta aún no se refleja, lo que quiere decir que aún no percibe el efecto de su impedancia. Por lo tanto, instantáneamente, la tensión a la entrada de la linea será:
$$
V^{+} = V_{g}\cdot \frac{Z_{o}}{Z_{o}+R_{g}}
$$
Una vez la señal llega a la carga, se observa que parte de esta se refleja y cual se transmite. A partir de esto, se observa que ocurre con la señal reflejada y asi sucesivamente, ya que los valores de tensión y corriente se van a ir sumando con las reflexiones de estas y de aqui surge el diagrama de rebotes:
![[Pasted image 20251002210929.png#center|450]]
**Condición de estado estacionario:** La suma de todos los rebotes, más la condición inicial, será el resultado estacionario. En particular, en estado estacionario, la linea de transmisión actua como cable → $V_{L}=V_{g}\cdot \frac{R_{L}}{R_{g}+R_{L}}$

| Relación de impedancias | Entrada                   |
| ----------------------- | ------------------------- |
| $Z_{g}>Z_{o}$           | Sobre amortiguado         |
| $Z_{g}<Z_{o}$           | Sub amortiguado (Ringing) |
| $Z_{g}=Z_{o}$           | Criticamente amortiguado  |
#### Discontinuidades
Al conectar lineas en cascada, también se debe analizar su comportamiento transitorio. Para ello, será importante determinar el coeficiente de reflexión entre estas. Por lo tanto, su onda reflejada será $V\cdot \Gamma$, y la transmitida $V\cdot \tau=V= (1+\Gamma)$. Los coeficientes de la discontinuidad serán determinados tal que:
$$
\Gamma_{\text{discontinuidad}} = \frac{V^{-}}{V^{+}} = \frac{Z_{o_{2}}-Z_{o_{1}}}{Z_{o_{2}}+Z_{o_{1}}} \quad \wedge \quad \tau_{\text{discontinuidad}} = \frac{V^{++}}{V^{+}} = \frac{V^{+} + V^{-}}{V^{+}} = 1 + \Gamma_{\text{discontinuidad}}
$$
### Pulsos en líneas
A la hora de estudiar el comportamiento de una línea frente a un tren de pulsos en la entrada, es importante entender que el escenario donde hay un pulso incidente y otro reflejado en simultáneo es factible. Para resolver esto, se puede aplicar el principio de superposición. Esta superposición va a verse reflejada en el diagrama de rebotes de la siguiente forma:

![[Pasted image 20251003191429.png#center|300]]
### Señales digitales y ringing
Como se vio en uno de los incisos anteriores, a altas frecuencias, una pista de PCB puede actuar como línea de transmisión, y puede ocurrir este fenómeno llamado **ringing**. Esto va a generar que, lo que a priori es una pista y su conexión a los demás puntos de la placa son equipotenciales, ahora será una especie de filtro que va a afectar el comportamiento de mi circuito. En particular, el fenómeno de ringing ocurre cuando el comportamiento de la pista es subarmortiguado.

![[Pasted image 20251003192247.png#center|450]]
### Reflectómetro
Este dispositivo se utiliza para medir reflexiones en una línea, para detectar problemas , tales como roturas en la misma.

Dado el siguiente diagrama:
![[Pasted image 20251003192405.png#center|550]]
Al conectar una carga con la misma impedancia que la $Z_{o}$ de la línea, lo que se esperaría sería que no haya reflexión, por lo que si detectamentos alguna en particular, se puede decir que hay una falla en algún punto de la línea.

El reflectómetro lo que hace es determinar la distancia de la llama a partir del tiempo que tarda en detectar una señal reflejada.

Sea la distancia a la falla en $D_{f}$, entonces:
$$
D_{f} = v\cdot \frac{t_{d}}{2} \to \Gamma_{d} = \frac{V_{in}-V_{o}^{+}}{V_{o}^{+}}
$$
![[Pasted image 20251003193019.png#center|400]]
### Discontinuidades en PCB
Se deben eliminar todas las características reflexivas mayores que $\frac{\lambda}{10}$, además de los cambios de impedancia.
![[Pasted image 20251003193257.png#center|400]]
### Rise time y retardo de propagación
A partir del tiempo que tarda una señal en propagarse y el tiempo de rise, se puede definir una regla para determinar si es o no una línea de transmisión:
$$
\begin{split}
& \text{Línea de transmisión (parámetros distribuidos)} \quad t_{r}<2.5\cdot t_{p} \\
& \text{Línea equipotencial (parámetros concentrados)} \quad t_{r}>6\cdot t_{p}
\end{split}
$$
El intervalo entre estos puntos va a depender del caso.