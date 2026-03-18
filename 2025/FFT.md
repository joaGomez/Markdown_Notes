La transformada rápida de fourier (FFT) es un algoritmo que permite él cálculo eficiente de la transformada discreta de Fourier (DFT). Habíamos visto que la DFT de una secuencia de N muestras estaba dada por:
$$X(n)=\sum_{k=0}^{N-1}x(k)e^{-j \frac{2\pi}{N}nk}$$
Con el objeto de simplificar la notación podemos poner a la expresión previa como:
$$X(n)=\sum_{k=0}^{N-1}x(k)W_{N}^{nk} \qquad \qquad \text{donde } W_{N}= e^{-j \frac{2\pi}{N}}$$
El factor $W_{n}$ es conocido con el nombre de **twiddle factor** y tiene las siguientes propiedades:
$$\begin{split}
&\text{Periodicidad: } \qquad W_{N}^{nk}= W_{N}^{(n+N)k} \\
&\text{Simetría: } \qquad W_{N}^{nk} = - W_{N}^{(n+N}{2)k}
\end{split}$$
![[Pasted image 20250424112055.png#center]]

Las propiedades del factor $W_{N}$ se pueden aprovechar para reducir el número de cálculos en la DFT. Para poner en evidencia esto último comenzaremos por dividir la DFT de $N$ muestras en dos partes, de manera que una de ellas contenga las muestras pares mientras que la otra las impares.
$$X(n)=\sum_{m=0}^{N/2-1}x(2m)W_{N}^{(2m)n}+\sum_{m=0}^{N/2-1}x(2m+1)W_{N}^{(2m+1)n}$$
Como $W_{N}^{2mn} = \left(e^{- j\frac{2\pi}{N}}\right)^{2mn} = \left(e^{- j\frac{2\pi}{N/2}}\right)^{mn}=W_{N/2}^{mn}$, resulta que:
$$X(n)=\sum_{m=0}^{N/2-1}x(2m)W_{N/2}^{mn}+W_{N}^{mn}\sum_{m=0}^{N/2-1}x(2m+1)W_{N/2}^{mn}=Y(n)+W_{N}^{mn}Z(n) \qquad n=0,\dots,N-1$$

En la expresión previa esta implícita la periodicidad de $X(n)$, $Y(n)$ y $Z(n)$. Obsérvese que $Y(n)$ y $Z(n)$ son dos DFT de $N/2$ muestras cada una de manera que mientras $X(n)$ tiene período $N$, $Y(n)$ y $Z(n)$ tienen período $N/2$. Si bien en la expresión previa $X(n)$ puede ser evaluada en el rango $0$ a $N-1$, podemos reducir el número de operaciones si usamos las propiedades de periodicidad y simetría del factor $W_{N}$ y evaluamos $X(n)$ de la siguiente forma:
$$\begin{split}
& \text{Primera mitad del espectro: } \qquad 0\leq n\leq \frac{N}{2}-1 \\
& \text{Segunda mitad del espectro: } \qquad \frac{N}{2}\leq n\leq N-1
\end{split}$$
Para evaluar la segunda mitad hacemos:
$$X(n)|_{n=N/2,\dots,N-1}=X\left(\frac{n+N}{2}\right)\bigg{|}_{n=0,\dots,N/2-1}$$
Es decir que:
$$
X(n + N / 2) = Y(n + N / 2) + W_N^{(n + N / 2)} Z(n + N / 2)
$$
$$
X(n + N / 2) = Y(n) + W_N^{(n + N / 2)} Z(n) \quad \text{para } n = 0, \ldots, N/2 - 1
$$

Así el espectro total se calcula con las siguientes expresiones:

$$
X(n) = Y(n) + W_N^n Z(n)
$$
$$
X(n + N / 2) = Y(n) + W_N^{(n + N / 2)} Z(n)
$$
Evaluando ambas en el rango $\{ 0,N / 2 - 1 \}$ obtenemos el siguiente diagrama de flujo:

![[Pasted image 20250425105843.png#center|600]]

Haciendo uso de las propiedades de simetría la expresión de la segunda mitad del espectro queda:
$$X(n + N / 2) = Y(n)-W_{N}^{n}Z(n)$$
Por lo tanto las siguientes ecuaciones nos permiten calcular el espectro total:
$$\begin{split}
&X(n)=Y(n)+W_{N}^{n}Z(n) \\
X(n&+ N / 2) = Y(n) - W_{N}^{n}Z(n)
\end{split}$$
Podemos representar estas ecuaciones mediante un diagrama de flujo de señal:

![[Pasted image 20250425111032.png#center|300]]

Este diagrama de flujo se conoce con el nombre de *"ButterFly"* o *“Mariposa”* y representa el núcleo o *kernel* del algoritmo de la FFT.  

Podemos reconocer estos núcleos en el primer diagrama, donde podemos ver que el número de multiplicaciones por cada mariposa es 2 mientras que en el último diagrama es 1. Por lo tanto, si reemplazamos cada una de las mariposas, el número total de multiplicaciones será $N/2$.  

El proceso de división en muestras pares e impares puede ser repetido para cada una de las DFT de $N/2$ muestras hasta llegar a una DFT de 2 muestras o mariposa. El método consiste en dividir sucesivamente las muestras temporales (*Decimation in Time*) en dos grupos iguales y requiere que el número total de muestras sea potencia de dos, es decir:

$$
N = 2^\gamma \quad \text{donde} \quad \gamma \in \mathbb{N}
$$

El número total de veces que se realiza la división será:

$$
\gamma = \log_2 N
$$

Por lo tanto el número total de multiplicaciones será:

$$
N_{mult\_FFT} = \frac{N}{2} \cdot \gamma = \frac{N}{2} \log_2 N
$$
Mientras que para la DFT el número total de multiplicaciones era:
$$N_{mult\_DFT} = N^{2}$$
Por lo tanto, el ahorro en la cantidad de operaciones en ambos algoritmos estará dado por el cociente:
$$\frac{N_{mult\_FFT}}{N_{mult\_DFT}}= \frac{2N}{\log_{2}N}$$
#### Algoritmo

La primera descomposición de la DFT de $N$ muestras en dos DFT de $N/2$ muestras cada una, constituye la primera etapa del proceso.  
La segunda etapa consistirá en la descomposición de las dos DFT de $N/2$ muestras en cuatro de $N/4$ muestras cada una.  
Así continuamos hasta la etapa en que todas las DFT tengan 2 muestras, es decir una mariposa cada una. Las etapas se numeran de derecha a izquierda mediante el índice r (es decir $r = 1, 2, ..., γ$).

- El número total de etapas será: $γ$  
- El número total de DFT (o grupos de mariposas) por etapa será: $( 2^{(r-1)} )$  
- La distancia entre grupos consecutivos es: $( N / 2^{(r-1)} )$

Dado que cada grupo tiene la mitad de muestras que los de la etapa previa, los factores  $(W_N^n)$  aparecerán en la siguiente secuencia:

$$
W_N^n,\ W_{N/2}^n,\ W_{N/4}^n,\ W_{N/8}^n, \ldots
$$

**Donde**

$$
W_{N/2^{r-1}}^n = \left( e^{j\frac{\cdot 2\pi}{N / 2^{r-1}}} \right)^n = \left( e^{\frac{j2\pi}{N}} \right)^{n 2^{r-1}} = W_N^{n 2^{r-1}}
$$

A su vez cada vez que nos corremos $( N / 2^{r-1} )$ muestras (distancia entre dos grupos consecutivos) dentro de la etapa r el exponente del factor W se vuelve a repetir.

En efecto:

$$
W_{N}^{(n +  N / 2^{r-1}) 2^{r-1}} = W_N^{(n 2^{r-1} + N)} = W_N^{n 2^{r-1}} W_N^N = W_N^{n 2^{r-1}}
$$

Dicho de otra manera, al pasar de un grupo al siguiente dentro de una etapa dada, los exponentes del factor $W$ se repiten. Por lo tanto, sólo necesitamos evaluar los factores $W$ del primer grupo para  $( n = 0 \ldots N / 2^{r-1} - 1 )$ y repetir los restantes.

![[Pasted image 20250425114645.png#center|600]]

![[Pasted image 20250425114714.png#center|600]]

En la ultima etapa de la descomposición se observa que las entradas no están en orden secuencial si no en un orden aparentemente arbitrario. Se puede justificar con que cada vez que se efectúa la descomposición en dos DFT, se dividen las muestras en pares e impares de manera que tendremos una DFT de muestras pares y otras de impares. Para continuar con el proceso de descomposición debemos renumerar las muestras que pertenecen a cada DFT. Por ejemplo las muestras pares (0,2,4,6) ahora serán (0,1,2,3) mientras que las impares (1,3,5,7) serán (0,1,2,3).

El proceso de renumerar es equivalente a dividir los índices por 2. Al dividir por 2 se pierde la información de cuál era la muestra original.  

El árbol binario de la figura nos sirve para determinar cuál es el origen y el destino de las muestras (algo así como un árbol genealógico).

La interpretación del árbol es la siguiente:  
Se escribe el índice en binario (XXX), luego se ubican los índices pares (bit menos significativo en 0) en la rama superior, y los impares (bit menos significativo en 1) en la rama inferior, se renumeran y se repite el proceso.  

Con el objeto de no perder el origen de la muestra se van dejando anotados los bits menos significativos antes de renumerar.

Para conocer el destino de las muestras se usa el mismo árbol (que representa el proceso de descomposición) donde las últimas ramas estarán en orden secuencial comenzando por arriba.

Por ejemplo, la muestra original 001 (1) realizó el siguiente recorrido:  
[I P P] (I = impar rama inferior, P = Par rama superior)  
es decir que ahora ocupa la posición 100.

Como puede apreciarse, la **posición final de la muestra original se obtiene invirtiendo el orden de los dígitos binarios**. Este proceso es conocido como *“inversión de bits”* o *“bits reverse”*.

Formalmente:

Sea n ∈ ℕ y $( 0 ≤ n ≤ 2^γ )$, “$n$ tiene $γ$ dígitos” $( n = (b_{γ-1}, b_{γ-2}, \ldots, b_1, b_0) )$

Si expresamos $n$ en binario:

$$
n = \sum_{i=0}^{γ-1} b_i 2^i \quad \text{donde } b_i \in \{0, 1\}
$$

Entonces, la inversión de bits se define como:

$$
BR(n) = \sum_{i=0}^{γ-1} b_{\gamma - 1 - i} 2^i
$$

o también:

$$
BR(n) = (b_0, b_1, \ldots, b_{\gamma - 2}, b_{\gamma - 1})
$$
![[Pasted image 20250425120722.png#center|500]]
![[Pasted image 20250425120739.png#center|500]]

Cuando se realiza la FFT en tiempo real, las muestras de entrada provienen del muestreo de una señal analógica, e ingresan secuencialmente en la memoria del procesador de señales. Es por eso que conviene tener las muestras de entrada en orden secuencial y no invertidas (bit reversed). Una forma de lograr este objetivo es poner las entradas del diagrama de flujo de la figura 7 en orden secuencial, para lo cual debemos intercambiar todos los nodos de la entrada 4 con la 1 y de la 6 con la 3 manteniendo las relaciones existentes con los demás nodos del diagrama. El resultado de esta transformación se puede ver en la figura 8, en la cual se observa los siguientes cambios: 

1. Las salidas quedaron invertidas (bit reversed)
2. El numero de grupos por etapa se duplica cuando nos movemos desde la entrada a la salida. 

Dado que los cálculos comienzan en la entrada vamos a numerar las etapas de cálculo comenzando por la entrada, es decir que r se incrementa de izquierda a derecha. Los nodos de cada etapa del diagrama de flujo los seguiremos numerando igual que antes, es decir comenzando por la parte superior del diagrama.

Habíamos visto que los factores W se calculaban usando la expresión:

$$
W_N^{n \cdot 2^{r-1}}
$$

Dado que las relaciones entre los nodos del diagrama y la numeración de los mismos continúan siendo las mismas, el nuevo valor de $n$ será BR(n).

A su vez, como $r$ se numera de izquierda a derecha, se tiene que la nueva expresión de los factores $W$ será:

$$
W_N^{BR(n) \cdot 2^{(\gamma - r)}}
$$

Dado el nodo $n$ de la etapa $r$, el valor del exponente se calcula de la siguiente forma:

1. Se expresa $r$ en binario ($γ$ bits).  
2. Se invierten los bits del mismo (BR(n)).  
3. Se desplazan $\gamma - r$ bits hacia la izquierda completando con ceros por la derecha.

