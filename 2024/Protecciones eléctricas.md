Choque eléctrico (shock): El choque eléctrico es la estimulación física que ocurre cuando la corriente eléctrica circula por el cuerpo. El efecto que tiene depende de la magnitud de la corriente y de las condiciones físicas de la persona, así como el tiempo de exposición. El contacto directo se origina cuando la persona toca directamente un conductor o una parte activa bajo tensión. En general, cuando una persona entra en contacto directo entre una parte activa bajo tensión y tierra o una masa unida a tierra, la tensión de contacto ($VC$) adquiere un valor muy próximo a la tensión simple o de fase ($V = 220 V$). Se produce contacto indirecto cuando el individuo entra en contacto con una masa o una carcasa envolvente de un receptor que accidentalmente presenta un fallo de aislamiento. Debido al fallo, una fase puede entrar en contacto con la envolvente del aparato, presentando este circuito una resistencia (Ri ) debida a la carcasa, pintura, material, etc., del aparato. NOTA es como el ejercicio de la abuela en el hospital y su radio de física.
#### Tipos de protecciones
##### Interruptor diferencial (disyuntor): 
Es un dispositivo electromagnético que se coloca en las instalaciones eléctricas de corriente alterna con el fin de proteger a las PERSONAS de accidentes provocados por el contacto con partes activas de la instalación (contacto directo) o con elementos sometidos a potencial debido, por ejemplo, a una derivación por falta de aislamiento de partes activas de la instalación (contacto indirecto). Es un interruptor que tiene la capacidad de detectar la diferencia entre la corriente de entrada y salida en un circuito. Cuando esta diferencia supera un valor determinado (sensibilidad), para el que está calibrado (30 mA, 300 mA, etc.), el dispositivo abre el circuito, interrumpiendo el paso de la corriente a la instalación. Cuando las corrientes de entrada IF y salida IN no son iguales, los flujos FF y FN creados por ambas corrientes en el núcleo toroidal dejan de ser iguales y el flujo diferencial FF - FN crea una corriente i que activa el electroimán que a su vez posibilita la apertura de los contactos del interruptor. Un botón de prueba permite comprobar el correcto funcionamiento del dispositivo. Al pulsar dicho botón se deriva una corriente IF a través de la resistencia R, siendo ahora IN = 0, activándose el dispositivo. 

Supongamos que alguien toca y nos saca 30mA, entonces vuelven 960 mA. Aparece un flujo remanente en la bobina, genera una fem y activa el electroimán que abre el circuito. Al abrirse deja de circular la corriente sobre la carga por la fuga. El disyuntor detecta esto y protege las descargas. 

