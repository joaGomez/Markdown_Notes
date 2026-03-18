### Amplificador operacional
- No inversor: $$\frac{V_{0}}{V_{i}}= (1+ \frac{R_{1}}{R_{2}})\cdot \frac{1}{1+\frac{1+ \frac{R_{1}}{R_{2}}}{A_{0}}}$$
![[Pasted image 20240822183536.png#center|150]]
	Siendo el primer factor $k_{ni}$, (ganancia ideal), y el segundo término el factor de error.
- Inversor: $$\frac{V_{0}}{V_{i}}= - \frac{R_{1}}{R_{2}}\cdot \frac{1}{1+\frac{1+ \frac{R_{1}}{R_{2}}}{A_{0}}}$$
![[Pasted image 20240822183825.png#center|200]]
Siendo el primer factor $k_{i}$, y en este caso puede ser atenuador.

En el modelo ideal, la impedancia de entrada es infinita, y la impedancia de salida $0$. Además, la ganancia del opamp es infinita también.
#### Modelo real
Ahora considero una impedancia de entrada finita $r_{i}$, y una impedancia de salida finita $r_{0}$.
![[Pasted image 20240822183920.png#center|150]]

La ganancia de tensión y de corriente suele estar limitada por un $V_{cc}$, y llega hasta una tensión de saturación, tal que se cumple lo siguiente:
![[Pasted image 20240822184047.png#center]]

![[Pasted image 20240822184105.png#center]]
### Buffer analógico
Funciona como un opamp con realimentación negativa pero sin una ganancia $\beta$, por lo que la tensión de salida es prácticamente la tensión de entrada, es decir, tiene una ganancia de uno. Esto nos sirve cuando queremos cierta tensión de entrada para una carga, como en el siguiente ejemplo:
![[Pasted image 20240822184123.png#center|200]]
### Masa virtual
Si la salida es finita, y la ganancia muy grande $\to$ $V^{+}\simeq V^{-}$.
### Sumador
![[Pasted image 20240822184519.png#center]]
### Integrador
![[Pasted image 20240822184650.png#center|200]]
$$V_{0}= V_{i}\cdot \frac{- \frac{1}{sC}}{R}= - V_{i}\cdot \frac{1}{sRC}$$
Y su diagrama de bloques es:
![[Pasted image 20240822184832.png#center|200]]

De modo que la salida la puedo escribir como $V_{0}(t) = - \frac{1}{RC} \cdot \int_{0}^{t}V_{i}~ dt$
### Derivador
![[Pasted image 20240822185036.png#center|200]]
$$V_{0}=V_{i}\cdot \left(- \frac{R}{\frac{1}{sC}}\right)=-V_{i}\cdot sRC \to V_{0}= -RC \frac{dV_{i}}{dt}$$
**Obs:** Un problema con este modelo es que amplifica mucho las señales de alta frecuencia. Por lo tanto, es mejor limitar la ganancia agregando una resistencia de compensación.

![[Pasted image 20240822185356.png#center|200]]

**Obs:** En el integrador también deberíamos agregar una resistencia de compensación en paralelo con el capacitor por las señales de continua.
### Respuesta en frecuencia
Cuando la curva corta el eje de la frecuencia, es decir, $|H(j\omega_{CR})|[dB]=0 \to |H(j\omega_{CR})|=1$. Por lo tanto, el valor $\omega_{CR} > \omega_{1}$, que es el valor del polo. Si conocemos el polo podemos aproximar el valor de $\omega_{CR}$ como:
$$\omega_{CR}\simeq|K|\cdot \omega_{1}=GBWP$$
> Demo: 
> ![[Pasted image 20240822190351.png|300]]

En la fabricación de amplificadores operacionales se debe tener especial cuidado con la inversión de fase, ya que podemos pasar de tener realimentación negativa, a tener realimentación positiva si el desfasaje es de $180$°. Por lo tanto, los fabricantes suelen poner un polo dominante a frecuencias bajas para evitar esta problemática:
$$A_{v}(s)= \frac{A_{0}}{1+ \frac{s}{\omega_{1}}}$$
Esto se puede visualizar de la siguiente forma:
![[Pasted image 20240822190944.png#center|200]]

Teniendo en cuenta esta variación de la ganancia del operacional, la ecuación para ambos casos con los que se trabajo quedarían:
$$\begin{split}
&\frac{V_{0}}{V_{i}} = K_{ni}\cdot \frac{1}{1+ \frac{K_{ni}}{A_{0}}} \cdot \frac{1}{1+ \frac{s}{\frac{\omega_{1}A_{0}}{K_{ni}}}} \qquad &\text{No inversor} \\
&\frac{V_{0}}{V_{i}} = K_{i}\cdot \frac{1}{1+ \frac{K_{ni}}{A_{0}}} \cdot \frac{1}{1+ \frac{s}{\frac{\omega_{1}A_{0}}{K_{ni}}}} \qquad &\text{Inversor}
\end{split}$$
Como se ve en las expresiones, el único factor que cambia es la ganancia. Donde se cumple que si tenemos misma configuración para ambos:
$$K_{ni}=1 + \frac{R_{1}}{R_{2}} \quad K_{i}=\frac{-R_{1}}{R_{2}}$$
Por lo tanto, esto nos deja que si $f_{corte_{ni}}=f_{corte_{i}} \to K_{ni}> K_{i}$. Se puede modificar el valor de los componentes de modo que ambos operacionales tengan la misma ganancia, pero esto generará que ya no tengan la misma frecuencia de corte, sino que la del no inversor será mayor.

![[Pasted image 20240822193259.png#center|200]]
### Slew rate
El slew rate es la máxima tasa de variación de tensión a la salida que el operacional puede dar.

![[Pasted image 20240822194458.png#center]]

En un buffer, la salida intenta igualar a la entrada, pero si ésta tiene una variación mayor a la posible por el slew rate, entonces la salida tendrá una pendiente máxima hasta que compense e iguale a la entrada.

![[Pasted image 20240822194654.png#center|300]]
### Buffer con realimentación positiva
![[Pasted image 20240822194739.png#center|200]]
La ganancia del buffer será:
$$\frac{V_{0}}{V_{i}}= \frac{1}{1- \frac{1}{A_{0}}}$$
Pero si tengo en cuenta el polo dominante del operacional queda:
$$\frac{V_{0}}{V_{i}}= \frac{1}{1- \frac{s}{\omega_{1}(A_{0}-1)}}$$
Por lo que ahora se tiene un polo en el semieje positivo y el sistema es inestable.
**Obs:** Si el polo cumple $|\omega_{c}|=|\omega_{1}(A_{0}-1)|<1$, el sistema es estable.
### Fuentes controladas con opamps
Mediante un operacional inversor se puede armar una fuente de corriente controlada por tensión:
![[Pasted image 20240822195807.png#center]]

Donde la salida estará dada por $V_{0}= R_{L}\cdot |i_{L}|<V_{sat}$

**Obs:** El problema con este modelo es que buscamos que la carga esté conectada a masa y en este caso no es así.

El siguiente caso cumple con esto:
![[Pasted image 20240822200007.png#center|600]]
### Modelo real: Cálculo de $i_{bias}$ y $V_{io}$
![[Pasted image 20240822200140.png#center]]

Para buscar que configuración de componentes logra poner el offset en 0, puedo sumar $V_{0}(i_{bias})=V_{0}(i_{bias}^{+})+V_{0}(i_{bias}^{-})=0$.
### Ecualizador de fase
Éste es un filtro que no modifica la amplitud (ganancia unitaria), pero cambia la fase. Es un circuito con un diagrama de polos y ceros que se vea tal que:
![[Pasted image 20240823000040.png#center|100]]
En principio esto no debería de poder modelarse en la realidad, pero mediante despejes matemáticos podemos llegar a un resultado tangible:
$$H(s)= \frac{\frac{s}{-\omega C}+1}{\frac{s}{\omega C}+1}=\frac{-\frac{s}{\omega C}-1+2}{\frac{s}{\omega C}+1}=2\cdot \frac{1}{\frac{s}{\omega C}+1}-1 \to V_{0}=2V_{i}\cdot \frac{1}{\frac{s}{\omega C}+1}-V_{i}$$
Este resultado si se puede modelar mediante un circuito:
![[Pasted image 20240823000556.png#center|300]]
La fase de esta transferencia será:
$$Arg(H(s))=-2\cdot arctg\left(\frac{\omega}{\omega_{c}}\right)$$
**Obs:** Se debe tener en cuenta que al ser un polo y un cero, solo se logra un desfasaje de $180$°. Por lo tanto $Arg(H(s))\in[-180°,0°]$.

Si tomamos una segunda función de transferencia tal que: 
$$H_{2}(s)=-H(s)=2\cdot \frac{\frac{s}{\omega C}}{\frac{s}{\omega C}+1}-1$$
Para esta función de transferencia se encuentra asociada el siguiente circuito:
![[Pasted image 20240823001109.png#center|300]]
La fase en este caso será:
$$Arg(H_{2}(s))= 180°-2\cdot arctg\left(\frac{\omega}{\omega_{c}}\right)$$
Donde $Arg(H_{2}(s))\in[0°, 180°]$.
### Single supply
En vez de alimentar el operacional con una fuente compartida que provee $+V_{cc}$ y $-V_{cc}$, se utiliza una batería. El problema con esta ocurre al no tener una referencia común, como si tenía la fuente compartida.

Debido a esto, se utiliza el siguiente tipo de circuito:
![[Pasted image 20240823001830.png#center|400]]
Donde se provee al operacional con $+V_{cc}$ y al terminal negativo se lo conecta a tierra.

Al hacer esto ocurre otro problema, si utilizamos una señal con polaridad negativa, esta se perderá, no habrá salida. Para esto, Se utiliza un primer capacitor $C_{i}$, el cual si hacemos un análisis en DC, se ve como aporta una salida $V_{0}^{'}$.
![[Pasted image 20240823002143.png#center|250]]
Esto generá un offset en la salida, por lo cual si ahora analizamos en AC la señal oscilará a partir de $\frac{V_{cc}}{2}$.
![[Pasted image 20240823002304.png#center|250]]
Mediante este método, logramos exclusión completa, es decir, no se perdieron los valores del semieje negativo y se logró obtener a la salida una señal completa representada por la entrada en su totalidad.

Luego, hay un $C_{0}$ antes del que llamamos la verdadera salida $V_{0}$. Esto se debe a que el trabajo de este capacitor es no dejar pasar la señal continua, por lo que el offset producido se va y la salida es la esperada como si la terminal negativa no estuviese conectada a tierra.
![[Pasted image 20240823002633.png#center]]

**Obs:** Debido a colocar estos capacitores, tendremos dos frecuencias de corte que limiten el operacional.
![[Pasted image 20240823003257.png#center|300]]
### Feedback
Se denomina feedback al concepto e implementación de realimentación. Un sistema realimentado lo podemos caracterizar como:
![[Pasted image 20240823003547.png#center|250]]
Donde la expresión que representa la salida se define como:
$$X_{0}=a\cdot X_{d}=a\cdot (X_{i}-X_{f})=a\cdot(X_{i}-\beta\cdot X_{0}) \to \frac{X_{0}}{X_{i}}= \frac{a}{1+\beta\cdot a}$$
Se denomina **Loop gain** a $T=\beta\cdot a$.
- Si $T>0:$ Realimentación negativa → Feedback degenerativa.
- Si $T<0:$ Realimentación positiva → Feedback regenerativa. El sistema es inestable y diverge.

Se define la ganancia de lazo cerrado (sistema realimentado) como:
$$A_{CL}= \frac{X_{0}}{X_{i}}= \frac{a}{1+T}$$
E idealmente:
$$A_{CLi}=\lim_{T\to \infty}A_{CL}=\frac{a}{T}=\frac{1}{\beta}$$
Por lo que se puede ver que gracias al feedback (realimentación), el sistema no depende de $a$, sólo depende de $a\cdot\beta$ sea muy grande.
### Tracking
Si $T\to \infty \Rightarrow X_{d}\to 0 \Rightarrow X_{i}\simeq X_{f}$ (**Condición de trancking**).
### Ventajas de la realimentación
- Mejora la impedancia de entrada, haciendola muy grande, casi ideal: $Z_{i}= \frac{V_{d}}{i_{d}}\cdot (1+\beta\cdot a)=r_{d}\cdot (1+\beta\cdot a)$
- Mejora la impedancia de salida, tal que: $Z_{0}= \frac{r_{0}}{1+\beta\cdot a}$
- Aumenta el ancho de banda: $BW_{f}=BW_{0}\cdot(1+\beta\cdot a)$
- Si $a$ no es completamente lineal no importa, ya que el feedback me soluciona estos problemas.

**Obs:**
![[Pasted image 20240823005238.png#center|510]]
### Diseño de circuitos
Se pueden realizar diseños de circuitos que parecen imposibles. Para esto, se debe proceder cuidadosamente con los cálculos, de forma de pasar de algo imposible, a algo que conocemos.

Los polos o ceros en el semieje positivo son imposibles de lograr, generan que el sistema no sea estable.

![[Pasted image 20240903232141.png#center|200]]
Si quiero un circuito que realice esto, puedo comenzar escribiendo la tansferencia que manifiesta este comportamiento imposible. Luego, manipulo matemáticamente para hacerlo posible.

$$
H(s) = \frac{(\frac{s}{\omega_{0}})^{2} - \frac{s}{\omega_{0}Q} + 1}{(\frac{s}{\omega_{0}})^{2} + \frac{s}{\omega_{0}Q} + 1} =
\frac{(\frac{s}{\omega_{0}})^{2} + \frac{s}{\omega_{0}Q} + 1 - 2\cdot \frac{s}{\omega_{0}Q}}{(\frac{s}{\omega_{0}})^{2} + \frac{s}{\omega_{0}Q} + 1} =
1-2\cdot \frac{\frac{s}{\omega_{0}Q}}{(\frac{s}{\omega_{0}})^{2} + \frac{s}{\omega_{0}Q} + 1}
$$
Esta transferencia si se puede realizar. El segundo término corresponde a un pasabanda.
$$\frac{H(s)}{2}= \frac{1}{2}-BP(s) \to V_{0}= \frac{V_{i}}{2}-V_{i}\cdot BP(s)$$
La implementación sería:
![[Pasted image 20240903232926.png#center|500]]
### Síntesis circuital
Mediante distintos circuitos, se pueden lograr ciertas impedancias.

Con el circuito FDNR se ve una impedancia negativa, tal que:

![[Pasted image 20240903233706.png#center|500]]

El GIC es un convertidor de impedancia muy conocido, su esquema es:

![[Pasted image 20240903233853.png#center]]

Luego, Antoniou presentó su propio GIC.

![[Pasted image 20240903233942.png#center]]

El problema con este modelo, es que, de ser necesario, la corriente que sale es distinta a la que entra. Por lo que si esperábamos reemplazar este circuito por un impedancia como tal y ya está, hay un problema.

Este problema se resuelve contrarrestando el efecto del factor que modifica la corriente:

![[Pasted image 20240903234215.png#center]]

#### Fuente de corriente mejorada

![[Pasted image 20240903234316.png#center]]
### Margen de fase y de ganancia
Para el diseño de un circuito es importante tener en cuenta estos margenes. Estos margenes delimitan cuan cerca estamos de la inestabildad.

Se podrían definir como el rango de desplazamiento seguro antes de tener problemas de estabildiad.
### Conexión de cuadripolos
![[Pasted image 20240903230614.png#center]]

Teniendo en cuenta el diagrama de bloques para un sistema con realimentación negativa, donde se cumple que:
$$
\begin{split}
&X_{d}= X_{i}-X_{f} \\
&X_{f} = \beta \cdot X_{0} \\
& X_{0}=A\cdot X_{d} \rightarrow \frac{X_{0}}{X_{i}} = \frac{A}{1+\beta\cdot A} \approx \frac{1}{\beta} \quad \text{(si A es muy grande)}
\end{split}
$$
Ahora, estas expresiones las puedo pensar para circuitos, y utilizar los digramas para modelar los distinros actores del mismo, y de esta forma, llegar a la expresión del circuito. Por esto, también es importante identificar como se debe proceder para el circuito. Por ejemplo, para un operacional no inversor, se hace lo siguiente:

![[Pasted image 20240903231810.png#center]]
#### Gyrator
El gyrator es un modelo circuital, que se ve:

![[Pasted image 20240903234413.png#center|300]]

Para hacerlo en la realidad hay distintas formas. Lo ideal, es encontrar la forrma de utilizar la menor cantidad de componentes, o recursos.

Una implementación del gyrator con 4 operacionales:

![[Pasted image 20240903234603.png#center]]

Esto se puede mejorar, y se puede lograr sólo usando dos operacionales:

![[Pasted image 20240903234710.png#center]]
### Amplificadores diferenciales
![[Pasted image 20240913082734.png#center]]
Para un circuito que cuente con señal de modo diferencial, y de modo común, la salida será:
$$V_{0}= V_{0DM}+V_{0CM}=A_{DM}\cdot V_{DM}+A_{CM}\cdot V_{CM}$$
Donde se dice que el circuito está balanceado si: $A_{CM}=0$.
$$\begin{cases}
\frac{V_{0}}{V_{DM}}\bigg|_{V_{CM}=0}=A_{DM} \\ \\
\frac{V_{0}}{V_{CM}}\bigg|_{V_{DM}=0}=A_{CM}
\end{cases}$$
$$CMRR= \frac{A_{DM}}{A_{CM}}[dB] \qquad \text{Relación de rechazo de modo común}$$
### Sensibilidad
$$S_{R}^{H}= \frac{\partial H}{\partial R}\cdot \frac{R}{H}$$

