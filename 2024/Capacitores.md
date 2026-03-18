La capacitancia se define como: $C=\varepsilon_{0} \cdot \varepsilon_{r} \cdot \frac{A}{d}=k\cdot \frac{A}{d}$, y su corriente será tal que: $i_{c}= C \cdot \frac{dV}{dt}$

Se pueden clasificar según:
- El dieléctrico: Cerámicos - Film - Electrónicos (óxido de aluminio-tantalio) - Aceite - Doble capa
- Fijos/Variables
- Polarizados/No polarizados

**Constante dieléctrica:** Es la relación de la capacidad de un capacitor con un dado dieléctrico y la capacidad del mismo capacitor con vacío como dieléctrico.

**Rigidez dieléctrica:** Un dieléctrico sometido a un campo eléctrico (E) creciente, cambia abruptamente sus características de aislador a semiconductor. (alcanza la tensión disruptiva o el valor de la rigidez dieléctrica). Es la capacidad de tolerar una diferencia de potencial sin perforar el aislante.
### Modelo de capacitancia real

![[Pasted image 20240405105259.png#center|400]]
Tengo en cuenta que el capacitor tiene placas que tienen propiedades resistivas. Tienen terminales con propiedades resistivas e inductivas. Además, tengo en cuenta que pueden saltar electrones al otro lado → Modelizo una resistencia en paralelo.

### Respuesta en frecuencia para distintas capacitancias

![[Pasted image 20240405105606.png#center|300]]
### Capacitores cerámicos
Hay tres tipos:
1. Multicapa/Monolíticos: Tienen múltiples capas enfrentadas. ESL (Parte inductiva de la impedancia) baja. Van desde $x~pF \to xxx~\mu F$. Estos tienen SMT, SMD (Solo pueden estar hechos con este tipo de capacitores). x (ancho) e y(profundidad) → xxyy decenas de milis: 0805 → 80 * 50 mils (Medida estandar).
 Si tengo un capacitor de 103 → Equivale a $10* 10^{3}~pF → 10~nF$.

![[Pasted image 20240405111943.png#center|200]]


2. Disco: Dos placas enfrentadas con dieléctrico en forma de disco. Baja ESL (Terminales). Baja capacitancia. Van desde $1pF \to x~nF$. $\frac{\Delta C}{\Delta Temp}$. Capacitores NPO (Negro/Blanco/Punto O) tiene $\frac{\Delta C}{\Delta Temp}=0$.

![[Pasted image 20240405110915.png#center|200]]


3. Mica: Dos placas rectangulares enfrentadas. Dieléctrico Mica. Van desde $1pF\to x~nF$.
$47~p = 47~pF$, pero si tengo $4p7$ equivale a $4.7 ~ pF$. La $p$ me delimita la coma.

![[Pasted image 20240405110936.png#center|200]]
### Nomenclatura
$XX * 10^{Y}$ (tecnología)
$XX$ (letra)


> **Observaciones**
> 3.9 → Disco → $pF, nF$.
> .1 → Cerámico multicapa → 1 $\mu F$.

### Capacitores electrolíticos
##### Aluminio
###### Circuito equivalente
![[Pasted image 20240409112112.png#center|300]]
$R_{1}$ es la resistencia del aluminio. $R_{2}$ es la resistencia del electrolito y $R_{3}$ son los electrones que se pierden por el óxido. $L$ aparece porque al enroscar el aluminio actúa como bobina. El $C_{2}$ es muy chica y despreciable, pero aparece por la segunda placa de aluminio. El diodo del circuito equivalente representa el efecto polarizado del capacitor. Si se conecta en inversa (ánodo -, cátodo +) el electrolito destruye al dieléctrico (reducción), generando gases que pueden llevar a hacer explotar al capacitor.

El circuito equivalente fianl sería tal que: $ESR + C +ESL$ (en serie). $ESR$ no es solo la suma de las resistencias, sino que tiene $\omega$ → Varía un poco con la frecuencia.

Primero le realizamos **etching** al aluminio, lo desbastamos → Aumenta el área efectiva. Luego lo oxidamos en ácido clorhídrico por ejemplo. Posterior a eso, se coloca un líquido conductor (electrolito) para que sea uniforme. Encima de eso, se coloca un papel que actúa como esponja y evite que se derrame el líquido. Se tapa con otra capa de aluminio (sin etching). Finalmente, se enrolla y tenemos un capacitor electrolítico, que como logramos disminuir la $d$ por el óxido y logramos aumentar $A$ → Aumentamos significativamente la capacitancia.

Electrolitos:
1. Con agua: $T_{max}=85°C$
2. Con amidas: $T_{max}=105°C$

![[Pasted image 20240409113409.png#center|200]]
El cátodo es donde se genera capacitancia desde el negativo (electrolito).

Los capacitores electrolíticos son polarizados, pero solo puedo usar una polaridad.

El objetivo es conectar un cap electrolítico con un cap cerámico multicapa en paralelo → La pendiente de la respuesta en frecuencia no es tan pronunciada → Sigue teniendo un efecto capacitivo a altas frecuencias.

Ultracaps → Con un efecto double layer, son polimeros polarizados, que por la pequeña distancia entre estas moléculas, no va a resistir grandes tensiones (High voltage $3,3V$) pero va a tener una capacitancia enorme.

Capacitores LW son capacitores multicapa más anchos que soportan menos tensión, pero tienen menos resistencia e inductancia → Funciona mejor hasta más frecuencia que otro capacitor no LW. Estos capacitores son del tipo SMD.

**Obs:** Cuando en una curva característica, la curva del capacitor en función de la frecuencia se transforma en una recta → El capacitor pierde el efecto capacitivo y actúa como una resistencia.
#### Electrolíticos (Tántalo o tantalio(Para los OG))
El tántalo tiene muy poco peso pero gran superficie. Para la fabricación de un capacitor de estos, se hace el mismo proceso de oxidación, los cubro con electrolito y en vez de cubrirlos con un aluminio, los cubro con un tántalo. En este caso el electrolito es el cátodo (-), y el tantalio es el ánodo (+). Al tantalio que cubre por fuera, se le hace una capa de plata para que el electrolito no lo oxide.

La capacitancia del capacitor de tantalio es mayor que la del aluminio, ya que la distancia del óxido de tantalio es mucho menor y mejor dieléctrico, y además, el área es mucho mayor porque hay mayor superficie de contacto entre el óxido y el dieléctrico. Además estos capacitores tienen baja ESL.

**Obs:** Si bien es tentador decir que podemos lograr capacitores con más capacitancias, pero lo importante es que con los de tantalio podemos hacerlos más chicos y con la misma capacidad, siendo mucho mejores, aunque son más costosos.

**Obs:** A partir de $100kHz$ voy a usar un cap de tantalio, más dos caps multicapa en paralelo. Pero a baja frecuencia es preferible usar los de aluminio.

**Obs:** Si un capacitor electrolítico no dice nada, su tolerancia es Z.

**Obs:** Si pongo $.0047$ → Son $0.0047 \mu F$
#### Capacitores de Film
$XnF$ → $XX\mu F$

Hay dos tipos:
- Laminados: Se enrollan dos tiras de aluminio con aislantte entre ellas (polímero), una vez enrollo todo lo que necesito lo corto y ya tengo mi capacitor de film. Mucho aluminio → Baja resistencias. Pero al enroscarlo le aumento la indictancia → A veces en vez de enrollarse se apilan o se hacen en zigzag.
      Cuando hay un cortocircuito no funciona más.

- Metalizados: Se metaliza el polimero. Más chico, más liviano → Por la misma capacidad es más barato. Pero tengo más resistencia porque tengo poco metal. Si tengo un cortocircuito → Se evapora el metal (efecto inverso a cuando lo creo) → Pierdo un mínimo de capacidad y sigue funcionando (auto healing).