Sensibilidad: Corriente mínima que debe que correr para que funcione el disyuntor. Tiempo de reacción, ¿Para qué queremos tener diferentes tiempos de reacción? Para poder serializar los circuitos. Distinguir donde se produce una fuga mediante el tiempo de activación. Una instalación puede tener una fuga a tierra y funcionar sin ningún problema. Pero su función principal es proteger personas. Toda superficie que pueda estar en contacto con las personas tiene que tener una conexión a tierra.
##### Interruptor Termo-Magnético (térmica):
Su funcionamiento se basa en dos de los efectos producidos por la circulación de corriente en un circuito: el magnético y el térmico (efecto Joule). El dispositivo consta, por tanto, de dos partes, un electroimán y una lámina bimetálica, conectadas en serie y por las que circula la corriente que va hacia la carga. PROTEGE CIRCUITOS. 
Se fija si: 
- $\frac{dI}{dt}$ aumenta 
- $\int I ~ dt$ aumenta 
- Si la corriente esta por arriba de la curva la llave térmica salta, es decir sube mucho en poco tiempo (gran derivada!) La integral señala la cantidad de calor que le da. La derivada me protege de un pico de corriente en un corto tiempo.
![[Pasted image 20240422201936.png#center|200]]

Hay 3 clases para clasificar objetos eletrónicos en cuánto a la protección eléctrica que debe tener dependiendo de su uso y donde va a ubicarse.

![[Pasted image 20240430113451.png#center|500]]

![[Pasted image 20240430113623.png#center|600]]

Las distintas normas exigen que los equipos sean sometidos a un número de descargas de cierta amplitud, forma y duración. Es responsabilidad del Ingeniero a cargo del diseño garantizar el cumplimiento de las normas.

Norma 8/20:
![[Pasted image 20240430115052.png#center|300]]
Esta norma es un modelo del rayo. Si mi equipo no aguanta esto → No cumple la norma. Depende de la función de mi equipo, es la norma que tiene que cumplir. Algunos equipos tan solo no tienen que quemarse, mientras que otros tienen que seguir en funcionamiento mientras les esta pegando el rayo.
#### Señales de modo común vs modo diferencial
![[Pasted image 20240430115759.png#center|250]]
La corriente entra por el vivo y sale por el neutro. El disyuntor verifica si hay corrientes de fuga.

![[Pasted image 20240430115903.png#center|250]]

Parte de la tensión se pierde en las inductancias del cable. Además, el aire entre ambos cables actúa como dieléctrico en un capacitor, por lo que el rayo cae en un cable pero por efecto capacitivo viene por ambos. Además tiene tanta energía que consideramos potencia infinita. El que vengan las dos corrientes actúa como señal de modo común.
![[Pasted image 20240430120910.png#center|300]]
#### Protecciones: Serie + Paralelo
![[Pasted image 20240430121436.png#center|200]]
- Serie: debe evitar el paso de la corriente, ofreciendo una alta impedancia entre sus bornes para generar una gran caída de tensión. Si quiere pasar corriente le tiene que dar tensión al serie. Esta protección debe estar antes del paralelo.
- Paralelo: debe evitar que la tensión aumente, ofreciendo un camino de baja impedancia a tierra para la corriente. La corriente que le llegue al paralelo le pide tensión.

**Obs:** Si en un circuito hay uno solo no funciona, se necesitan los dos.

Uno de las protecciones serie-paralelo más básicoes es un LC.
![[Pasted image 20240430122105.png#center|300]]
Un circuito Pasa-Bajos LC detiene las altas frecuencias, “demorando” el avance de la descarga y absorbiendo parte de la energía. El problema es que presenta la misma característica para todas las señales de entrada (señal útil y descargas).

Esta protección es muy útil para señales de modo común, pero no para las diferenciales, ya que si quiero utilizar un equipo, por la inductancia en serie tengo pérdidas. Ante esto, planteamos un LC acoplado, mediante este planteamiento logramos anular los flujos para señales de modo diferencial.

![[Pasted image 20240430122359.png#center|400]]

Esto hace que la impedancia en serie sea mínima, y evita disipar potencia con la corriente de alimentación. Para las señales de modo común, los flujos magnéticos se suman y por lo tanto la impedancia serie es máxima. Permite oponerse a descargas que entren por uno o más cables. Éstas buscan tierra, por lo tanto le estamos dando una salida a tierra y que no nos queme el equipo.

![[Pasted image 20240430123210.png#center|500]]

![[Pasted image 20240430123536.png#center]]

Los capacitores a tierra los tengo que diseñar de modo tal que a señales muy cortas (del orden de $20~\mu s$) quieran ir por el capacitor a tierra, pero a señales de mayor período no tiene que circular por el capacitor.

**Obs:** Un circuito de 4to orden (2 LC) se la banca mucho más que uno en 2do orden (1 LC) con mayores coeficientes.

Cuando la tensión quiere subir de la tensión nominal, los zenners comienzan a conducir corriente. Por lo que a mi circuito le voy a agregar varistores, y su función es, cuando estoy en modo común, los varistores no hacen nada, mientras que cuando cae un rayo y los capacitores se empiecen a cargar, los varistores tienen tan poca impedancia (cuando hay alta tensión) que van a conducir muchisima corriente y se la llevan a tierra. A tensiones bajas, tiene una imoedancia tan grande que circula mucho menos que $1~mA$ (despreciable), y encima es tan baja que el disyuntor no se entera. Por eso, a tensiones normales podemos decir que el varistor no está.

![[Pasted image 20240430125124.png#center|600]]


**Obs:** En los varistores se testea con pulsos cuadrados, ya que si sobrevive al pulso → Sobrevive al rayo.

Los varistores se conectan en paralelo, por lo que debe tener una impedancia en serie.
![[Pasted image 20240503101925.png#center|300]]
![[Pasted image 20240503103609.png#center]]

Elijo un varistor con cierta tensión de la parte A. Una vez obtenemos la corriente de mov ($i_{mov}$) mediante la ec. $i_{mov}=\frac{V_{desc}-V_{mov}}{Z_{L}}$. Utilizo la corriente de mov obtenida y me fijo en el gráfico en que tensión de mov cae. Itero una vez más para verificar que la tensión de mov no sobrepase el pico de tensión que aguante mi equipo.

![[Pasted image 20240503112526.png#center|400]]

**Obs:** Al poner varistores la conexión debe estar hecha de modo que el circuito se conecte al varistor, y el varistor conecte con lo demás, ya que sino la corriente no va a ir por los varistores y no vamos a proteger nada. Además, debemos consguir la mínima impedancia en serie, ya que si tenemos mucho cable por ejemplo, estaríamos añadiendo una resistencia y una inductancia serie, lo que provocaría que la energía del rayo no pase por el varistor (no vaya a tierra), y nos queme el equipo.
![[Pasted image 20240507112323.png#center|100]]
#### Descargadores gaseosos
Cuando tiene baja tensión no circula nada de corriente. Al aumentar la tensión, el gas inerte dentro se ioniza y baja la tensión y la corriente se dispara. Lo disipa en forma de calor.

Los descargadores gaseosos aguantan mucho más corriente que los mov y no sube tensión. Se utilizan para distintos rangos. La desventaja del descargador gaseoso es que sigue conduciendo en la descarga hasta que no llegue a un valor específicco de tensión.
#### Diodo zener
![[Pasted image 20240508102033.png#center|400]]
Suele trabajar con baja potencia. El efecto zener es instantáneo. Mucha tolerancia de fábricación. Se utiliza como último hombre capturando las componentes de mayor frecuencia de las descargas, que pueden haber atravesado las protecciones más robustas.
##### Circuito de protección completo
![[Pasted image 20240507113436.png#center]]

Las descargas suelen tener componentes de muy alta frecuencia, por lo que pueden pasar del primario al secundario por efecto capacitivo, incluso con mínima atenuación.

El zener bidreccional se pone debido a que si la descarga es en un tiempo muy corto (frecuencia muy alta - poca energía) puede saltar las protecciones en paralelo y el zener nos podría proteger.

Todas las protecciones que ponemos tratan de frenar la energía del rayo para intentar evitar que se active el descargador gaseoso. Si el rayo tiene la energía suficiente, se va a activar el descargador gaseoso para enviar toda la corriente a tierra.
##### Pantalla electroestática
Añado el concepto de pantalla electroestática a el modelo de transformador que teníamos, de modo que podamos restar el efecto capacitivo que se induce en estos a altas frecuencias.
![[Pasted image 20240508102510.png#center]]
##### Elección de térmicas
![[Pasted image 20240507115959.png#center|300]]
Por debajo del $i^{2}t$ de mi equipo salta la térmica. Por arriba, funciona, excepto si pasa la línea punteada roja en ese caso, mi equipo se quema. Por lo que si pongo la térmica azul, va a saltar antes de que el equipo se queme. Pero si uso la térmica slow, va a quemarse antes de que salte.

Para un fusible también tengo una curva $i^{2}t$, ya que tarda un tiempo entre que transforma la corriente en calor y se funde. Si le pongo al fusible una cerámica conductora de calor, la cerámica lo enfría mientras se calienta y la curva es más lenta (slow blow). En cambio, una cerámica aislante actúa como fast blow.

Polyswitch-reset fuse: Al calentarse, el plástico se deforma por lo que fluye menos corriente, por lo que se baja la temperatura y se estabiliza.

**Obs:** Las NTC se usan para que al conectar un equipo, no hay corriente al principio → Baja temperatura, la resistencia es grande, y como los caps están descargados, actuan como corto, por lo que las resistencias NTC me ayuda a que no salten chispas, sino que el circuito no esté en corto hasta que los capacitores se comiencen a cargar.