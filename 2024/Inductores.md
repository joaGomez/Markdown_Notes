$B:$ Densidad de campo magnético
$H:$ Intensidad de campo magnético
$J:$ Densidad de corriente
$E:$ Tensión

$$\begin{split}
Gauss: \oint_{s}B\ ds = 0 \\
Faraday-Lenz: \oint_{l}E\ dl = \frac{-d}{dt}\int_{s}B\ ds\\
Ampere: \oint_{s}H\ dl = \int_{s}J\ ds
\end{split}$$
#### Ciclo de histéresis
![[Pasted image 20240305111555.png|600]]
$$\mu_{efec}=\mu_{0}\ . \mu_{relativo}$$
Si tengo el $\mu$ de un elemento, en realidad tenemos el $\mu_{relativo}$ o $\mu_{inicial}$.

**Obs:** Ponerle campo magnético a un componente/elemento, es rodearlo con un cable y al cable le pongo que corriente, que si esta se modifica en el tiempo → el campo que le doy también se modifica.

Si a un calvo lo rodeo con un alambre y lo conecto a una pila, le estoy dando corriente. Al desconectarlo, la corriente baja a 0 pero como hay pérdidas de campo magnético, el clavo queda con un campo remanente. Si la corriente sigue bajando me va a quedar un $H_{c}$ (coercitivo). Si subo la corriente vuelve al campo remanente pero 'invertido' (en cuanto a su polaridad). Por último, si sigo subiendo llego hasta un $H_{c}$ nuevamente.

