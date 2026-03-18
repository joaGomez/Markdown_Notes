#### Pilas y baterías
- Primarias: Su reacción química es difícilmente reversible. Se diseñan para un sólo uso, con posterior descarte y reciclado.
- Secundarias: Su reacción es prácticamente reversible. Se diseñan para ser recargadas. El rendimiento de carga suele ser aproximadamente del 50%. Tienen (en general) menor densidad de energía, pero mayor densidad de potencia que las primarias.
![[Pasted image 20240523154131.png#center|400]]
- Terciarias: 
	- Su reacción química se activa al momento del uso.
	- Tienen una enorme capacidad de potencia.
	- Se diseñan para un sólo uso, con un largo período de almacenamiento. Luego de ser usada debe ser reemplazada.
	- Generalmente, se basan en almacenar el electrolito por separado, con algún sistema automático para el armado de la batería.
![[Pasted image 20240523154416.png#center|50]]
#### Celdas de combustible
Realizan una reacción química entre dos compuestos combustibles, mediante el uso de membranas químicas y catalizadores. Las más comunes son las celdas PEM (Proton-exchange Membrane).
![[Pasted image 20240523154527.png#center|200]]
#### Paneles solares
![[Pasted image 20240523154612.png#center|600]]
Un problema con los paneles solares es que en la conexión tradicional, la batería se carga sólo cuando la tensión del panel solar es mayor que la tensión de la batería. Si la tensión de los paneles es muy alta, la batería se daña severamente. Mientras que si se usan paneles de menor tensión, la batería se carga sólo cuando hay mucha radiación (Al mediodía y sin nubes).

![[Pasted image 20240523154932.png#center|350]]

Por lo tanto, para resolver esta problemática, utilizamos la electrónica de potencia. Realizamos una conexión correcta mediante un circuito con algotimos MPPT, el cual busca encontrar el mayor nivel de potencia que puede ofrecer un sistema solar fotovoltaico.

![[Pasted image 20240523155157.png#center|300]]

#### Baterías de flujo
La energía se almacena en el electrolito, la estructura de la batería no se modifica con la carga y descarga. Permite acumular grandes cantidades de energía (tanta como lugar tenga para almacenar el electrolito cargado). Incluso permite transportar electrolito cargado de un lugar a otro, lo que se utiliza en aplicaciones de emergencias y catástrofes (además de militares). Se usan también como almacenamiento provisorio en energías alternativas y como sistema de backup en aplicaciones industriales.

#### Capacidad nominal
Se define con la letra $C$ y su unidad es el **amperhora**.

**Obs:** Los fabricantes no están obligados a seguirlas y por lo tanto muchas veces se utiliza como elemento de marketing.

La norma más usada especifica que C es el valor de Amper * Horas de una batería que soporta una descarga de C/20 durante 20 hs.

##### Cálculo de la capacidad real
El valor de la capacidad real la podemos obtener multiplicando la capacidad nominal por factores $k_{i}$ que dependerán de las condiciones, como temperatura, número de ciclos, etc.

> Ejemplo
> ![[Pasted image 20240523161142.png|500]]
##### Uso de las baterías
- Standby → Carga a flote
- Cycle → Carga rápida

1. $V=cte:$ Primero se carga rápidamente hasta poder llegar al punto de tensión cte y se cargue lentamente. Al llegar al máximo, se carga a flote. Ej: Litio-Polímero.
![[Pasted image 20240524113945.png#center|400]]
2. $i=cte:$ Se utiliza corriente cte para evitar estar conectada a una tensión. No se pueden usar mientras se cargan. Ejemplo: Níquel-Metal.

![[Pasted image 20240531192404.png#center|400]]
