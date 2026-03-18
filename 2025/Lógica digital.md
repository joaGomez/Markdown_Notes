### Comparador
![[Pasted image 20250309111415.png#center]]
### Multiplicador
Es un switches: Depende el valor de los bits de control. Hace que se conecte alguna entrada a la salida.
![[Pasted image 20250309111829.png#center]]
### LUT (Look up table)
![[Pasted image 20250309112212.png#center]]
> Repaso:
> **Complemento A1:** Se hace el complemento de cada bir individualmente → $0001 = 1$ → Su complemento A1 será $\overline{0001} = 1110 = -1$.
> **Complemento A2:** Se hace el complemento apartir de sumar un bit al último bit del complemento A1 del número → $0001 = 1$ → Su complemento A2 será $\overline{0001} + 1 = 1111 = -1$.

### Sumador
#### No signado
Se necesita un bit más para obtener un buen resultado en todos los posibles casos. Este bit lo brinda el carry out.
![[Pasted image 20250315163611.png#center]]
#### Signado
En este caso, a pesar de contar con un bit más por el carry out, no siempre el output es correcto:
![[Pasted image 20250315163719.png#center]]
El problema radica en que se obtiene un signo cuando debía dar el otro. Por lo tanto, se puede intentar detectar cuando la suma no es válida.

- Overflow: Cuando quería + pero obtuve -.
- Underflow: Cuando quería - pero obtuve +.
![[Pasted image 20250315164332.png#center]]
Donde $A[N-1]$ es el bit más significativo de la variable A.

Una posible solución es agregar un bit a la entrada replicando el bit más significativo.
$$b_{n~bits}=b_{n-1}b_{n-2}\dots b_{0} \to b_{n+1 ~~ bits}=b_{n-1}b_{n-1}b_{n-2}\dots b_{0}$$
![[Pasted image 20250315173645.png#center|400]]
**Obs:**
- No uso carry in ni carry out
- En no signado, el bit más significativo no es el signo, sino que agrego un cero.
### Multiplexor
![[Pasted image 20250315175504.png#center|400]]
### Decoder y encoder
![[Pasted image 20250318175000.png#center]]
### Compatibilidad
#### Niveles de tensión
Para cada integrado, existe un valor para $V_{min}$, $V_{L}$, $V_{H}$, $V_{max}$. Al concatenar con otro integrado, hay que ser precavidos y que los niveles de tensión se encuentren dentro de los niveles de tensión de la entrada.
![[Pasted image 20250318175542.png]]**Obs:** $V_{min}$ puede ser menos que cero. Para que ande correctamente $V_{omax}$ y $V_{oh}$ debe estar comprendido entre $V_{max}$ y $V_{ih}$, lo mismo con el low.

**Definición:** El fanout es la capacidad de mi circuito a la salida del integrado → Afecta la respuesta en frecuencia.
### Tiempo de conmutación en combinacionales
Aún con conmutación ideal existe un $t_{p}>0$. A peor conmutación de la compuerta → Mayor $t_{p}$ → Limitación con respecto a la frecuencia.
![[Pasted image 20250318185158.png#center|300]]
Debido a esta condición, existe lo que se denomina *riesgo estático* → El circuito cambia cuando no debería cambiar. 

Se denomina *riesgo dinámico* cuando el circuito cambia más veces de las que debería. Debido a esto, los resultados combinacionales obtenidos pueden variar hasta establecerse en el resultado final.
![[Pasted image 20250318194832.png#center]]
**Observaciones:**
- Estos cambios se producen por el tiempo de transición de las operaciones.
- El peor camino no es el de mayor compuertas, sino el de mayor tiempo.
- Cuento todos los caminos posibles de cada entrada y veo el tiempo que tarda cada uno.

→ Una forma de solucionarlo es compensando todos los caminos. Pero no es muy eficiente, y vulnerable a cambios de entorno, temperatura, etc. 
→ Para reducir riesgos se pueden utilizar grupos que cubran las transiciones del mapa de karganugh pero es imposible cubrir cada caso y no siempre funciona para todas las condiciones.
→ La mejor solución es discretizar el tiempo, realizar las lecturas en los tiempos efectivos y almacenar ese dato.
#### LATCH
![[Pasted image 20250318195326.png#center]]
R: Resetear, S: Setear, R=S=0 → Q=$Q_{prev}$. Con dos ceros en las entradas dependo del estado anterior.

|  S  |  R  |     Q      |       $\bar{Q}$       |
| :-: | :-: | :--------: | :-------------------: |
|  0  |  0  | $Q_{prev}$ | $\overline{Q_{prev}}$ |
|  0  |  1  |     0      |           1           |
|  1  |  0  |     1      |           0           |
|  1  |  1  |     0      |           1           |
![[Pasted image 20250318200509.png#center]]

![[Pasted image 20250318200529.png#center|450]]

Para mejorar los problemas de replicación por transiciones:
![[Pasted image 20250319095748.png#center|350]]
**Obs:** Con esta implementación el dato es estable.
#### Frecuencia máxima
- Tiempo de setup: Tiempo que debe estar el dato D estable antes del flanco.
- Tiempo de hold: Tiempo en el que tengo que mantener D estable después del flanco.

**Obs:** Cuando ocurre alguna de estas dos ocasiona *metaestabilidad* → No se en que estado va a estar D.

Para que no haya metaestabilidad, se debe cumplir la siguiente condición:
$$T_{D \to Q}\mid_{clk} + T_{comb} + T_{setup} < T_{clk}$$
A veces, en un circuito necesitamos cierta frecuencia de trabajo. Hay casos, donde esta no se puede reducir, y el tiempo combinacional está fijo, ya que no siempre se busca cambiar la cantidad de compuertas lógicas. Cuando ocurre esto y el tiempo combinacional es el culpable de no hacerte alcanzar la frecuencia buscada, una técnica útil para resolver este problema es agregar flip flops entre medio. De este modo, donde se ubican los flip flops, se corta el tiempo combinacional de ese camino.

La contraparte de esta técnica, es que al agregar flip flops añadimos tiempo de latencia, lo cual puede llegar a ser un problema en nuestra aplicación.
#### Máquinas de estado
##### FSM de Moore
![[Pasted image 20250402114228.png#center|400]]
##### FSM de Mealy
![[Pasted image 20250402114257.png#center|400]]
> Ejemplo de uso de ambas para un problema de encender 4 leds en orden ascendente o descendente dependiendo de si se presiona un botón o no:
> ![[Pasted image 20250402114443.png|800]]