![[Pasted image 20240305115658.png#center|400]]
Faraday: $\oint E\ dl = \frac{-d}{dt}\int_{s}B\ ds$, $v_{(t)}= \frac{-d}{dt}(N*B*A)=N A \frac{dB}{dt}$ 
Ampere: $\oint_{l}H\ dl = \int_{s}J\ ds$, $H\oint_{l}dl = N*i$, $H*l=N*i$, $H= \frac{N*i}{l}$, siendo $l$ la longitud media del circuito magnético.

![[Pasted image 20240305123428.png#center|600]]

Un cable lo debemos visualizar siempre con una resistencia y un inductor. Esto se debe que por el material siempre va a contar con una resistividad. Además, el cable genera un campo magnético (aunque muy pequeño), y como el campo que genera es un diferencial de campo, y si la corriente depende del tiempo → va a generar una fem inducida. Esa fem se va a oponer a que la corriente pase (como una inductancia) y por eso la fem es negativa.

![[Pasted image 20240308102908.png#center|200]]
La inductancia de un cable promedio es $L_{cable} \approx 5 \frac{nH}{cm}$. El cable esta lleno de N espiras que rodean el cable y son esa misma cantidad de espiras las que 'sienten' el flujo magnético del cable.

La resistencia de un cable depende del material, y se puede ver con la siguiente fórmula:
$$R= \rho \frac{l}{s}$$

**Obs:** La energía se guarda en la deformación de los cristales del núcleo.
#### Transformadores
Al conectar un segundo cable, hay menos flujo, menos dipolos deformados. Y como la fem disminuye, la corriente sube. Al subir la corriente aumenta el campo magnético del primario, esto, aumentará hasta que el campo magnético del primario y el secundario sean iguales → Alcanza el equilibrio → Puede seguir funcionando todo lo que quiera.

![[Pasted image 20240308111026.png#center|500]]

La densidad de flujo magnético $B$ que circula por el núcleo es siempre la misma y se denomina $B$ **de magnetización**. Este $B_{mag}$ es el que asegura que el sistema siga en equilibrio.

###### Trafo ideal
$$\begin{cases}
V_{1}=N_{1}A \frac{dB}{dt} \\
V_{2}=N_{2}A \frac{dB}{dt} \\
\end{cases}
\quad \to \quad \frac{V_{1}}{V_{2}}=\frac{N_{1}}{N_{2}}, \quad i_{1}N_{1}=i_{2}N_{2}$$
![[Pasted image 20240308112606.png#center|450]]

Cuando no es ideal, planteamos una parte ideal, y le sumamos un inductor por el $B_{mag}$ que nos aparece, y le sumamos una resistencia por las pérdidas de energía en el núcleo. También añadimos, tanto al primario como al secundario una resistencia y un inductor por las propiedades físicas del cable.

![[Pasted image 20240308112632.png#center|500]]


![[Pasted image 20240312115430.png#center|500]]
Cálculo aproximado de la inductancia, sin tener en cuenta la dispersión del flujo, o la tensión del bobinado, etc.

![[Pasted image 20240312120606.png#center|400]]
Cálculo de la reluctancia total. Al añadirle un gap al transformador, si tengo un $\mu_{r}$ muy grande, sin importar que varía un poco, al agregarle el término del gap, esa variación se ve reducida.

> **Obs:**
> ![[Pasted image 20240312121433.png#center|400]]
> Aquí vemos como se ve el ciclo de histéresis corrido por el gap añadido.

|                                                                            Teoría                                                                             |                                                                                                                        Realidad                                                                                                                        |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                       Todo el flujo magnético se concentra en el núcleo                                                       |                                                                                            Hay flujo disperso alrededor de los cables, entrehierro y núcleo                                                                                            |
|                    Toda la tensión de entrada se reparte en las N espiras por igual. Todo el flujo magnético está encerrado en el núcleo.                     |                                                                Hay pérdidas de tensión por ley de Ohm en los cables ($R*i$). Hay FEM inducidas en el núcleo. Efectos Skin y proximidad.                                                                |
| Toda la corriente se concentra en el bobinado. Todo el H se reparte uniformemente por el núcleo. Todas las líneas de flujo magnético recorren el mismo camino | Hay corrientes parásitas en el núcleo por efecto Foucault (Eddy Currents). El núcleo no es uniforme (en forma y composición). Existen infinitos caminos distintos para que se cierren las líneas de campo, pero sólo  se toma la “promedio” $l_{mag}$. |


La tensión produce la corriente. La corriente genera una fuerza magnética (H), esta fuerza se distribuye en todo el largo del material, y consume energía que es almacenada en los dipolos (B). Los cristales se pueden deformar una cantidad finita, mediante la aplicación de H, cuando alcanza esta cantidad se satura → $\mu=\mu_{0}$
#### Núcleos de hierro
$$I=\frac{BRA}{N} \qquad P=i{^{2}}r$$

Buscamos el $B_{max}$ antes de que sature en el ciclo de histéresis:
$$B_{max}=\frac{1}{2} \frac{\int_{t1}^{t2} v(t)dt}{NA}+\frac{NI_{DC}}{RA}<B_{sat}$$

![[Pasted image 20240320090957.png#center|600]]

Para fijar los límites de integración de $v(t)$ y calcular $dB$ hay que analizar la correlación entre el ciclo de histéresis y la tensión en el tiempo.
1. El circuito tiene una tensión en alterna y NO tiene corriente en continua: $\Delta B = \frac{\int_{t1}^{t2} v(t)dt}{NA} = 2B_{max}<2B_{sat}$

![[Pasted image 20240320091621.png#center|350]]
2. El circuito permite una CC superpuesta: $B_{max}= \frac{1}{2} \frac{\int_{t1}^{t2} v(t)dt}{NA} + \frac{NI_{DC}}{RA} <B_{sat}$

![[Pasted image 20240320092021.png#center|200]]
##### Producto Volt-Segundo
Para un circuito trabajando a muchos KHz, el régmen permanente puede ser un tiempo muy chico, por lo que para que el núcleo no sature, la integral de la tensión debe ser acotada (Todo lo que 'sube' de tensión debe 'bajar') → $\bar{V_{l}}=0 \wedge \bar{I_{c}}=0$.

**Obs:** El área de la curva $v(t)$ se la denomina **producto volt-segundo**.
![[Pasted image 20240320092822.png#center|150]]
En un circuito trabajando en régimen permanente → El producto volt-segundo debe ser nulo

##### Ecuación fundamental de diseño
![[Pasted image 20240320093343.png#center|500]]

##### Tipos de bobinas
Según la forma de la corriente que circula, se tratan por separado tres tipos de bobinas:
1. Inductores: $B_{max}=\frac{1}{2} \frac{\int_{t1}^{t2} v(t)dt}{NA} < B_{sat}$ 
![[Pasted image 20240320093946.png#center|200]]
2. Choques: $B_{max}= \frac{NI_{DC}}{RA} <B_{sat}$
![[Pasted image 20240320094221.png#center|200]]
3. Inductores de potencia: $B_{max}= \frac{1}{2} \frac{\int_{t1}^{t2} v(t)dt}{NA} + \frac{NI_{DC}}{RA} <B_{sat}$
![[Pasted image 20240320094319.png#center|200]]
#### Efecto skin
Es un efecto de “centrifugado” de los electrones del cable debido a su propio campo magnético variable (fem). El efecto es mayor cuanto mayor es la frecuencia. Debido a esta fem, aparece una fuerza en el centro del cable que frena a los electrones, por lo que estos comienzan a circular por las paredes del cable.
![[Pasted image 20240320094816.png#center|300]]
Esta región donde circulan se llama **skin depth**.
![[Pasted image 20240320094731.png#center|80]]
Ecuación de skin depth: $SD= \frac{66}{\sqrt{F}}mm$

**Obs:** Como consecuencia de este efecto, al reducirse la sección → Aumenta la resistencia del cable, ya que la resistencia depende de la sección ($R= \rho \frac{l}{S}$).
##### ¿Cómo minimizar el efecto skin?
1. Se utilizan varios cables aislados entre sí, de poca sección en paralelo. De manera de que en cada uno el efecto skin sea mínimo.
![[Pasted image 20240320095622.png#center|250]]
2. Cable Litz: es un trenzado especial de muchos cables muy finos, aislados entre si. El doble trenzado minimiza además el efecto proximidad. También se trenzan en forma de cintas.
3. Flejes: se utilizan en transformadores de mucha corriente o de muy alta frecuencia. El espesor debe ser menor a 2SD para garantizar que todo el cobre conduzca corriente. Se pueden cortar a medida con los pliegues necesarios para la acometida y salida del carrete.
#### Efecto proximidad
Es el efecto de la interacción entre dos cables por donde circula corriente variable. Como resultado ambos conductores se afectan mutuamente y la corriente circula mayormente por un lado del conductor y no por el otro.
![[Pasted image 20240320100201.png#center|300]]
Como los electrones son los que 'circulan' corriente → Cuando las corrientes van en dirección opuesta, los $e{^{-}}$ se atraen. En cambio, cuando las corrientas van en la misma dirección → Los $e{^{-}}$ se repelen.

Para minimizar el efecto proximidad se trata de evitar tener gran magnitud de campo magnético, para ello se apilan los bobinados en forma intercalada.
![[Pasted image 20240320100503.png#center|350]]

$k_{w}:$ Factor de ventana: Es la relación entre el área total para bobinar y el área efectiva de cobre. Depende del tipo de bobinado a realizar, la calidad (orden) del bobinado, los aislantes, tipo de cable, etc.
$$k_{w}= \frac{Área\ efectiva\ de\ cobre}{A_{w}}$$
![[Pasted image 20240320101820.png#center|300]]

Razones por las que debemos considerar $K_{w}$ a la hora de hacer un transformador:
- Aire
- Aislantes (entre cables, entre capas, entre bobinados)
- Espesor carrete
- Tolerancias
- Clearence

Áreas designadas para cada núcleo:
$$Área_{1}= \frac{A_{N}}{2}\to Sección~Cu_{1}= \frac{\frac{A_{N}}{2}.K_{w}}{N_{1}}$$
$$Área_{2}= \frac{A_{N}}{2}\to Sección~Cu_{2}= \frac{\frac{A_{N}}{2}.K_{w}}{N_{2}}$$
Este resultado me da la cantidad de cobre que necesito en $mm{^{2}}$. Si tengo efeco skin → Le debo restar la sección acorde al efecto skin.

Se define la resistencia de un cable para el transformador como $r_{Cu}\simeq A_{R}\cdot N{^{2}}$.

**Obs:** El área que le doy al primario va a ser mayor al área que le doy al secundario, ya que por el cable del primario circulan 3 corrientes, mientras que en el del secundario sólo 1.

![[Pasted image 20240322114158.png#center|200]]
Del modelo simplificado del transformador se puede observar que el cable del primario tiene que conducir la suma de tres corrientes: 
- La corriente que va a ir a la carga ($i_{1}=i_{2} \frac{N_{2}}{N_{1}}$) 
- La corriente de magnetización 
- La corriente de pérdidas en el núcleo (histéresis y Foucault)


**Obs:** $Duty= \frac{Ton}{T}$, siendo $T$ el período de la señal y $Ton$ el momento/tiempo de la señal 'activa'.

##### Ejercicio de clase

![[Pasted image 20240416112603.png#center|600]]
![[Pasted image 20240416114628.png#center|600]]
![[Pasted image 20240416122607.png#center|600]]
El área mínima se toma en donde se congestiona el flujo primero, y como $9 < 19$ → El $A_{min}=9\times 30$.

En el $N_{1~min}$ redondeo para arriba para que no se sature. Para el $N_{2}$ tambén redondeo para arrba para compensar las pérdidas