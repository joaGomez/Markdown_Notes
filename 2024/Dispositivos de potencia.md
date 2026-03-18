#### Diodo de potencia
![[Pasted image 20240530184255.png#center|400]]
![[Pasted image 20240530184357.png#center|400]]
- En niveles bajos de inyección → $\delta p << n_{n0}$, los electrones de equilibrio térmico ($n_{n0}$) neutralizan sin dificultad la carga de espacio de los huecos.
- En niveles altos de inyección → $\delta p > n_{n0}$, la carga de espacio de huecos atrae electrones de la región $n^{+}$ a la región de arrastre.
- Esto lleva a la inyección d electrones a través de la interconexión $n^{+}n^{-}$ a la región de arrastre con densidades $\delta n = \delta p$. (**inyección doble**).
#### Recombinación en dispositivos de potencia
- Velocidad de generación-recombinación térmica:
$$\frac{d(\delta n)}{dt}=-\frac{\delta n}{\tau}$$
Donde $\delta n$ es la densidad del portador libre excedente, y $\tau$ es el tiempo de vida del portador excedente o minoritario.

**Obs:** El $\tau$ no es cte para dispositivos de portadores minoritarios de potencia TBJ, tiristor, GTO. Además, este tiempo aumenta con la temperatura.

Para altas densidades, cercanas a ($n_{b}$) $10^{16}~cm^{-3}$, este tiempo disminuye (por Auger), e incrementa las pérdidas en estado activo de los dispositivos.
$$\tau = \frac{\tau_{0}}{1+\frac{(\delta n)^{2}}{n_{b}^{2}}}$$
Valores mayores de $\tau$ reducen las pérdidas de los dispositivos en estado activo, pero también tienden a desacelerar la transición de conmutación de encendido a apagado y viceversa.
#### Tiristor
###### Circuito equivalente
![[Pasted image 20240530185826.png#center|250]]
Y se comportará tal que:
![[Pasted image 20240530185915.png#center|400]]
#### Triac
El triac funciona igual que el tiristor pero en ambos sentidos, como si tuviera dos tiristores en paralelo. Aunque no es tan asi porque debería tener dos gates y solo tengo uno. Además, el triac se utiliza para baja potencia, a diferencia de los tiristores que se usan para media/alta potencia.
![[Pasted image 20240530190722.png#center|400]]
**Obs:** Un pico de tensión ($\frac{dV}{dt}$) puede encenderlo erráticamente. Esto se puede evitar con una impedancia en serie. Un pico de corriente ($\frac{dI}{dt}$) me lo quema, por lo que debería poner una bobina que me reduzca esta variación de corriente. También se puede usar un fusible.
#### Circuitos de aplicación de control de fase
![[Pasted image 20240530191610.png#center|400]]
##### Transición del estado de equilibrio al estado de bloqueo directo del tiristor
![[Pasted image 20240530194829.png#center|200]]
![[Pasted image 20240530194851.png#center|250]]
##### Encendido del tiristor
![[Pasted image 20240530194954.png#center|600]]
##### Apagado y bloqueo inverso del tiristor
Del estado de conducción directa al apagado.
![[Pasted image 20240530195103.png#center|300]]
- En estado de conducción se inyectaron en las regiones $n$ y $p$ concentraciones de portadores que exceden mucho los valores de equilibrio.
- Se reduce la $I_{ak}$ hasta que los portadores se recombinan o salen de zona de deserción, y la tensión inversa $V_{ak}$ aumenta.
##### Estados de bloqueo
- Bloqueo inverso: El ánodo es negativo respecto al cátodo. Junturas J1 y J3 están en inversa. J2 está en directa. J1 tiene que soporta la tensión inversa (limitado por el ancho de zona n1). J3 tiene una Vruptura baja debido al alto dopaje en ambos lados de la unión.
- Bloqueo directo: Junturas J1 y J3 están en directa. J2 está en inversa. Debido a las densidades de dopaje, en la zona n1 aparece la zona de deplexión de la polarización inversa de J2. Nuevamente la zona n1 determina la tensión de bloqueo $V_{B0}$.
![[Pasted image 20240530195441.png#center|450]]
##### Proceso de encendido
- La zona de resistencia negativa es inestable debido a la realimentación (+).
- En el encendido aumentan los α1 y α2 debido al aumento de la Zona de deplexión de J2 hasta la capa $n_{1}$ al subir $V_{AK}$.
- Así se reduce el espesor de la base del p1n1p2 →  sube $\alpha_{pnp}$. La extensión de la deplexión de J2 en la capa p2 →  sube $\alpha_{npn}$.
- La combinación de la realim + y del aumento de los alfas posibilitan que el gate encienda al tiristor.
- Si se aplica una IG entrante, se inyectan e- mediante la polariz directa de J3 a la base p2. Luego los $e^{-}$ se difunden por la base y se barren a la capa n1.
- Estos e- en n1 producen 2 efectos:
	- Aumenta el espesor de zona de deplexión de J2.
	- Se produce la interacción de huecos (x requerimiento de neutralidad espacial) desde la unión J1.
- En estado activo: Se produce una inyección fuerte de portadores minoritarios en las cuatro zonas de la estructura. La unión J2 es de polarización directa, y los BJT en el circuito equivalente están saturados. $$V_{AK(enc)}=V_{j1}-V_{j2}+V_{j3}+V_{n^{-}}$$ Debo tener cuidado y limitar la corriente mediante un circuito externo.
##### Proceso de apagado
- La acción simultanea de recombinación interna y barrido de portadores retira la carga almacenada suficiente para sacar a los BJT de la saturación y dirigirlos a la zona activa.
- Una corriente de compuerta negativa no apaga el dispositivo (área de la zona del cátodo es mucho mas grande que el área de la compuerta.) 
- Se invierte la polarización del G-K, se produce una concentración de corriente en el centro y el tiristor  permanece encendido.
##### Transitorio de encendido
![[Pasted image 20240530200858.png#center]]
Donde $td_{enc}$ es el tiempo de retraso de encendido. $tr$ es el tiempo de subida. $tps$ es el tiempo de extensión de plasma.
##### GTO
Modifica estructura para lograr la capacidad de desconexión. Diferencias con el tiristor:
1. Estructura  compuerta cátodo muy interdigitada.
2. Cátodos formados con el grabado de Si que rodea los cátodos en forma de islas.
3. En el ánodo las zonas $n^{+}$ penetran el ánodo tipo p.

En sentido inverso, el GTO no tiene prácticamente ninguna capacidad de bloqueo debido a la estructura de cortocircuito del ánodo. La única que bloquea en sentido inverso es la J3 de tensión muy baja (20 ó 30v) debido a las altas densidades de dopaje a ambos lados de la unión.

![[Pasted image 20240530201250.png#center|600]]
- Debido a la estructura de cortocircuito del ánodo, no puede haber tensiones inversas de ánodo-cátodo y por tanto no hay corrientes de modo inverso para retirar los portadores excedentes mediante un barrido de portadores.
- La única manera de sacar los portadores excedentes son la recombinación interna y la difusión a través de las zonas $n^{+}$.
- Las zonas $n^+$ en la estructura del ánodo del GTO retira la barrera a la difusión de huecos y proporciona un disipador para huecos excedentes.
- Se logra que la carga almacenada se retire mucho mas rápido durante la desconexión del dispositivo, y  el GTO permite un apagado con tiempos de recuperación directa mas cortos en comparación con tiristores convencionales, sin comprometer gravemente sus perdidas en estado activo.
- La estructura recortada del ánodo es eficaz para reducir los tiempos de desconexión y recuperación.
- La capacidad de desconexión de compuerta es una estructura de compuerta y cátodo muy interdigitada que minimiza las caídas de tensión laterales en la capa p2 durante el encendido y el apagado.
#### MOSFET de potencia
![[Pasted image 20240530201515.png#center|300]]
- Región de estrangulamiento: Cuando la $V_{GS}< V_{GS}(th)$.
- Región ohmica: $V_{GS}-V_{GS}(th)> V_{DS}>0$.
- La región de arrastre de drenaje determina la tensión de ruptura.
![[Pasted image 20240530201722.png#center|350]]
#### IGBT
![[Pasted image 20240530202453.png#center]]
Circuito equivalente:
![[Pasted image 20240530202556.png#center|300]]
- Latchup: Se produce por el encendido del transistor npn que genera el enclavamiento del tiristor por la inyección de electrones desde la fuente al cuerpo (p). El fabricante  define una IDN max para evitar esta condición. (Latchup estático).
- Latchup dinámico: cuando conmuta de encendido a apagado, la corriente máxima es menor que la IDN max.
- La R de la región de arrastre depende del valor de Vg.
- El transistor NPN permite anular las corrientes parásitas que se generen al conmutar los otros transistores.
- Es un transistor de compuerta aislada, y por tanto $I_{drenaje} = I_{fuente}$.

 **Obs:** Con el aumento de la temperatura, la concentración de minoritarios en una juntura aumenta, ya que aumenta $n_{i}$.

Si quiero dos uniones que soporten la misma tensión máxima:
$$R_{N~sic}= \frac{R_{N~si}}{92.94}$$
Por otro lado, si construimos dos uniones (una de Silicio, y otra de SIC) que tengan la misma resistencia, veríamos que el SIC soporta 9,6 veces mas tensión que el Silicio.
##### Transistor de efecto de campo JFET de SiC
###### Ventajas
- Dispositivo de conducción unipolar.
- No es bipolar → Sin degeneración bipolar.
- Es rápido.
- Se fabrica partiendo de obleas N.
- Estructura simple.
###### Desventajas
- Dispositivo normalmente cerrado.
- Se controla con tensión negativa.

**Obs:** Los mosfet de SiC tienen baja movilidad de los electrones en el canal, debido a las cargas eléctricas que se acumulan en el óxido (problema). El material del óxido es clave. Es difícil conseguir el óxido del SiC.

