### Elementos
Se pueden considerar 3 elementos para transmitir información:
$$
\text{FUENTE  →   CANAL → RECEPTOR} 
$$
#### Modelo de Shannon-Weaver
![[Pasted image 20260318132348.png#center|566]]

**Definición:** La información que nos da el conocer la ocurrencia de un evento está asociada a la posibilidad que tiene dicho evento de ocurrir.
### Características de la información
Al conocer la ocurrencia del evento $X_{1}$ entrega la información $I_{1}$, y conocer la ocurrencia de otro evento independiente $X_{2}$ entrega la información $I_{2}$. Si conozco que han sucedido ambos eventos, la información obtenida será:
$$
I_{3}=I_{1}+I_{2}
$$
La información es aditiva.

Shannon propone la siguiente forma para relacionar la probabilidad de ocurrencia de un evento, con la información que este brinda.
$$
Ii = \log_{a} \left( \frac{1}{p_{i}} \right)
$$
Cuanto menos probable es un evento → Mayor cantidad de información brinda.

Además, $a$ tomará distintos valores dependiendo de la medida de información utilizada:
$$
\begin{align}
a=10 \quad &\text{Hartleys} \\
a=e \quad &\text{Nats} \\
a=2 \quad &\text{Bits} 
\end{align}
$$
Estas unidades presentan las siguientes relaciones:
$$
1 \text{ Nat} = 1.44 \text{ Bits} \quad \wedge \quad 1 \text{ Hartley} = 3.32 \text{ Bits}
$$
### Fuentes de información de memoria nula
Son un modelo matemático que trata de definir en forma sencilla un elemento que emite información:

La información de cada símbolo emitido por la fuente es:
$$
I_{i} = \log_{a}\left( \frac{1}{p_{i}} \right)
$$
Se define la **entropía** de la fuente como la información promedio por símbolo para el total de la fuente:
$$
H(S)=\sum_{i=1}^{q}p_{i}\cdot I_{i}=\sum_{i=1}^{q}p_{i}\cdot \log_{a}\left( \frac{1}{p_{i}} \right)
$$
La entropía representa la información promedio que cabe esperar del próximo símbolo de la fuente, el cuál aún no ha sido emitido.

**Observación:** A partir de las desigualdades $\log(x)\leq x-1$, y $\log\left( \frac{1}{x} \right) \geq 1-x$, se puede demostrar que:
$$
H(S)\leq \log(q)
$$
Siendo $q$ la cantidad de eventos.
#### Extensiones de fuentes sin memoria
Como se puede intuir por el nombre, consiste en considerar los símbolos a la salida de la fuente agrupados de a ‘$n$’.

Cada símbolo $\sigma_{i}$ de la fuente extendida representa un conjunto de $S_{i_{1}},\, S_{i_{2}}, \, \dots, \, S_{in}$ de la fuente original.

La probabilidad de cada símbolo $\sigma_{i}$ será el producto delos símbolos que le dan origen:
$$
p(\sigma_{i}) = p_{i_{1}}\cdot p_{i_{2}}\cdot\, \dots\,\cdot p_{in}
$$
La entropía de la fuente extendida está dada por:
$$
H(S^{n}) = n\cdot H(S)
$$
Además, la fuente extendida posee $Q=q^{n}$ símbolos.
### Fuentes con memoria (de Markov)
Se define un modelo matemático donde los $q$ símbolos de la fuente se emiten cada uno cona probabilidad que depende de los ‘$m$’ símbolos anteriores. Se la representa como $S_{m}$.

La fuente se definirá por sus $q$ símbolos, y por sus $q^{m+1}$ probabilidades condicionales de ocurrencia.

La probabilidad de oucrrencia del símbolo $S_{i}$ será:
$$
p(S_{i}) = p(S_{i}|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm})
$$
La información que brinda $S_{i}$, si previamente ocurrieron $S_{j_{1}}, S_{j_{2}},\, \dots\, , S_{jm}$ será:
$$
I(S_{i}|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm}) = \log_{a}\left( \frac{1}{p(S_{i})} \right) = \log_{a}\left( \frac{1}{p(S_{i}|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm})} \right)
$$
La entropía de la fuente, si han ocurrido los $'m'$ eventos anteriores será:
$$
H(S|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm}) = \sum_{i=1}^{q} p(S_{i}|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm})\cdot I(S_{i}|S_{j_{1}},S_{j_{2}}, \, \dots \, , S_{jm})
$$
#### Extensiones de una fuente con memoria
De manera similar al caso de una fuente sin memoria, se pueden definir extensiones de una fuente con memoria al considerar grupos de ‘$n$’ símbolos a la salida de la fuente como los símbolos de la fuente extendida $S_{m}^{n}$.

En la fuente original, la probabilidad de ocurrencia de cada nuevo símbolo depende de los $m$ anteriores → En la fuente extendida cada nuevo símbolo dependerá de los $\mu$ anteriores, donde $\mu = \lceil \frac{m}{n} \rceil$.
### Fuentes afín a una fuente con memoria
Una fuente afín es una fuente sin memoria, que tiene los mismos símbolos que la fuente que le da origen, y que tiene como probabilidades para estos símbolos las probabilidades incondicionales de primer orden de la fuente a la cual es la afín.

