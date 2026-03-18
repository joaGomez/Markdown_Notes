Hay 3 modos: Conducción, readiación, convección.

#### Conducción
La conducción es la transferencia de energía térmica a través de un medio.

Para un conductor rectángulo, de largo $d$, material de conductividad térmica $\lambda$, sección $b\times h(A_{c})$, donde el flujo de calor $Q$ va de una temperatura $T_{2}$ a $T_{1}$. Podemos definir una resistencia térmica como: $$R_{\theta}= \frac{d}{\lambda A_{c}}$$
Donde se cumple que: $$Q= \frac{\lambda A_{c}}{d}(T_{1}-T_{2})=\frac{(T_{1}-T_{2})}{R_{\theta}}$$
**Obs:**
![[Pasted image 20240508103917.png#center|400]]
###### Sugerencias en la aplicación de la conducción térmica:
- Todas las superficies de interfaz deben ser lisas y planas. Se deben utilizar grasas térmicas o pads de interfaz térmicos en todas las interfaces siempre que sea posible.
- Los semiconductores deberían estar espaciados para obtener una densidad de potencia uniforme.
- Si una parte de la carcasa del equipo se va a utilizar como un disipador de calor, asegúrese que el espesor de los materiales y que las zonas de interfaz son los adecuados para manejar la densidad de potencia esperada.
#### Radiación
La radiación es la transferencia de energía calórica en forma de ondas electromagnéticas entre dos superficies a diferentes temperaturas. Es más eficaz cuando se produce en el vacío.

###### Ec. de Stephan-Boltzmann
$$\begin{align*}
Q &= \varepsilon \sigma A_{r}(T_{s}^{4}-T_{a}^{4})\\
hr &= \varepsilon \sigma (T_{s}+T_{a})(T_{s}^{2}-T_{a}^{2})
\end{align*}$$
Donde $R_{\theta}= \frac{1}{h_{r}A_{r}}$
###### Consejos para disipar por radiación:
- Maximizar la emisividad de la superficie.
- Maximizar el área de superficie expuesta no obstruida.
- Las únicas superficies radiantes son aquellas en vista plana (no la superficie total). El área entre las aletas irradia una en la otra.
- Use un disipador de alta conductividad y materiales de interface para minimizar la resistencia térmica de la carcaza a la superficie radiante y aumentar la diferencia de temperatura entre la superficie de disipación y las moléculas del aire ambiente.
#### Convección natural
Es el flujo de fluido inducido por fuerzas de flotación, que se derivan de la diferencia de densidades, causada por variaciones de temperatura en el fluido. La convección es la transferencia de energía térmica de una superficie caliente a un fluido en movimiento (aire, agua, etc) a una temperatura inferior. Es el modo de transferencia de calor más difícil de predecir matemáticamente porque depende en gran medida de la disposición física del sistema.
![[Pasted image 20240508104820.png#center|200]]

Para disipadores de cobre o de aluminio, en el rango de temperaturas normales de electrónica ($-50°C/250°C$) a presión atmosférica normal, se cumple la siguiente expresión:
$$\begin{split}
Q&=1.34\cdot A_{s}\cdot \frac{(\Delta T)^{1.25}}{(d_{vertical})^{0.25}} \\
R_{\theta, conv}&= \frac{1}{1.34\cdot A_{s}}\left(\frac{d_{vertical}}{\Delta T}\right)^{0.25}
\end{split}$$
Se suele utilizar una aproximación lineal para casos de baja precisión o estimación de valores: $$Q= h\cdot c\cdot A_{s}(T_{s}-T_{a})$$
![[Pasted image 20240508105434.png#center|130]]
**Obs:** Para la misma área de disipación, el de menor altura disipa mejor porque aprovecha mejor la diferencia de temperatura entre la superficie del disipador $T_{s}$ y la temperatura ambiente (del aire) $T_{a}$.
##### Circuito térmico equivalente
![[Pasted image 20240508105635.png#center]]
El valor de $R_{\theta jc}$ lo obtengo de la hoja de datos. $R_{\theta cs}$ es un factor que depende si uso grasa siliconada o pasta térmica (valores típicos de $0.5\frac{°C}{W}$ o $0.3\frac{°C}{W}$) 
##### Interfaces case-sink
Debido a la rugosidad natural entre la superficie del disipador y la del componente, la transferencia de calor no es muy eficiente. Para mejorar la transferencia de calor se utilizan distintos tipos de compuestos: 
- Grasa siliconada: es la más económica y la preferida para baja escala de producción y trabajos artesanales
- PADs: buenos conductores del calor, algunos pueden ser aislantes eléctricos también. Algunos fabricantes ofrecen incorporarlo al disipador en fábrica. 
- PCM (Phase Change Material): permiten adaptarse mejor a la forma de la interface cuando se calienta el sistema.

![[Pasted image 20240510105624.png#center|700]]
El valor obtenido de la resistencia térmica es máximo debido a que trabajamos a partir de una temperatura de $150°C$.

**Obs:** La resistencia térmica es inversamente proporcional al torque aplicado al tornillo de fijación, hasta llegar a un mínimo (máximo torque) donde el componente se empieza a deformar por lo que la superficie de contacto disminuye. Debe tenerse especial cuidado en no aplicar demasiada presión ya que puede deformarse el componente o el disipador, empeorando la transferencia térmica.

La convección forzada es el flujo de fluido causado por medios externos (e.j. ventiladores, bombas, etc.). La eficiencia disminuye con la velocidad del aire debido al menor tiempo que tiene el fluido para absorber el calor de la superficie. El desgaste mecánico y ruido acústico son las principales contras de este método.

![[Pasted image 20240510112219.png#center|150]]
Se fabrican mediante procesos mecánicos como el estampado o mecanizados más complejos. Se busca maximizar el área en relación al volumen, también adaptarse a requerimientos especiales de aplicaciones y encapsulados.

![[Pasted image 20240510114110.png#center|300]]
Este tipo de gráficos son importantes. Se lee de la siguiente manera: La curva apunta a los ejes que debo usar. Por ej, la curva de abajo, apunta a los ejes de abajo y de la izquierda, por lo que debería de usar esos para leer esa curva.

![[Pasted image 20240510114301.png#center|150]]
Se fabrican mediante el proceso de “extrusión” que consiste en hacer pasar el material fundido (generalmente aluminio) por una boquilla que le da la forma. Se fabrican en barras de 3 ó 6 metros de largo. Al público se ofrecen en distintos largos, siendo la longitud “nominal” 3 pulgadas. Los de mejor calidad están anodizados por pieza, los de peor calidad se anodiza la barra entera por lo que los bordes quedan con el acabado del material virgen Suelen tener aletas para mejor la relación entre el área para disipar y el volumen total del disipador.

**Obs:** Una pulgada equivale a $25~mm$.

En caso que se utilice un disipador con largo distinto a 3in, o que su elevación de temperatura con Ts-Ta sea distinta a 75ºC, se pueden utilizar las siguientes tablas de corrección:

![[Pasted image 20240510114705.png#center|600]]

![[Pasted image 20240514122008.png#center|500]]

##### Espaciado de aletas (Fin spacing)
Aletas finas → Ventilación forzada. Aletas más espaciadas → Convección natural.

Para aumentar la relación entre el área y el volumen total del disipador se suelen agregar aletas. Si las aletas se encuentran muy próximas, se producen efectos mecánicos que reducen la movilidad del fluido entre las aletas. Existe una relación entre la mejora en el área y la pérdida de eficiencia por poner más aletas en el mismo volumen (reduciendo la distancia entre ellas). Aproximando la disipación por convección: $Q=hA_{c}\Delta T$. Donde $h$ es el coeficiente de transmisión de calor, función del espaciado y la altura de las aletas. El espaciado de aletas controla el flujo de aire libre. El área efectiva As aumenta a medida que disminuye la separación de aletas (para iguales dimensiones externas).

![[Pasted image 20240514125122.png#center|500]]

**Obs:** Para convección natural me importa la orientación del disipador. Pero en convección forzada ya no es tan importante.
##### Celdas Peltier
Utilizan el efecto Peltier, que permite transferir entre dos superficies de un semiconductor mediante el paso de una corriente eléctrica. Cuando se instalan entre el disipador y el componente a enfriar permiten mejorar la transferencia térmica mediante dos efectos: 
- Calentar el disipador: con lo que mejorar la eficiencia.
- Enfriar el componente: permiten trabajar a menor Tj.

Tienen un rendimiento muy pobre, generalmente inferior al 50%, eso quiere decir que para mover 1W de calor, es necesario gastar 2W de energía eléctrica.

![[Pasted image 20240517104922.png#center|300]]

![[Pasted image 20240517104946.png#center|300]]
Si se invierte la polaridad de la conexión eléctrica, se invierte el sentido de circulación de calor. Esto permite hacer equipos de: 
- Regulación de temperatura (crecimiento biológico).
- Ciclado térmico (calor-frío-calor-frío…). 
- Calefacción controlada.
##### Efecto termoeléctrico(Thomson)
Cuando se le entrega calor a un par de metales, de distinto potencial electroquímico, aparece una diferencia de potencial y la posibilidad de hacer circular una corriente eléctrica de la que se puede obtener energía. El ejemplo más usado es la válvula de seguridad de artefactos a gas, donde la termocupla calentada por la llama genera una corriente que al pasar por un bobinado genera un campo magnético que atrae al pestillo de apertura de la válvula de gas. Si se apaga la llama se cierra el paso del gas.
![[Pasted image 20240517105424.png#center|200]]
#### Convección forzada
![[Pasted image 20240517111754.png#center|400]]
Esta gráfica muestra la diferencia de presión en mi gabinete para la corriente de aire que va a circular por él.

Luego, tengo otra gráfica, la del disipador. Ésta va a representar el flujo de aire que puede entregar mi ventilador.
![[Pasted image 20240517112037.png#center|500]]
Por lo que si superpongo las dos gráficas, encuentro el punto de operación de mi gabinete.