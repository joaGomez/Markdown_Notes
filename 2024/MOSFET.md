Con un sustrato tipo p, se arma un NMOS. Y con un sustrato tipo n, armo un PMOS. Estos son los *body* del transistor. En cada sustrato, pongo dos contactos (Drain y Source) en el principio y fin del canal (para que circule corriente).
![[Pasted image 20240523185844.png#center]]
Próximo a esto, se hace crecer dióxido de silicio, el cual será utilizado como aislante.
![[Pasted image 20240523190203.png#center]]
Se utiliza metal o polysilicio para construir un gate.
![[Pasted image 20240523190304.png#center]]
Los procesos de fabricación CMOS (Complementary MOS) permiten construir tanto un NMOS como un PMOS sobre un mismo sustrato tipo-p. Para los PMOS se utiliza una difusión de n-well para formar el Body.
![[Pasted image 20240523190422.png#center]]
Al ser el MOSFET un dispositivo de cuatro terminales, el Body necesita tener una tensión definida.

**Obs:** $V_{TH0}$ aparece cuando el body está conectado al source.

##### Tipos de MOS
- Enriquecimiento
- Vaciamiento, depleción o canal preformado

![[Pasted image 20240523191603.png#center|300]]
#### Funcionamiento en inversión
Al aplicarse una tensión $V_{GS}$ por encima de la tensión de umbral $V_{TH}$ se formará un canal por el cual los portadores van a poder moverse cuando se aplique una tensión entre drain y source.
![[Pasted image 20240523193014.png#center|300]]
**Obs:** $V_{TH}$ es la tensión umbral que tengo que superar para que se cree el canal.

- Si $V_{DS}<V_{GS}-V_{TH}$, se dice que el transistor opera en la zona de triodo o lineal. En esta zona, el MOSFET se comporta como una resistencia.
- Aumentar la tension 𝑉𝐷𝑆 hace que el canal se estreche del lado del drain. Para entender este fenómeno se puede observar el capacitor formado entre el gate y el canal. El valorde dicha capacidad está dada por: $Q_{c}(x)=- C_{ox}\cdot(V_{GS}-V_{TH}-V_{C}(x))$ , donde $V_{c}(x)$ es la tensión en el canal en la posición $x$. Al ser $V_{GS}$, $C_{ox}$ y $V_{TH}$ fijos, a medida que la tensión del canal aumenta la carga $Q_{c}$ disminuye. Esto resulta en una disminución de portadores libres y una reducción del canal en esa posición.
![[Pasted image 20240523193834.png#center|300]]
Cuando la tensión $V_{DS}=V_{GS}-V_{TH}$, se dice que el transistor está entrando en saturación. En este caso, se produce el pinchoff ($V_{Dsat}=V_{GS}-V_{TH}$) y el canal en el drain se hace cero.
![[Pasted image 20240523194921.png#center|300]]
**Obs:** En $x=L$ se tiene que $V_{c}(x=L)=V_{GS}-V_{TH}$, por lo tanto la carga en ese punto del canal se hace cero. Por lo que si no hay cargas → No hay canal.

Si sigo aumentando $V_{DS}$ despues de la saturación (pinchoff),la zona de pinchoff se mueve hacia el source, es decir, el canal se hace más corto. Si asumimos $\Delta L << L$, la corriente entre drain y source en saturación permanecerá constante por más que aumente la tensión entre dichos terminales.
![[Pasted image 20240523195627.png#center|300]]
#### Curva de salida
![[Pasted image 20240523195656.png#center|600]]
##### Zonas de operación
- Corte: $V_{GS}<V_{TH}$ → No hay canal → $i_{D}=0$.
- Zona triodo o lineal: $V_{GS}> V_{TH}$ y $V_{DS}\leq V_{Dsat}=V_{GS}-V_{TH}$. En ese punto la corriente está dada por: $i_{D}=\mu_{n}C_{ox}^{'} \frac{W}{L}\left((V_{GS}-V_{TH})V_{DS}- \frac{V_{DS}^{2}}{2}\right)$. Para valores chicos de $V_{DS}$ el término cuadrático se desprecia → $i_{D}=\mu_{n}C_{ox}^{'} \frac{W}{L}\left((V_{GS}-V_{TH})V_{DS}\right)$. Y la resistencia del canal está dada por: $R_{canal}= \frac{1}{\mu_{n}C_{ox}^{'} \frac{W}{L}(V_{GS}-V_{TH})}$
- Saturación: $V_{GS}>V_{TH}$ y $V_{DS}>V_{Dsat}$ donde la corriente estará dada por: $i_{Dsat}= \frac{1}{2}\mu_{n}C_{ox}^{'} \frac{W}{L}(V_{GS}-V_{TH})^{2}$
**Obs:** Para NMOS uso $V_{GS}$ y $V_{TH}>0$. Para PMOS uso (reemplazo en las ecuaciones) $V_{SG}$ en vez de $V_{GS}$, y de esta forma puedo seguir tomando $V_{TH}>0$.
#### Modulación del largo del canal
![[Pasted image 20240523202937.png#center|600]]
> **Obs:** Como me aparece una resistencia de salida, ésta deja de ser infinita, por lo que es un efecto negativo si yo quiere que me circule cierta corriente, como en el caso de una fuente de corriente.
> ![[Pasted image 20240523203802.png|300]]
#### Body effect
- El source y el body pueden estar conectados a tensiones diferentes ($V_{SB}\neq 0$). En este caso, se debe asegurar que la juntura se encuentra en inversa para no encender el diodo body-source.  
- Si $V_{SB}=0$, la tensión de thrshold está definida por $V_{TH}=V_{TH0}=2\phi_{F}+\gamma\sqrt{2\phi_{F}}$, donde $\gamma= \frac{t_{ox}}{\varepsilon_{ox}}\sqrt{2\varepsilon_{s}qN_{D}}$ para un sustrato tipo p.
- Si la tensión entre source y body están en inversa, la zona desierta debajo del gate aumentará y se requerirá mayor tensión en el gate para invertirla. Por esta razón la tensión de threshold se verá aumentada: $V_{TH}=V_{TH0}+\gamma (\sqrt{V_{SB}+2\phi_{F}}-\sqrt{2\phi_{F}})$.
#### Curvas MOSFET
![[Pasted image 20240523205216.png#center|500]]
#### Modelo pequeña señal
![[Pasted image 20240523205245.png#center]]
**Obs:** Trabaja en modo de saturación, por eso aparece la fuente de corriente, y una resistencia (por modulación del canal). Si solo tuviese una resistencia estaría en zona triodo.

**Obs:** El modelo sin capacitores lo utilizo para frecuencias bajas. Y si quiere hacer una analisis de respuesta en frecuencia utilizo el modelo con capacitores.
#### MOSFET en circuitos digitales
Los transistores MOS pueden ser utilizados para implementar compuertas lógicas.
![[Pasted image 20240523210848.png#center|500]]
##### Inversor
Utilizando un MOSFET canal n y otro canal p se puede construir un Inversor CMOS.
![[Pasted image 20240523212110.png#center|250]]
![[Pasted image 20240523212524.png#center|350]]
