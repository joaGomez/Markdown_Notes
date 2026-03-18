El JFET es un transistor de efecto de campo de juntura. Hay de dos tipos, canal N, y canal P. El tipo de canal determinará la polarización de las tensiones $V_{GS}$ y $V_{DS}$, y también la corriente de drain $i_{d}$.

**Obs:** La corriente de drain-source es contolada por la tensión en el gate.

![[Pasted image 20240905115949.png#center]]

Como se polariza en inversa, la corriente en el gate es muy chica → La impedancia de entrada es muy grande. Por lo tanto, se toma $i_{G}\simeq 0 \longrightarrow i_{D}=i_{S}$. Una sola corriente atraviesa drain y source. Como la corriente de entrada es prácticamente nula, la potencia de entrada es cero.

**Obs:** En canal N, la corriente va de drain a source. Mientras que en canal P, la corriente va de source a drain. Opuesto a la dirección de la tensión $V_{DS}$ en ambos casos.

La expresión de la corriente en saturación es: $$i_{d}=i_{DSS}\cdot \left(1- \frac{V_{GS}}{V_{P}}\right)^{2}$$
Mediante esta expresión, se pueden hallar las curvas de transferencia, tanto para canal N, como para canal P.

![[Pasted image 20240905120622.png#center]]

**Obs:** $i_{DSS}$ es la corriente $i_{D}$ que circula cuando $V_{GS}=0$. Y $V_{P}$ es la tensión de pinchoff. Es la tensión entre el gate y source aplicada que genera que la corriente de drain sea cero.

### Curvas de salida
![[Pasted image 20240905120935.png#center]]

### JFET como amplificador
Antes que nada, se debe buscar el punto Q de trabajo, cuando o hay señal de entrada. Se calcula $i_{DSQ}$ y $V_{GSQ}$ con la malla de entrada, y $V_{DSQ}$ con la malla de salida. También, conociendo la curva de la corriente de drain, si se halla la recta de polarización de $V_{GS}$, en el punto que estas se intersecten es el punto Q.

![[Pasted image 20240905121917.png#center]]

**Obs:** El amplificador en este caso debería de invertir de fase. Cuando aumenta $I_{DQ}$ disminuye $V_{DSQ}$.

Para evitar distorsión, la amplitud de la señal debe ser chica. Esto se debe a que la curva que describe la corriente es cuadrática, no lineal.

### Circuitos equivalentes
- Circuito equivalente de alterna para pequeña amplitud y bajas frecuencias:
	![[Pasted image 20240905122304.png#center]]
- Circuito equivalente de alterna para pequeña amplitud y altas freuencias:
	![[Pasted image 20240905122400.png#center]]

La transconductancia del JFET se calcula como:
$$g_{m}= \frac{dI_{d}}{dV_{GS}}= \frac{d}{dV_{GS}}\left(i_{DSS}\cdot \left(1- \frac{V_{GS}}{V_{P}}\right)^{2}\right)=-2\cdot \frac{i_{DSS}}{V_{P}}\cdot \left(1- \frac{V_{GS}}{V_{P}}\right)$$
