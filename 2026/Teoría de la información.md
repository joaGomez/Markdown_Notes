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

De esta forma, quedan $r-n_{1}$ símbolos para usar como prefijos del resto de los códigos, de modo que podremos asignar un máximo de $n_{2}=(r-n_{1})\cdot r$ códigos de longitud $2$, es decir: $n_{2}\leq r^{2}-n_{1}r$

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
A partir de esto, y otras condiciones, se deduce el primer teorema de Shannon:
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

En un código instantáneo compacto, se debe cumplir:
- Los símbolos de mayor probabilidad de ocurrencia tienen asignados códigos de menor longitud. *Si esto no se cumple, el código no será compacto.*
- Al menos los 2 símbolos de menor frecuencia poseen palabras de igual longitud.

Como ningún código es prefijo de otro, las 2 palabras de mayor longitud no pueden tener como prefijo a ninguna otra palabra de modo que puedo acortar la longitud del símbolo mas largo.

Si $L_{q-1}< L_{q}$, puedo eliminar el código excedente llevando $L_{q-1}=L_{q}$.

*El algoritmo de Huffman hace que los 2 símbolos de menor probabilidad de error tengan igual longitud diferenciándose sólo en el último elemento de código.*

El método es aplicable a códigos con alfabeto no binario. Si al aplicar el método no se obtiene una fuente de $r$ símbolos, implica que es necesario agrear símbolos falsos al iniciar el método.

Es posible  conseguir distintas codificaciones según las asignaciones hechas, aunque todas las posibilidades deberán tener igual longitud media. 

Esto lleva a casos donde la relación entre la longitud de las palabras más frecuentes y las menos frecuentes es distinta. Cuanto mayor sea su diferencia -> Mayor varianza. Al transmitir datos, esto no es algo práctico, ya que mandar distintos símbolos requiere de distinta cantidad de datos que se puedan transmitir, y se llega a la necesidad de utilizar un buffer de datos. Si la varianza es mínima, se optimiza la utilidad del buffer.

Los códigos de Huffman no solo son compactos, sino que también consiguen la longitud media mínima posible para ese alfabeto, donde:
$$
H_{r}(S) \leq L \leq H_{r}(S)+1 
$$
Y se cumple que
$$
1 \geq \eta \geq \frac{H_{r}(S)}{H_{r}(S)+1}
$$
**Observación:** A medida que extendemos la fuente, conseguimos mejor rendimiento.

