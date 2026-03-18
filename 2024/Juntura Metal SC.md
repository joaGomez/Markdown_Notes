Este tipo de junturas se denominan heterogéneas. La función de trabajo $q\phi_{M}$ para metales y $q\phi_{S}$ para SC se define como la energía necesaria para remover un electrón del nivel de Fermi hacia el vacío. La afinidad electrónica $qX$ se define como la energía necesaria para remover un electrón desde el inicio de la banda de conducción hacia el vacío. $\phi_{M}$ y $X$ dependen del material, mientras que $\phi_{S}$ puede cambiar en un mismo material debido al dopaje. Hay dos tipos de junturas: 
• Rectificante (Diodo Schottky): 
	• $\phi_{M}$ > $\phi_{S}$ para SC tipo-n 
	• $\phi_{M}$ < $\phi_{S}$ para SC tipo-p 	
• Ohmica: 
	• $\phi_{M}$ < $\phi_{S}$ para SC tipo-n 
	• $\phi_{M}$ > $\phi_{S}$ para SC tipo-p
	
![[Pasted image 20240404200918.png#center|300]]
### Diodo Shottky en equilibrio
Al ponerse en contacto un metal con un SC tipo-n y considerando el caso $\phi_{M}$ > $\phi_{S}$ , los electrones de la banda de conducción comenzarán a moverse hacia el metal para ocupar los estados libres debajo de la energía de Fermi. Los electrones difundidos dejan atrás cargas positivas que formarán una zona desierta del lado del SC. Del lado del metal las cargas difundidas se acumularán en la superficie. No hay zona desierta en el metal. Se crea una barrera de Schottky $\phi_{B}$ = $\phi_{M}-X$ la cual deben vencer los electrones que deseen pasar del metal al SC. Esta barrera es independiente de la tensión de polarización. Del lado del SC, aparece una barrera de potencial que impedirá que electrones sigan inyectándose al metal. Dicha barrera está dada por $qV_{bi} = q\phi_{B} - (E_{c}-E_{F})_{FB}$

![[Pasted image 20240404202318.png#center|400]]
### Diodo Shottky con polarización en directa
El diodo estará en directa cuando la tensión positiva esté en el metal. La energía de Fermi del metal queda por debajo de la del semiconductor. La barrera $qV_{bi}$ se reduce favoreciendo la inyección de electrones hacia el metal. Contrario a lo que sucede en una juntura pn, la corriente en un juntura metal-SC se debe a los mayoritarios a través de un proceso denominado emisión termoiónica.

![[Pasted image 20240404202426.png#center|400]]
### Diodo Shottky con polarización en inversa
El diodo estará en inversa cuando la tensión positiva está en el SC. La energía de Fermi del semiconductor queda por debajo de la del metal. La barrera $qV_{bi}$ se incrementa dificultando la inyección de electrones hacia el metal. La corriente estará dada por los electrones capaces de saltar la barrera de Schottky.

![[Pasted image 20240404202756.png#center|400]]

**Obs:** Como la barrera de Shootky es mayor para que los electrones salten de un lado al otro → Corriente más pequeña que en directa.
### Electroestática de la zona desierta

![[Pasted image 20240404202841.png]]
### Resumen diagrama de bandas

![[Pasted image 20240404202919.png#center|400]]
### Corriente
La corriente en el diodo Shottky está dada por:
$$I=I_{0}(e^{\frac{V_{A}}{V_{T}}}-1) → I_{0}= A\cdot \mathcal{A}\cdot T^{2}\cdot e^{\frac{-\phi_{B}}{kT}} → \mathcal{A}=\frac{4\pi m_{e}k^{2}q}{h^{3}} $$
![[Pasted image 20240404203352.png]]
### Juntura óhmica
Son no-rectificantes, es decir, la corriente va a circular en ambos sentidos. Se dan cuando se necesita contactar al semiconductor desde el exterior (por ejemplo los pines de un circuito integrado). Los electrones (en SC tipo n) y los huecos (en SC tipo p) pueden moverse fácilmente hacia el metal así como los portadores en el metal pueden moverse fácilmente hacia el SC.

![[Pasted image 20240404203719.png#center|400]]
### Conclusiones
- Para poder resolver circuitos con diodos es necesario linearizar la curva I-V alrededor de su punto de equilibrio Q 
- La juntura PN presenta dos capacidades: capacidad de juntura (domina en inversa) y capacidad de difusión (domina en directa) 
- La juntura metal-SC puede ser tanto rectificante (diodo Schottky) como no rectificante (óhmica). Va a depender de lo relación entre las funciones de trabajo del metal y el SC así como del tipo de SC 
- Para los casos que se van a estudiar es posible utilizar la aproximación de Boltzmann 
- La Energía (Nivel) de Fermi representa el nivel energético más alto que puede tener un sistema a $𝑇 = 0𝐾$
- La Energía de Fermi está por encima de la Energía de Fermi Intrínseca para un SC tipo-n y debajo para un SC tipo-p 
- Hay diferentes ecuaciones que relacionan los parámetros de interés: $n_{i} , n_{0}, p_{0}, E_{Fi} , E_{F}$