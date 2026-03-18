### Polarización
- Directa: El diodo comienza a conducir cuando se supera la tensión umbral ($V_{Don}\simeq 0.6/0.7~V$) entre sus bornes. Tras empezar a conducir corriente su comportamiento se podrá modelar de las siguientes maneras:
	- Ideal: Conduce con $V_{D}>0$.
	- Quasi-Ideal: Conduce con $V_{D} > V_{Don}$. Por lo tanto aparece una batería que resta $V_{Don}$.
	- 3ra aproximación: Cuando comienza a conducir a partir de superar la tensión umbral, no solo aparece una batería, sino también una resistencia $r_{d}$. Ésta hará menor la pendiente en la que crece la corriente.
	- Modelo exponencial: La corriente en el diodo se puede modelar como $i_{d}=i_{s}\cdot (e^{\frac{V_{D}}{\eta V_{T}}}-1)$.
- Inversa: En inversa existe la tensión de ruptura/breakdown. A tensiones más pequeñas (en módulo) que la tensión de ruptura, circula una pequeña corriente de saturación en inversa. Ésta es del orden de los $nA/\mu A$. Al superar la tensión de ruptura en inversa, el diodo conduce descontroladamente y puede romper el dispositvo. Algunos diodos como el zener, están fabricados para trabajar en esta zona.

Se superpone continua y alterna para trabajar en el punto Q, donde el diodo se comporta linealmente para pequeña señal → Aparece una resistencia dinámica.
$$g_{D}= \frac{di_{DQ}}{dV_{DQ}}\to r_{d}= \frac{\eta \cdot V_{T}}{i_{DQ}+i_{s}}$$
![[Pasted image 20240824124320.png#center|300]]
### Diodo zener
Éste conduce en inversa y no se quema por efecto Joule cuando se pasa la tensión de ruptura.
$$P_{Z_{MAX}}=V_{Z}\cdot i_{Z_{MAX}}\to i_{Z_{K}}\simeq 10 ~ mA$$
**Obs:** El varicap funciona mejor en inversa ya que en directa la tensión es prácticamente constante, por lo que la capacidad no va a cambiar.