Dada la fuente $S$ su afín se denomina como $\bar{S}$.

**Observación:** Si la fuente origen no posee memoria → La fuente afín es igual a la fuente original.

**Propiedades**
$$
\begin{align}
&H(\overline{S_{m}}) \geq H(S_{m})  \\
&H(\overline{S_{m}^{n}}) - H(S_{m}^{n}) = \text{cte} \qquad \forall n\geq m
\end{align}
$$
### Codificación
Dada una fuente con símbolos $S_{1}$ a $S_{q}$, y un alfabeto código de $r$ símbolos $X_{1}$ a $X_{r}$, la fuente será codificada a partir de asignarle para cada símbolo de esta una palabra.

**Por ej:**
$$\begin{align}
&\text{Sean los símbolos 0 y 1 correspondientes al alfabeto código, se asignan combinaciones }  \\
&\text{para todos los símbolos de la fuente:} \\
&\begin{cases}
S_{1} \to 00 \\
S_{2} \to 01 \\
S_{3} \to 10 \\
S_{4} \to 11 
\end{cases} \qquad  
\begin{split}
&\text{Si las palabras no se repiten para distintos símbolos de la fuente → No singular} \\
&\text{Si las se repiten para distintos símbolos de la fuente → Singular}
\end{split} \\
&\text{Se denomina unívoco si existe una única forma de de decodificar una secuencia}
\end{align}
$$
**Observación:** Los códigos no singulares de palabras de igual longitud, son siempre unívocos.

Se denominan códigos instantáneos cuando es posible decodificar una palabra sin tener que esperar a la siguiente. Es decir, no necesito toda la secuencia de palabras, puedo ir recibiendo los símbolos codificados y resolver la misma secuencia de palabras. Para lograr esto, ninguna palabra debe ser prefijo de otra.
#### Inecuación de Kraft
Si se quiere obtener códigos instantáneos para una fuente de $q$ símbolos con un alfabeto de $r$ símbolos código, podremos asignar $n_{1}$ símbolos de longitud $1$ con $n_{1}\leq r$.

De esta forma, quedan $r-n_{1}$ símbolos para usar como prefijos del resto de los códigos, de moso que podremos asignar un máximo de $n_{2}=(r-n_{1})\cdot r$ códigos de longitud $2$, es decir: $n_{2}\leq r^{2}-n_{1}r$

Si generalizamos la inecuación de Kraft:
$$
\sum_{i=1}^{q} r^{-l_{i}} \leq 1
$$
Se cumple para una fuente de $q$ símbolos a codificar con un alfabeto de $r$ símbolos, donde $l_{i}$ es la longitud de la la palabra i-ésima.

La inecuación de Kraft es **condición necesaria** para que un código sea instantáneo. Además, es **condición suficiente** para que exista un código instantáneo con esas longitudes de palabra, pero **no** es **condición suficiente** para determinar que un código sea instantáneo.
$$
\text{Longitud media:} \quad L = \sum_{i=1}^{q} p_{i}\cdot l_{i}
$$
Dada una fuente de $q$ símbolos, existen distintas codificaciones que se pueden realizar con un alfabeto de $r$ símbolos. No todos tendrán la misma longitud media. Aquel de menos longitud media se denomina **código compacto**.

Además, siempre se cumple que:
$$
H(S)\leq \log(r\cdot L) \to H_{r}(S)\leq L
$$
A partir de esto, y otras condciones, se deduce el primer teorema de Shannon:
$$
H_{r}(S)\leq L \leq 1+H_{r}(S)
$$
Para una fuente extendida será:
$$
H_{r}(S^{n})\leq L_{n} \leq 1+H_{r}(S^{n})
$$
Donde vale que
$$
\lim_{ n \to \infty } \frac{L_{n}}{n} = H_{r}(S)
$$
#### Rendimiento de un código
Para transmitir información podemos utilizar más o menos código, en la medida en que utilicemos códigos más largos, es necesario más tiempo de comunicación, mayor tamaño de archivo, etc. Se denomina rendimiento a la relación entre la cantidad de información transmitida y la cantidad de código utilizada para realizar la transmisión. 
$$
\eta = \frac{H_{r}(S)}{L}
$$
#### Códigos de Huffman
Es un método que permite generar un código compacto para una fuente y un alfabeto dado. Genera códigos de longitud de palabra no constante. Se basa en asignar palabras largas a los símbolos de menor probabilidad de ocurrencia.

Los pasos para construirlo son:
1. Ordenar los símbolos en orden descendientes de probabilidad.
2. Agrupar los últimos $r$ símbolos en un símbolo consolidado.
3. Repetir los pasos 1 y 2 hasta lograr reducir la fuente a $r$ símbolos.
4. Asignar a cada símbolo uno de los $r$ símbolos código del alfabeto código.
5. Desagregar cada símbolo en los $r$ componentes y asignar a cada uno de estos un símbolo de los $r$ del alfabeto código de forma de incrementar un elemento a la palabra código.
6. Repetir el punto 5 hasta llegar a generar palabras códigos para todos los símbolos de la fuente.

**Observación:** Es posible que debido a distintas asignaciones u ordenamientos se obtengan distintos códigos: *Todos deben tener igual longitud media*.