![[Pasted image 20260327082547.png#center]]
#### Código de Shannon-Fano
Es un método de codificación estadística similar al de Huffman, en realidad es el primer método de codificación estadística desarrollado.

El procedimiento es el siguiente:
1. Se ordenan los símbolos de la fuente en probabilidades decrecientes.
2. Se divide en 2 grupos de probabilidades similares, y se asigna 0 o 1 a cada uno de esos grupos como primer símbolo.
3. Si los grupos tienen más de un símbolo, se repite el procedimiento.

```horizontal

![[Pasted image 20260327094248.png]]
---

![[Pasted image 20260327094018.png#center]]
```
#### Códigos aritméticos
Este es otro método que se basa en la estadística de la fuente. Se codifica la secuencia de símbolos de entrada en un valor numérico dentro del intervalo $[0.0,1.0)$.

![[Pasted image 20260327101613.png#center]]

La secuencia ABCAA se puede codificar con un valor numérico en el intervalo $[0.3475, 0.3515625)$ -> $[0.010110, 0.0101101 )$
Como los números son siempre menor a 1,puedo despreciar la información de la coma. Además, me conviene elegir el valor con menos bits. Asigno el código: $010110$

Para asignar el valor en el intervalo $[\alpha, \beta)$ obtenemos $t$ tal que $2^{ -t } \leq \beta-\alpha\leq 2^{-t+1}$. Luego, para obtener $x$, se debe cumplir que: $\alpha \leq \frac{x}{2^{t}}<\beta$

Si existen dos valores de $x$ en el intervalo, se toma el valor par, el código a utilizar será $r= \frac{x}{2^{t}}$

**Decodificación:**
![[Pasted image 20260327110207.png#center]]
#### Códigos de ventana y diccionario
La distinción de este código es agregar códigos a un diccionario a medida que aparecen nuevas cadenas en el texto sin comprimir.

**Algoritmo:**
1. Se definen 2 variables: Un carácter C, y un string P.
2. Al iniciar, el diccionario contiene todos los caracteres unitarios, y P está vacío.
3. Asigno el siguiente caracter del mensaje a codificar -> C.
4. Si el string P+C está presente en el diccionario, se hace P=P+C
5. Si el string P+C no está presente en el diccionario:
	- Doy como salida del algoritmo el código P.
	- Agrego el siguiente código para el elemento P+C, y hago P=C
6. Si hay más caracteres para codificar, vuelvo al paso 3.
7. Si no hay más caracteres, emito el código para P y finalizo.
```horizontal
![[Pasted image 20260327111117.png]]
---
![[Pasted image 20260327111132.png]]
```
**Algoritmo de decodificación:**
1. Definimos en adición a P y C el código previo CP y el código actual CA.
2. Al iniciar, el diccionario contiene todos los caracteres unitarios, CA es el primer código y se emite el string correspondiente al código CA (un solo caracter)
3. Se hace CP = CA y se toma el nuevo caracter del mensaje codificado como CA
4. Si el código CA está presente en el diccionario ( Es lo normal ):
	- Se emite la palabra correspondiente a CA como mensaje decodificado
	- Se hace P: la palabra decodificada de CP, C: primer carácter de CA y se agrega P+C al diccionario. 
	- Si hay más palabras para decodificar se repite desde el paso 3.
5. Si el código CA no está en el diccionario (Condición anómala)
	- P: palabra decodificada de CP, C : primer carácter de CP.
	- Se emite P +C como código de salida, se agrega al diccionario y pasa a ser CA.
	- Si hay más palabras para decodificar se repite desde el paso 3.

![[Pasted image 20260327111634.png#center]]
#### Códigos RLE (Run Length Encoding)
Codifica una secuencia de caracteres iguales por su la cantidad de repeticiones y el valor del carácter repetido.

Supongamos la secuencia a codificar ABCCCCCCDDDDDEABBBBC. Podría reemplazarse por AB6C5DEA4BC. De este modo, la secuencia de 20 caracteres se reemplaza por una de 14. 

En este esquema, sólo es conveniente una compresión ante repeticiones de 4 o más caracteres, si hay que codificar el carácter de control, se repite esto es una expansión. Es sencillo de implementar, requiere poca potencia de cálculo. Es particularmente útil en dibujos (Planos) e imágenes con grandes plenos. Se utiliza en los formatos TIFF , PCX y BMP.
#### BWT
Creada por Michael Burrows y David Wheeler. Transforma un string en otro y es reversible.

-> Toma un string de largo N.
-> Obtiene rotandolo en forma cíclica N strings.
-> Los ordena alfabéticamente.
-> Obtiene la última columna y el índice de la fila que contiene el string original.

```horizontal
![[Pasted image 20260327115749.png]]
---
![[Pasted image 20260327115804.png]]
```
#### MTF
Para aprovechar las repeticiones de caracteres se utiliza en lugar de RLE un método utilizado el "Move To Front" o MTF. En este, se parte de los carcateres ordenados (0 a 255). Para cada caracter se envía su posición en la lista, y luego se pasa al primer lugar de la lista desplazando al resto en una posición.

![[Pasted image 20260327120114.png#center]]

Las secuencias de caracteres repetidos se cnvierten en la posición de un caracter y luego secuencias de '0'. Se obtienen como resultado un gran número de valores pequeños, y pocos grandes. Una codificación estadística (Huffman) resulta eficiente y este el tercer paso utilizado.
### Compresión con pérdidas
Existen métodos de compresión con pérdida, en este caso el límite de Shannon no es aplicable, es decir que puede codificarse con un tamaño menor a la entropía.

Realmente el límite de Shannon sigue siendo aplicable, pero en el proceso de compresión se pierde parte de la información del mensaje por lo tanto la entropia del mensaje codificado es menor que la del original.

Se puede utilizar si el receptor considera aceptable la pérdida, como en imágenes.
#### Compresión JPEG
Las componentes de color se procesan en módulos de 8x8 pixels. Al aplicar la transformada discreta coseno se obtienen 64 coeficientes que
representan la composición “Espectral” de la imagen. Se usa DCT en lugar de DFT por su buen comportamiento en los límites al eliminar componentes de alta frecuencia.

En general los componentes de alta frecuencia son chicos. Se ponderan los coeficientes para disminuir la importancia de los coeficientes de alta frecuencia. Esta cuantificación y el redondeo de coeficientes es responsable de la perdida de información.

El resultado es un pequeño grupo de coeficientes no nulos que se ordenan de 1 a 64 y se codifican mediante una combinacion de RLE y Huffman.
#### Compresión MP3
Este modelo de compresión divide en bandas mediante DCT. Aplica un modelo psicoacústico a fin de codificar con menor precisión aquellos componentes que se ven enmascarados. 

-> Frente a 2 sonidos de frecuencias similares solo se
percibe la de mayor volumen.
-> El efecto estéreo se pierde en bajas frecuencias, se puede almacenar en mono.
->Se evalúa el monto de ruido admisible.
-> Se codifica por Huffman.

![[Pasted image 20260327114754.png#center]]
