Motor eléctrico: Es una máquina que transforma energía eléctrica en energía mecánica. Hoy en día existen de varios tipos: Rotatorias, lineales, y otras especiales.

![[Pasted image 20240617203752.png]]
Algunas partes de un motor eléctrico son:
- Estator: Parte fija
- Rotor: Parte móvil que gira dentro del estator.
- Inductor: Es el que genera el campo magnético.
- Devanado inducido: Convierte la energía eléctrica del estator en energía mecánica de rotación.
- Entrehierro: Espacio de aire que separa el estator del rotor, y permite la existencia del movimiento.

##### Rotor
En motores de corriente continua se da el nombre de armadura tanto al paquete de chapas que sostiene el bobinado inducido, como al conjunto de los conductores que constituyen el bobinado. En general el bobinado de armadura es también el rotor.

##### Estator
El bobinado de Campo es el que crea el campo magnético fijo, que se suele llamar Excitación. En los motores pequeños se consigue con imanes permanentes. Cada vez se construyen imanes más potentes, y como consecuencia aparecen en el mercado motores de excitación permanente, mayores. En general el bobinado de campo es el que está fijo y en ese caso también es el Estator.

##### Bobinados
Según su función eléctrica:
1. Campo: Es el que produce el campo eléctrico.
2. Armadura: Por el que circula la corriete que genera la fuerza al interactuar con el campo.
Según su función mecánica:
1. Estator: Está fijo.
2. Rotor: Gira.

En muchos motores, como los de máquinas eléctricas, electrodomésticos, etc., el bobinado de armadura es el rotor. En motores utilizados para tracción eléctrica (autos, motos, bicicletas) o generación (eólica, turbinas hidráulicas, etc.) el bobinado de armadura suele ser el estator. Generalmente en estos motores el campo se realiza con imanes permanentes.

##### Motores de corriente continua
Se utilizan en casos en los que es de importancia el poder regular continuamente la velocidad del eje y en aquellos casos en los que se necesita de un toque de arranque elevado. Por ejemplo motores para utilizar en el arranque y en los controles de automóviles, motores accionados a pilas o baterías, etc. Para funcionar, el motor de corriente continua o directa precisa de dos circuitos eléctricos distintos: el circuito de campo magnético y el circuito de la armadura. El campo (básicamente un imán o un electroimán) permite la transformación de energía eléctrica recibida por la armadura en energía mecánica entregada a través del eje. La energía eléctrica que recibe el campo se consume totalmente en la resistencia externa con la cual se regula la corriente del campo magnético. Es decir ninguna parte de la energía eléctrica recibida por el circuito del campo, es transformada en energía mecánica. El campo magnético actúa como una especie de catalizador que permite la transformación de energía en la armadura. La armadura consiste en un grupo de bobinados alojados en el rotor y conectados a un colector mediante el cual se recibe corriente continua desde una fuente exterior y se convierte la correspondiente energía eléctrica en energía mecánica que se entrega a través del eje del motor. En la transformación se pierde un pequeño porcentaje de energía en los carbones del colector, en el cobre de los bobinados, en el hierro (por corriente parásitas e histéresis), en los rodamientos del eje y la fricción del rotor por el aire.

![[Pasted image 20240617204700.png]]
#### Motores de corriente alterna
![[Pasted image 20240617210006.png]]
El estator es como un campo magnético rotante, el cual gira espacialmente a una velocidad denominada velocidad de sincronismo. La velocidad de sincronismo (sincronismo/freucncia angular de $\vec{B}$) $\omega_{s}= \frac{60\cdot F}{PPF}$ y $\omega_{r}$ es la velocidad de giro del rotor. La velocidad relativa entre el estator y el rotor es $S=\omega_{s}-\omega_{r}~[RPM]$, por lo que la frecuencia que ve el rotor será $F_{r}= \frac{S\cdot PPF}{60}$.
![[Pasted image 20240617210221.png]]
![[Pasted image 20240604112253.png#center|400]]
###### Curva torque-velocidad
![[Pasted image 20240617210321.png]]
Al cambiar la forma de las barras, más el material, logra modificar la curva de torque. La forma de la barra me modifica la inductancia en el motor, y el material modifica la resistencia interna. En otras palabras, modificando la forma y el material de las barras del rotor es posible controlar la relación entre las corrientes del rotor y el deslizamiento ‘s’, obteniendo distintas curvas torque-velocidad.

###### Control de velocidad V/F=cte
Dado que la energía llega al rotor por medio del campo magnético B, es posible modificar el marco de referencia temporal sin modificar la forma de la curva, manteniendo la relación V/F constante. La curva se desplaza de acuerdo a la nueva velocidad de sincronismo $\omega_{s}= \frac{60~f}{P~P_{f}}$
![[Pasted image 20240617210526.png|150]]
![[Pasted image 20240617210551.png]]
Utilizando herramientas de Electrónica de Potencia, se puede hacer un circuito (llamado inverter) que permita modificar tanto la tensión como la frecuencia del sistema trifásico con el que se alimenta al motor. La combinación motor + inverter permite controlar las condiciones de trabajo del conjunto motor+carga, regulando velocidad, torque o cualquier otra variable física medible. Los inverters son fácilmente programables para generar patrones de aceleración o velocidad que permitan un control óptimo del sistema.

Frenado regenerativo: Para los tiempos característicos de control de la electrónica ($ms$ o $\mu s$), la inercia de la carga hace que su velocidad pueda ser considerada constante
![[Pasted image 20240617210733.png]]

![[Pasted image 20240604114959.png#center|600]]
En las hojas de datos me dan el $\omega_{n}$ y el torque nominal, por lo que con esos datos hago una recta que choque con el torque = 0. Esa recta vale para toda la recta, por lo que para lo que sea que me pida el ejercicio, puedo desplazar la recta y mientras siga teniendo en cuenta el desplazamiento, puedo calcular la frecuencia para cualquier punto. Además, el fabricacante nos suele dar la frecuencia nominal, es decir, la frecuencia con la que se realizaron las mediciones.

**Obs:** Si en un ejercicio no me dicen nada, tomo $\omega_{n}=2\pi 50Hz$.

##### Motores asincrónicos de inducción
- Monofásicos: con espira de sombra o polo sombreado. Se coloca una “espira de sombra” en corto circuito. La FEM inducida sobre ella generará una corriente y ésta a su vez un campo magnético, a 90º del campo original. Se utilizan para aplicaciones de muy baja potencia (50W), con cargas que requieran un bajo torque de arranque.
- Monofásicos: con bobinado auxiliar y capacitor. El capacitor en serie con el bobinado auxiliar genera un desfasaje en la corriente, por lo que el campo magnético producido por ese bobinado estará desfasado igualmente.

##### Motores stepper/Brushless
Los motores stepper o paso a paso se utilizan donde se requiere precisión en la posición angular del motor. Requieren electrónica externa para controlar qué bobinas se encienden en cada paso. El rotor puede quedar estacionario por largo tiempo en una posición fija.

Los motores brushless se utilizan donde se requiere precisión en la velocidad angular del motor. Requieren electrónica externa para controlar qué bobinas se encienden en secuencia continua. El rotor debe girar continuamente a la velocidad de sincronismo con el encendido de las bobinas.

#### Tipos de rotores
![[Pasted image 20240618081524.png]]
![[Pasted image 20240618081622.png]]