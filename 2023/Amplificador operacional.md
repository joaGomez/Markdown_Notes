Los amplificadores operacionales son componentes activos.
![[Pasted image 20231010202812.png|500]]
							
								Modelo ideal

En el modelo ideal, la $R_{input}\to\infty$ y la $R_{output}\to0$.
**Obs.** Para tener el control, utilizo un ampplificador operacional realimentado. La realimetación negativa me da *control*, la positiva me lo amplifica demasiado y se *satura*.

**Ejemplo**
![[Pasted image 20231010205422.png]]
### Sumador
![[Pasted image 20231019110406.png|400]]
En los ideales: $V_{A}=V_{B}$, "Tierra virtual".
Consideramos $R_{input}\to \infty \Rightarrow I_{input}=0 \Rightarrow \Delta V_{AB}=0$.
Entonces, obtenemos que $V_{out}=-(\frac{V_{1}}{R_{1}}+ \frac{V_{2}}{{R_{1}}})R_{3}$, con signo negativo porque entra por el negativo.

### Integrador
![[Pasted image 20231019111646.png|400]]
$V_{out}= \frac{V_{1}}{R_{1}} \frac{1}{j.\omega C}$
**Obs.** Está integrando la señal de entrada. $L. \frac{di}{dt}\longrightarrow j\omega L.I= \frac{1}{j\omega C}I$

Por ej, si entra una señal triangular, sale una señal cuadrada.

### Buffer
![[Pasted image 20231019112033.png|400]]
**Obs.** La función del buffer es aislar eléctricamente la entrada de la salida. Las corrientes NO se van a compartir, pero sostienen la tensión → $V_{input}=V_{out}$.
