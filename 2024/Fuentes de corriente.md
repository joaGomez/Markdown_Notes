**Fuente de corriente ideal:** Entrega una corriente constante independientemente de la tensión entre sus bornes.

#### Usos
- Usar una fuente de corriente para polarizar una o varias etapas mejora la estabilidad y la sensibilidad frente a cambios de tensión y temperatura.
- Mejora la impedancia de salida.
- Carga activa: La carga que ve el amplificador ahora entrega energía.
- Acople entre etapas.
- Generar señales triangulares.

**Obs:** En las fuentes simples, el valor de la corriente está fijo por la polarización. Mientras que en las fuentes referenciales, el valor de corriente es función del valor de otra corriente denominada corriente de referencia.
### Fuente espejo
- $1^{ra}$ aproximación: 
	![[Pasted image 20241030104359.png#center]]
- $2^{da}$ aproximación:
	![[Pasted image 20241030104458.png#center]]
- $3^{ra}$ aproximación:
	![[Pasted image 20241030104541.png#center]]
Donde $K = \frac{I_{c2}}{I_{c1}}$.
#### Problema con la fuente espejo
La impedancia de salida es $R_{of}= r_{ce2}$. Con la fuente espejo mejorada podemos mejorar la corriente $I_{o}$, para que copie lo máximo posible de $I_{ref}$. Con la fuente espejo proporcional aumentaremos la impedancia de salida.
### Fuente espejo mejorada
![[Pasted image 20241030105219.png#center]]
### Fuente espejo proporcional
La fuente espejo proporcional no sólo mejora la impedancia de salida, sino que se vuelve independiente de la dispersión de la tensión base-emisor.
![[Pasted image 20241030105343.png#center]]
Y la impedancia de salida será: $R_{of}= r_{ce2}\cdot (1+ h^{*}_{fe})$.
### Fuente widlar
La fuente widlar a diferencia de la fuente espejo simple, tiene una resistencia en el emisor de alguno de los transistores.
![[Pasted image 20241030154912.png#center]]
Al colocar la resistencia, la tensión $V_{BE}$ de los transistores serán distintas, por lo que las corrientes serán distintas.

Utilizando la resistencia en el emisor de $Q_2$ aumenta la impedancia de salida, como en la fuente espejo proporcional.

![[Pasted image 20241030155152.png#center]]
### Fuente peak current
![[Pasted image 20241030155333.png#center]]
Donde la impedancia de salida será: $R_{of}=r_{ce2}$.
### Fuente wilson
![[Pasted image 20241030155813.png#center]]
En $1^{ra}$ aproximación $I_{o}\simeq I_{ref}$. Y la impedancia de salida será: $R_{of}= \frac{1}{2}\beta ~ r_{ce3}$.
### Fuente cascode
![[Pasted image 20241030160026.png#center]]
## Resumen
![[Pasted image 20241030160106.png#center]]
