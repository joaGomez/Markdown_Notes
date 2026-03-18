#### Símbolo eléctrico y estructura
![[Pasted image 20240418200311.png#center|400]]
El positivo lo denota el primer caracter de la tensión.
$$V_{EC}=V_{EB}+V_{BC} \qquad I_{E}=I_{C}+I_{B}$$
##### Conexiones
En general vamos a tener una malla de entrada y una de salida. Dependiendo de como se conecte al transistor vamos a decir que uno de sus terminals es COMÚN a esas 2 mallas.
![[Pasted image 20240418200520.png#center|400]]
Estos son los 3 tipos de estas conexiones.
##### Regiones de operación
El transistor bipolar tiene 2 junturas, las cuales pueden estar en directa o en inversa. Lo cual da origen a 4 regiones de operación:

|       Polarización        | Juntura B-E | Juntura B-C |
| :-----------------------: | :---------: | :---------: |
|        Saturación         |   Directa   |   Directa   |
| Modo Activo Directo (MAD) |   Directa   |   Inversa   |
| Modo Activo Inverso (MAI) |   Inversa   |   Directa   |
|           Corte           |   Inversa   |   Inversa   |

#### Diagramas de energía
![[Pasted image 20240418201629.png#center|400]]
![[Pasted image 20240418201932.png#center|400]]
Hay difusión de huecos → Hay corriente. Se reduce el potencial por estar conectada en directa, al igual que se reduce el ancho. 

Dado un transistor PNP con el emisor más dopado que la base y esta a su vez, más dopada que el colector:
![[Pasted image 20240418203145.png#center|300]]
###### Análisis en el emisor
![[Pasted image 20240418203323.png#center|200]]
$$I_{En}=qA \frac{D_{E}}{L_{E}}n_{E0}\left(e^{\frac{V_{EB}}{V_{T}}}-1\right)$$
Donde $L_{E}^{2}= \tau_{E}D_{E}, ~ n_{E0}= \frac{n_{i}{^{2}}}{N_{E}}$.
###### Análisis en el colector
$$I_{Cn}=-qA \frac{D_{C}}{L_{C}}n_{C0}\left(e^{\frac{V_{CB}}{V_{T}}}-1\right)$$
###### Análisis en la base
$$W= W_{B}-x_{EB}-x_{CB}$$
#### Corrientes
![[Pasted image 20240418203810.png#center|350]]
PNP: Una pequeña corriente de electrones controla una gran corriente de huecos.
![[Pasted image 20240418205726.png#center|250]]
#### Parámetros importantes
![[Pasted image 20240418210144.png#center|400]]
Como la base es angosta ($W<<L_{B}$), lo puedo aproximar:
![[Pasted image 20240418210355.png#center|200]]
#### Conclusiones
- El transistor bipolar es un dispositivo controlado por CORRIENTE. 
- En la base se busca que haya la menor recombinación posible para que llegue la mayor cantidad de portadores posible al colector. 
- Según la polarización de ambas junturas el transistor estará operando en distintos regimenes. 
- Hay una curva de entrada y una de salida. 
- Las ecuaciones de Ebers-Moll describen el funcionamiento eléctrico del transistor. 
- El factor de mérito más importante de un BJT es el β y se mantiene constante dentro de un rango de corrientes (ejemplo del tester) y a una cierta temperatura.
#### Distribución de portadores minoritarios
![[Pasted image 20240509184241.png#center|600]]
![[Pasted image 20240509185508.png#center|550]]
![[Pasted image 20240509185542.png#center|600]]
#### Punch-Through (Perforamiento)
![[Pasted image 20240509185646.png#center|200]]
Si las zonas desiertas se tocan, se destruye el dispositivo.

Un aumento en la tensión C-B va a afectar a B-E, disminuyendo la barrera de potencial y aumentando todavía más la corriente. Generalmente la corriente aumenta tanto que la disipación de potencia excede el límite de operación segura (SOA, Safety Operation Area) y la falla se vuelve no reversible.
![[Pasted image 20240509190023.png#center|200]]
La variación de potencial en un transistor PNP después de la avalancha, cuando la anchura efectiva de la base se ha reducido a cero. La barrera de emisor efectiva es $V'$.

##### Impact ionization (avalancha)
En general la juntura C-B será la que soporte la mayor tensión de operación. Si esta juntura llega a la ruptura por efecto Zener (sea tanto por efecto túnel como por avalancha), el transistor dejará de comportarse como tal y basicamente será un diodo zener con un diodo en serie. 

El alto campo eléctrico de la juntura C-B hace posible el efecto de multiplicación de portadores (ionización por impacto). Este mismo efecto se usa en los fototransistores, donde la generación de los pares electrón laguna se deben a la incidencia de un fotón, en vez de la colisión de un electrón.
![[Pasted image 20240509190329.png#center|200]]
Aumento drástico de la corriente de colector (tiende a infinito). Para las cuentas se utiliza un multiplicador (M), tal que $M=\frac{1}{1-(\frac{V_{CB}}{BV_{CBG}})^{n}}$.

Si la ruptura por avalancha/breakdown, sucede antes que la de perforamiento, la tensión de BC va a depender de la tensión de breakdown.

![[Pasted image 20240509191014.png#center|300]]
Donde $BV_{CEO}=BV_{CBO}\sqrt[n]{\frac{1}{h_{FE}}}=0.52 \cdot BV_{CBO}$
##### Ganancia de corriente en base común
![[Pasted image 20240509191339.png#center|500]]
##### Ganancia de corriente en emisor común
![[Pasted image 20240509191411.png#center|500]]
$I_{CB0}$ es la corriente de colector que circula entre colector y base cuando el emisor está a circuito abierto (por eso el $0$). En nuestro desarrollo, sería la $I_{Cn}$. Analogamente, $I_{CE0}$ es la corriente de colector que circula cuando la base está en circuito abierto.
![[Pasted image 20240509191652.png#center|400]]
##### Saturación
Si queremos usar el transistor como llave: ON → $V=0$, OFF → $I=0$.

En corte está claro que el transistor está prácticamente apagado y la única corriente que se va a tener es la corriente de saturación inversa a través de las junturas. En saturación:
![[Pasted image 20240509191909.png#center|300]]
![[Pasted image 20240509192130.png#center|500]]

La malla de salida (colector) es la que define si el transistor está en saturación o no. En este caso $R_{c}$ empuja al colector a saturación por un aumento desmedido de la corriente.

![[Pasted image 20240509192732.png#center|400]]
En saturación, $\beta_{DC}= \frac{I_{c}}{I_{B}}$. Como ambas junturas están en directa pero son opuestas, $I_{c}$ baja, pero a su vez $I_{B}$ aumenta desmedidamente por la recombinación de los portadores del emisor y del colector, haciendo que la ganancia de corriente baje considerablemente. En circuitos lineales se busca evitar esto a toda costa.

##### Modelo de corriente alterna
Pensamos al transistor como una caja negra con las siguientes tensiones y corrientes de entrada y salida.

**Obs:** Si la tensión está en mayúscula, es directa. Si es en minúscula, es alterna/pequeña señal/bias.

![[Pasted image 20240509193437.png#center|300]]
![[Pasted image 20240509193833.png#center|350]]
![[Pasted image 20240509194045.png#center|500]]
![[Pasted image 20240509195750.png#center|500]]
En general, la base emisor está en directa → Predomina la capacidad de difusión.

Teniendo en cuenta las capacidades, el modelo equivalente de Giacoletto será:
![[Pasted image 20240509200222.png#center|300]]
Donde $C_{\pi}$ y $C_{\mu}$ son las capacidades calculadas anteriormente, $r_{\mu}$ es la resistencia inversa entre B-C y se la puede estimar como $r_{\mu}=\beta r_{0}$. $r_{b}$ es la resistencia intrínseca de base que representa la resistencia entre el contacto externo de base y la base interna del transistor.

![[Pasted image 20240509200419.png#center|400]]
Se construyen de esta forma para obtener ganancias decentes. $W_{B}$ tiene que ser mucho menor al diámetro de un conductor normal. El colector no se tiene en cuenta porque se agrega una zona $n^{+}$ llamada Buried layer que permite reducir esta resistencia.

Otras formas de representar el modelo linealizado del transistor es mediante parámetros: Z (Impedancia), Y (Admitancia), H (Híbrido), G (Híbrido inverso).

![[Pasted image 20240509200725.png#center|200]]
![[Pasted image 20240509200750.png#center|200]]
![[Pasted image 20240509200821.png#center|200]]

![[Pasted image 20240509200900.png#center|500]]

![[Pasted image 20240509202157.png#center|500]]
