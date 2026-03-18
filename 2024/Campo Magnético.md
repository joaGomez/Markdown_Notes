----
Por el momento, la idea de campo magnético se puede pensar como la región del espacio que rodea cualquier carga eléctrica en **movimiento**.Un campo magnético también rodea una sustancia magnética que forma un imán permanente.
##### Obs
Los imanes cuentan con dos tipos de polos magnéticos, polo Norte y Sur, ambos siendo las regiones donde el campo magnético es más intenso.
Además, polos de igual tipo (signo) se repelen, y de distinto tipo se atraen.
En la actualidad, sabemos que es imposible separar los polos magnéticos, es decir, no existen los monopolos magnéticos.
##### Obs
A diferencia del campo eléctrico, las líneas de campo del campo magnético son cerradas, van desde el polo norte al polo sur por fuera del imán, y de sur a norte por dentro del mismo. Es por esto que la expresión queda tal que: $\vec{\nabla}.\vec{B}=0$
![[Pasted image 20230925094857.png|200]]
### Fuerza magnética sobre una carga en movimiento
Teniendo en cuenta las siguientes observaciones sobre el campo magnético, se deduce la siguiente expresión:
$$\vec{F_{B}}=q~\vec{v}\times \vec{B} \longrightarrow F_{B}=|q|vBsen~\theta$$
### Regla de la mano derecha
![[Pasted image 20230925100027.png|350]]
##### Obs
![[Pasted image 20230925101015.png|300]]
### Partícula cargada en un campo uniforme de inducción magnética
Suponiendo un campo $\vec{B}$ uniforme y $\vec{v_{0}}$ la velocidad inicial de la partícula:
- Si $\vec{v_{0}} = 0$ → La fuerza magnética será nula y la partícula permanecerá en reposo.
- Si $\vec{v_{0}} ~ || ~ \vec{B}$ → $\vec{F_{B}}=0$ y $\vec{v}=\vec{v_{0}}$ cte.
- Si $\vec{v_{0}} ~ \bot ~ \vec{B}$ : $\vec{F_{B}} ~ \bot ~ \vec{v_{0}}$ → La rapidez se mantendrá cte. y la partícula comenzará a describir un MCU.
![[Pasted image 20230925101141.png#center|150]]
##### Obs
La fuerza magnética no realiza trabajo y por ello la rapidez se mantiene cte. → $W_{AB,C}=\Delta K_{AB}=0$.

> Por sumatoria de fuerzas: $\sum\limits \vec{F}=m\vec{a}$ y $\vec{a}=a_{t}\hat{t}+a_{n}\hat{n}$, con $a_{t}=0$
> Luego, $\vec{v}=\vec{v_{||}}+\vec{v_{\bot}}$ → $\vec{v_{||}}= cte$. Y además, $||\vec{v_{\bot}}||=v_{\bot}=cte$, porque el movimiento es circular uniforme.
> Además;
> - $F_{B}=\frac{mv^{2}}{r}$, $r=\frac{mv}{qB}$, $\omega= \frac{v}{r} = \frac{qB}{m}$, $T= \frac{2\pi m}{qB}$
### Fuerza de Lorentz
Se define la fuerza de Lorentz sobre una carga en movimiento en presencia tanto de un campo eléctrico y un campo magnético.
$$\vec{F}=q\vec{E}+q\vec{v}\times\vec{B}$$
### Fuerza sobre un conductor con corriente eléctrica en un campo magnético
$$\vec{F_{B}}=I\vec{L}\times\vec{B}$$
Esta expresión es el resultado de una fuerza ejercida sobre un conductor uniforme, pero si queremos ser un poco más generales a la hora de calcular esta fuerza, para cualquier tipo de conductor, utilizaremos un diferencial de longitud para cada infinitésimo de segmento con presencia de campo magnético.
$$d\vec{F_{B}}=Id\vec{s}\times \vec{B} \Rightarrow \vec{F_{B}}=I\int_{a}^{b}d\vec{s}\times \vec{B}$$
### Momento de torsión en un campo magnético uniforme
Para el momento de torsión tenemos que pensar en la fuerza magnética que afecta una espira con corriente en presencia de un campo uniforme. Si la corriente es paralela al campo, no habrá fuerza magnética, por lo que no va a haber momento. En cambio, si éstas no lo son, aparecerá una fuerza magnética y por ende la espira podrá oscilar acorde al momento de torsión que aparece.
La expresión para el momento de torsión ejercido sobre una espira colocado en un campo uniforme $\vec{B}$ es:
$$\vec{\tau}=I\vec{A}\times \vec{B}$$
El producto $I\vec{A}$ representa el **momento dipolar magnético** $\vec{\mu}$, tal que $\vec{\mu}\equiv I\vec{A}$, y en una bobina con $N$ espiras: $\vec{\mu}=NI\vec{A}$.
Entonces, el momento de torsión puede quedar expresado como: $\vec{\tau}=\vec{\mu}\times \vec{B}$

Sea $U_{B}$ la energía potencial de un sistema constituido por un dipolo magnético en un campo magnético, entonces:
$$U_{B}=-\vec{\mu}.\vec{B}$$
Donde $U_{min}=-\mu B$, cuando $\vec{\mu}$ y $\vec{B}$ apuntan en la misma dirección. Y $U_{max}=+\mu B$, cuando $\vec{\mu}$ y $\vec{B}$ apuntan en direcciones opuestas.
### Efecto Hall
Cuando se coloca un conductor de corriente en un campo magnético, se genera una diferencia de potencial en una dirección perpednicular tanto a la corriente como al campo magnético.
![[Pasted image 20231005081034.png|200]]
En la deducción de una expresión que defina el voltaje Hall, primero observe que la fuerza magnética ejercida sobre los portadores tiene una magnitud igual a $qv_{d}B$. En reposo, esta fuerza está equilibrada por la fuerza eléctrica $qE_{H}$, donde $E_{H}$ es la magnitud del campo eléctrico debido a la separación de las cargas (conocido a veces como campo Hall). Debido a eso:
$$\begin{split}
& qv_{d}B=qE_{H} \to E_{H}=v_{d}B \\
Además, \quad &\Delta V_{H}=E_{H}d=v_{d}Bd \\
v_{d}= \frac{I}{nqA} \Rightarrow~ &\Delta V_{H}=\frac{IBd}{nqA}= \frac{IB}{nqt}
\end{split}$$
![[Pasted image 20231005081100.png|650]]
**Obs.** $R_{H}=\frac{1}{nq}$ es el **coeficiente de Hall**.
### Ley de Biot-Savart
$$d\vec{B}=\frac{\mu_{0}}{4\pi}\frac{Id\vec{s}\times\hat{r}}{r{^{2}}}\Rightarrow \vec{B}=\frac{\mu_{0}I}{4\pi}\int\frac{d\vec{s}\times\hat{r}}{r{^{2}}}$$
Con $\mu_{0}=4\pi.10^{-7} \frac{T.m}{A}$, la **permeabilidad del espacio libre**. Y $\hat{r}=\frac{\vec{r}}{|r|}$.
**Obs.** $B= \frac{\mu_{0}I}{2\pi a}$, campo magnético de un alambre infinito, siendo a la distancia al punto P donde quiero calcular el campo.
### Fuerza magnética entre dos conductores paralelos
La fuerza que siente un conductor es perpendicular al campo generado por el conductor paralelo.
![[Pasted image 20231005084941.png|200]]
Para este caso, la fuerza que aparece en el conductor 1 es:
$$F_{1}=I_{1}lB_{2}=I_{1}l(\frac{\mu_{0}I_{2}}{2\pi a})=\frac{\mu_{0}I_{1}I_{2}}{2\pi a}l$$
### Ley de Ampere
Se define la integral de línea del campo magnético por el segmento conductor alrededor de cualquier trayectoria cerrada. Donde $I$ es la corriente total estable que pasa a través de cualquier superficie limitada por la trayectoria cerrada:
$$\oint \vec{B}.d\vec{s}=B\oint ds=\frac{\mu_{0}I}{2\pi r}(2\pi r)=\mu_{0}I_{c}$$
**Obs.** El flujo magnético neto a través de cualquier superficie cerrada siempre es igual a cero: $\oint \vec{B}.d\vec{A}=0$
**Obs.** Para un conductor que lo puedo encerrar con una circunferencia: $|\vec{B}|= \frac{\mu_{0}I_{c}}{2\pi r}$, donde $I_{c}= \iint\vec{\mathcal{J}}.d\vec{A}$, y $\mathcal{J}= \frac{i}{Área~encerrada}$ 

> Obs
> Campo magnético de un solenoide: $B=\mu_{0} \frac{N}{l}I=\mu_{0}nI$
> Campo magnético de un toroide: $B=\frac{\mu_{0}NI}{2\pi r}$
### Ley de Faraday
Como resultado de cirtas observaciones, Faraday concluyó que es posible inducir una corriente eléctrica en una espira mediante un campo magnético cambiante. La corriente inducida existe sólo mientras el campo magnético que pasa a través de la espira cambia. En cuanto el campo magnético alcanza un valor estable, la corriente en la espira secundaria desaparece. En efecto, la espira se comporta como si se hubiera conectado una fuente de fem durante un lapso breve. Es habitual decir que una fem inducida se produce en la espira debido al campo magnético cambiante.
Por la tanto, la **ley de inducción de Faraday** por el cambio del flujo magnético a través de la espira en el tiempo se escribe como:
$$\mathcal{E}=- \frac{d\Phi_{B}}{dt}$$
Donde $\Phi_{B}=\oint \vec{B}.d\vec{A}$ es el flujo magnético a través de la espira. Y para una bobina con N epiras: $\mathcal{E}=- N\frac{d\Phi_{B}}{dt}$
### Fem de movimiento
Se describe la fem de movimiento como la fem inducida en un conductor en movimiento a través de un campo magnético cte.
**Obs.** Puedo deducir la siguiente expresión de la definición de la fem inducida:
$$I=\frac{|\mathcal{E}|}{R}$$
### Ley de Lenz
La corriente inducida en una espira está en la dirección que crea un campo magnético que se opone al cambio en el flujo magnético en el área encerrada por la espira.
### Fem inducida y campos eléctricos
Es posible relacionar una corriente inducida en una espira conductora con un campo eléctrico al afirmar que se produce un campo eléctrico en un conductor como resultado de un flujo magnético cambiante. También se observó que la existencia de un campo eléctrico es independiente de la presencia de cualquier carga de prueba. Lo anterior sugiere que incluso en ausencia de una espira conductora, un campo magnético cambiante genera un campo eléctrico en el vacío. Este campo eléctrico es no conservativo, a diferencia del campo electrostático producido por cargas fijas.
**Def.** La fem corrrespondiente a cualquier trayectoria cerrada puede expresarse como la integral de línea de $\vec{E}.d\vec{s}$ a lo largo de la trayectoria:
$$\mathcal{E}=\oint \vec{E}.d\vec{s}=- \frac{d\Phi_{B}}{dt}$$
**El campo eléctrico inducido es un campo no conservativo generado por un campo magnético cambiante**.
### Inductancia
La fem $\mathcal{E}_{L}$ establecida se llama **fem autoinducida**, y es proporcional a la rapidez de cambio en el tiempo de la corriente:
$$\mathcal{E}_{L}=-L \frac{dI}{dt}$$
Donde $L$ es una cte, llamada **inductancia** de la espira, que depende de la geometría de la espira y otras características físicas, y su expresión es tal que:
$$L=\frac{N\Phi_{B}}{I}$$
### Energía en un campo magnético
Si $U$ representa la energía almacenada en el inductor en cualquier instante, se puede escribir la relación de la variación de energía la almacenada en el tiempo:
$$\frac{dU}{dt}=LI \frac{dI}{dt}$$
Por lo que la expresión para la energía almacenada en el inductor en cualquier instante es:
$$U= \frac{1}{2}LI^{2}$$
Y la densidad de energía magnética, o la energía almacenada por cada unidad de volumen en el campo magnético de un inductor, es igual a:
$$u_{B}=\frac{U}{V}=\frac{B^{2}}{2\mu_{0}}$$
### Inductancia Mutua
Si considero dos bobinas de alambre enrolladas apretadamente. La inductancia mutua $M_{12}$ de la bobina 2 respecto de la bobina 1 es:
$$M_{12}=\frac{N_{2}\Phi_{12}}{I_{1}} \to \Phi_{12}=\frac{M_{12}I_{1}}{N_{2}}$$
Por lo que la fem inducida por la bobina 1 en la bobina 2 es igual a:
$$\mathcal{E}_{2}= -N_{2} \frac{d\Phi_{12}}{dt}= -N_{2} \frac{d}{dt}(\frac{M_{12}I_{1}}{N_{2}}) =-M_{12} \frac{dI_{1}}{dt}$$
Y la fem inducida en la bobina 1 es: $\mathcal{E}_{1}=-M_{21} \frac{dI_{2}}{dt}$
**Obs.** La inductancia mutua de 1 en 2 y de 2 en 1 son iguales, entonces:
$$M_{21}=M_{12}=M \longrightarrow \mathcal{E}_{2}=-M \frac{dI_{1}}{dt} \quad \mathcal{E}_{1}=-M \frac{dI_{2}}{dt}$$
