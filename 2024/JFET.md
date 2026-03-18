Es un transistor de efecto de campo.

Se contamina con tipo-p, impurezas con átomos de valencia 3.

![[Pasted image 20240411184734.png]]
Cuan estrecho este esta juntura P-N dependerá de $V_{GS}$ . Si la juntura es de tipo-p la polarización es en inversa, mientras que en tipo-n no.

![[Pasted image 20240411185148.png]]

#### Relaciones I-V
![[Pasted image 20240411185328.png]]
Las características de salida van a depender de mi tensión de entrada $V_{GS}$. También, según mi tensión de entrada voy a tener un punto de trabajo $Q$ en $V_{GSQ}, V_{DSQ}$ y una corriente asociada $I_{DSS}$.

• Efecto de campo (eléctrico): La señal de entrada crea un campo eléctrico que controla el paso de la corriente a través del dispositivo.

• Se los denomina unipolares: Basan su funcionamiento en portadores de un solo tipo: electrones para los de canal N y huecos para los de canal P.

• Principio básico de funcionamiento: Aplicar una tensión al Gate para variar la conductancia (resistencia) del canal.

• Ventajas: Presentan impedancia de entrada muy elevada comparado al BJT.


$$V_{P}=V_{bi}-\frac{qN_{c}a^{2}}{2\varepsilon_{r}\varepsilon_{0}}$$
Siendo $a$ el ancho de la juntura en $V_{P}~\to~(W(V_{P}))$.
$G_{0}= \frac{qZ\mu_{c}N_{c}2a}{L}$ es la conductancia del canal si no hubiera zonas de vaciamiento.

![[Pasted image 20240411191836.png]]

![[Pasted image 20240411192158.png]]

![[Pasted image 20240411192141.png]]

#### JFET en saturación
Cuando el canal se satura/estrangula → $V_{DS}=V_{GS}-V_{P}=V_{DSat}$.

En este estado, la corriente de drain de saturación nos queda:
$$I_{DSat}=\frac{G_{0}V_{DSat}^{2}}{2V_{P}}$$
Una vez estrangulado el canal ($V_{DS}>V_{Dsat}$), la corriente $I_{D}$ ya no depende de $V_{DS}$!

Cualquier punto del canal donde se llegue a -V_P, se va a estrangular. V_GS permite “correr” esa tensión.
$$I_{D}= I_{DSS}\left(1- \frac{V_{GS}}{V_{P}} \right){^{2}}= \frac{G_{0}V_{P}}{2} \left(1- \frac{V_{GS}}{V_{P}} \right){^{2}}$$

![[Pasted image 20240411193230.png]]
Al aumentar $V_{DS}$ se deforma el canal. Si aumento $V_{GS}$ se estrecha.
![[Pasted image 20240411193328.png]]
Cuando ya llego a la saturación, no importa cuanto aumente $V_{DS}$ la corriente ya no se modifica.

**Obs:** La corriente depende solo de la tensión de entrada en la saturación.

Aplicaciones: Fuentes de corriente, amplificadores, llaves (juego yendo de un extremo al otro, o saturado o de corte).
![[Pasted image 20240411193853.png#center|100]]
#### Efecto Early
Después la saturación, aumentar $V_{DS}$ dará lugar a un crecimiento de la longitud de la región estrangulada, haciendo que el punto de estrangulamiento se desplace hacia el Source. Esto disminuirá la resistencia del canal y por ende aumentará levemente la corriente dando lugar a una resistencia dinámica de salida finita. Las proyecciones lineales de las curvan convergen a una tensión llamada tensión de Early ($V_{A}$).
![[Pasted image 20240411194043.png#center|200]]
Así se verían las proyecciones hacia un mismo punto (Tensión de Early).

![[Pasted image 20240411194312.png]]
La primera ecuación corresponde antes a la saturación, mientras que la segunda corresponde a la corriente de drain-source ya en saturación (Donde no depende de $V_{DS}$ → Se ve que no aparece en la ec.)
#### Comportamiento en alterna
Generalmente se asocia un circuito quivalente de un JFET como un cuadripolo. 

Polarizando el transistor con una VGSQ y una VDSQ suficientemente elevada como para que el punto de operación se sitúe en la región de saturación (definido por una IDQ). La tensión alterna que se desea amplificar (vg) se aplica en el Gate, superpuesta a la tensión continua VGS de polarización de Gate. Esta señal generará variaciones de la corriente de Drain, id, que se superponen con la ID de continua. Y producen una variación vd en la caída de tensión de la resistencia RL introducida en el circuito de salida.

![[Pasted image 20240411194840.png]]
Aproximando con polinomio de primer orden de Taylor:
$$i_{d}=g_{D}v_{ds}+g_{m}v_{gs}$$
El primer término es la conductancia del canal ($\frac{1}{\Omega}$), y el segundo es la transconductancia ($\frac{mA}{V}$).

El $g_{m}$ es la ganancia del transistor, ya que es como varía la corriente de la salida, dividido la variación de la tensión de entrada.
$$g_{m}=\frac{-2}{V_{P}}\sqrt{I_{DQ}I_{DSS}}$$
#### Circuito equivalente para pequeña señal y baja frecuencia
![[Pasted image 20240411195540.png]]
La primera expresión de la conductancia es previa a la saturación, y la segunda es posterior.
#### Conclusiones
• El transistor JFET es un dispositivo de 3 terminales que permite controlar la corriente entre drain y source mediante la tensión de gate. Por eso se dice que es un dispositivo controlado por TENSIÓN.

• Analogía de la canilla de agua.

• Como el dispositivo tiene 3 terminales, a diferencia del diodo donde solo teníamos UNA relación I-V, en este caso vamos a tener DOS relaciones I-V.

• Típicamente una va a ser entre $I_D$ y $V_{GS}$ (entrada) y responde a una relación CUADRÁTICA.

• Y otra entre el $I_{D}$ y $V_{DS}$ (salida) que responde primero “QUASI-LINEALMENTE” antes de la saturación y  es prácticamente CONSTANTE después de ella (salvo por el efecto Early).

• Mientras el transistor opere en un punto de polarización $Q$ ($V_{GSQ}, I_{DQ}$), el comportamiento en alterna para señales de pequeña amplitud (o débiles) estará dado por un modelo linealizado (extensión del concepto de resistencia dinámica a un dispositivo de 3 terminales).

• A frecuencias altas, las capacidades parásitas del transistor van a degradar sus características, limitando así su ancho de banda a una frecuencia llamada frecuencia de transición ($f_{T}$).