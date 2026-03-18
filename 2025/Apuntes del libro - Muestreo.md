Esta sección está dedicada a la teoria útil del libro para apoyo de las clases.

### Cap. 1
Para procesar las señales digitales es necesaria una interfaz entre la señal analógica recibida y el procesamiento digital, o DSP. Para ello se encuentr el convertidor A/D. Cuando recibe una señal analógica, devuelve un output apropiada para que el DSP trabaje.

Además, si la señal que recibe el usuario debe ser analógica, se suma otra etapa con un convertidor D/A.

El diagrama de bloques es el siguiente:

![[Pasted image 20250326174436.png#center]]

Algunas razones por las cuales es más conveniente el procesamiento de la señal en digital son:
- Flexibilidad. Un programa siempre es más flexible a reconfiguraciones.
- Mayor control a la hora de establecer objetivos de precisión.
- Costos.
##### Función de un convertidor A/D
En pocas palabras, un convertidor A/D toma una señal analógica y devuelve un código binario que representa la información de la señal recibida. Para ello, copia la información de la señal, codifica y continua. Todos los convertidpres A/D ‘conectan los puntos’ mediante distintos métodos de interpolación. El método utilizado en la materia es ZOH (zero ordel hold) o S/H (sample and hold). La señal analógica puede reconstruirse a partir de las muestras recolectadas por este método.

Un problema que se debe evitar a la hora de realizar el muestreo es el ‘aliasing’ o ‘alias’. Este ocurre cuando la frecuencia de muestreo no es suficientemnete rápida para muestrear la señal, por lo que conduce a tomar menos muestras de las necesarias para reconstruir adecuadamente la señal.

El método de muestreo S/H:

![[Pasted image 20250326180249.png#center]]

#### Muestreo de señales analógicas
Si se utiliza un muestreo ideal, es decir, muestrear la señal con deltas cada un tiempo T (Periodo de muestreo), por lo tanto:
$$x(n) =x_{a}(nT) \qquad \qquad -\infty<n<\infty $$
A partir del periodo de muestreo se obtiene la frecuencia de muestreo tal que $f_{s}=\frac{1}{T}$, por lo tanto:
$$t=nT= \frac{n}{f_{s}}$$
##### Ejemplo de muestreo de una señal analógica
![[Pasted image 20250326192647.png#center]]

![[Pasted image 20250326192753.png#center]]

> Relación de las variables de frecuencia
> ![[Pasted image 20250326192951.png#center]]

#### Frecuencia de Nyquist
Para evitar alias, se debe utilizar una frecuencia de muestreo mayor que dos veces la frecuencia máxima de la señal:
$$F_{s} > 2\cdot F_{max}$$
![[Pasted image 20250326193537.png#center|200]]
#### Teorema de muestreo
Sea $B$ la frecuencia máxima de muestreo de una señal, esta señal se puede recuperar utilizando una frecuencia de muestreo de $2B$, utilizando una función de interpolación $g(t) = sinc(2\pi Bt) = \frac{sen(2\pi Bt)}{2\pi Bt}$.

Además, la señal que queremos muestrear puede expresarse tal que:
$$x_{a}(t) = \sum_{n=-\infty}^{\infty}x_{a}\left( \frac{n}{f_{s}} \right) g\left( t-\frac{n}{f_{s}} \right)$$
Tal que $x_{a}\left( \frac{n}{f_{s}} \right)=x_{a}(nT)\equiv x(n)$ son las muestras de la señal $x_{a}(t)$.

Si el muestreo se realiza a la fecuencia mínima para que no haya alias, la señal queda expresada tal que:
$$x_{a}(t) = \sum_{n=-\infty}^{\infty}x_{a}\left( \frac{n}{2B} \right) \frac{sen\left( 2\pi B\left( t-\frac{n}{2B} \right) \right)}{2\pi B\left( t-\frac{n}{2B} \right)}$$
### Cap. 6
#### Muestreo ideal y reconstrucción de señales continuas
Para procesar la señal debemos convertir la misma en una secuencia de números. Podemos lograr muestreando la señal cada T segundos. De esta forma pasamos de una señal continua, a una discreta → $x(n)=x_{a}(nT)$.

Si la señal $x_{a}(t)$ es una señal periódica de energía finita, su espctro está dado por:
$$X_{a}(f) = \int_{-\infty}^{\infty}x_{a}(t)e^{-j_{2}\pi ft} \, dt $$
A su vez, se puede recuperar la señal a partir de su espectro:
$$x_{a}(t)= \int_{-\infty}^{\infty} X_{a}(f)e^{j_{2}\pi ft} \, df $$
El espectro de una señal discreta $x(n)$, que la obtenemos a partir del muestreo de la señal original, está dado por la transfromada de Fourier discreta:
$$X(\omega) = \sum_{n=-\infty}^{\infty}x(n)e^{-j\omega n} \quad \text{o} X(f) = \sum_{n=-\infty}^{\infty}x(n)e^{-j2\pi fn}$$
La antitransformada en tiempo discreto:
$$x(n) = \frac{1}{2\pi}\int_{-\pi}^{\pi}X(\omega)e^{j\omega n} \, d\omega = \int_{-\frac{1}{2}}^{\frac{1}{2}}X(f)e^{j2\pi f n} \, df $$
Debido a que trabajamos con una señal muestreada periódicamente, la relación entre kas variables independientes $t$ y $n$ de las señales $x_{a}(t)$ y $x(n)$ es:
$$t=nT=\frac{n}{f_{s}}$$
Por lo tanto, al trabajar con las transformadas de Fourier hay que tener en cuenta ese cambio de variable:
$$x(n)\equiv x_{a}(nT)=\int_{-\infty}^{\infty}X_{a}(F)e^{j_{2}\pi n\frac{F}{f_{s}}}  \, dF \qquad \text{Antitransformada de la señal original} $$
Al compararla con la antitransformada discreta, se puede hallar la siguiente relación que aparece por la señal muestreada:
$$f=\frac{F}{f_{s}}$$
Donde $f$ es la frecuencia del espectro discreto de la señal $x(n)$, y $F$ es la frecuencia del espectro continuo de la señal original $x_{a}(t)$.

Dada la señal discreta $x(n)$ con espectro $X(f)$, sin alias, se puede reconstruir la señal original:
$$X_{a}(f)=\begin{cases}
\frac{1}{f_{s}}X(f) \qquad \mid f\mid \leq \frac{f_{s}}{2} \\ \\
0 \qquad \qquad ~ \quad |f| > \frac{f_{s}}{2} 
\end{cases}$$
Donde $X(f)=\sum_{-\infty}^{\infty}x(n)e^{-j_{2}\pi f(n/f_{s})}$ y la señal original antitransformandola por Fourier es $x_{a}(t)=\int_{-\frac{f_{s}}{2}}^{\frac{f_{s}}{2}}X_{a}(f)e^{j_{2}\pi ft}  \, df$.

Con estas expresionas queda tal que:
$$x_{a}(t)=\sum_{n=-\infty}^{\infty}x(n) sinc\left( \frac{\pi}{T} 
 (t-nT)\right)$$
![[Pasted image 20250328153518.png#center|400]]

![[Pasted image 20250328153630.png#center]]
**Obs:** Con interpolación ideal (Infinitas muestras), la señal reconstruida sería esta.

Cuando se produce alias debido a utilizar una frecuencia más baja de lo ideal, el resultado es el siguiente:
![[Pasted image 20250328153828.png#center|400]]
> Relaciones útiles entre funciones:
> ![[Pasted image 20250328153920.png|450]]


> **Observación:**
> Si la señal analógica está limitada con un ancho de banda $B\leq \frac{f_{s}}{2}$, no hay alias. Aún así, en la práctica se suele utilizar un filtro antialias previo al muestreo de la señal. Esto nos asegura que las componentes en frecuencia de la señal, con $f\geq B$ están lo suficientemente atenuadas, por lo que si hubiese alias, la distorsión es despreciable.
#### Procesamiento de señales continuas en tiempo discreto
![[Pasted image 20250331200526.png#center|500]]

![[Pasted image 20250331201013.png#center|400]]
$$x(n)=x_{a}(t)|_{t=nT}=x_{a}(nT) \qquad \text{Dominio del tiempo}$$
$$X(f)=\frac{1}{T}\sum_{k=-\infty}^{\infty}X_{a}(f-kf_{s}) \qquad \text{Dominio de la frecuencia}$$
Los convertidores A/D ideales son sistemas LTI que escalan eñ espectro analógico por un factor $f_{s}=\frac{1}{T}$, y crean una repetición periódica del espectro escalado, con un período de $f_{s}$.

En el dominio del tiempo, la entrada y la salida están relacionadas por:
$$y_{a}(t)=\sum_{n=-\infty}^{\infty}y(n)g_{a}(t-nT) \qquad \text{Dominio del tiempo}$$
Donde
$$g_{a}(t)=\frac{\sin\left( \frac{\pi t}{T} \right)}{\frac{\pi t}{T}} \overset{\mathcal{F}}{\longleftrightarrow} G_{a}(f)=\begin{cases}
T \quad |f|\leq \frac{f_{s}}{2}\\
0 \quad \text{Otro caso}
\end{cases}$$
es la función de interpolación del convertidor D/A ideal.

En el dominio de la frecuencia el resultado es el siguiente:
$$Y_{a}(f)=\sum_{n=-\infty}^{\infty}y(n)\int_{-\infty}^{\infty}g_{a}(t-nT)e^{-j_{2}\pi ft} \, dt = \sum_{n=-\infty}^{\infty}y(n)G_{a}(f)e^{-j_{2}\pi fnT} \longrightarrow Y_{a}(f)=G_{a}(f)Y(f)$$
#### Convertidores A/D
El convertidor A/D se encarga de convertir una señal analógica en una secuencia de bits que puedan ser procesados por un sistema digital. Para ello se deben muestrar una cantidad finita de valores de una señal que representen información significativa para un correcto muestreo de la señal.
![[Pasted image 20250331210018.png#center|500]]
Un circuito S/H es el que se encarga del muestreo analógico de la señal tomando muestras de valores y manteniendolas mientras procesa y cuantiza estos valores. Idealmente, no producen distorsión, y son muy precisos. Aún así, hay dos fenómenos que pueden ocurrir:
- Jitter: Distorciones en el dominio del tiempo, como errores en la periodicidad del proceso de muestreo.
- Droop: Variaciones no lineales en la duración de la apertura de muestreo y cambios en el valor de tensión mantenido durante la conversión.
#### Muestreo de pasabanda
Al muestrear con una señal pasabanda, con una frecuencia de muestreo $f_{s}$ produce una secuencia discreta $x(n)=x_{a}(nT)$ con un espectro:
$$X(f)=\frac{1}{T}\sum_{k=-\infty}^{\infty}X_{a}(f-kf_{s})$$
Debido a que la señal pasabanda tiene dos bandas espectrales, es más complicada de trabajar desplazandola en la frecuencia para evitar alias.

Primero se restringe una frecuencia máxima de la banda, tal que sea un múltiplo del ancho de banda: $f_{H}=mB$, y el entero $m=\frac{f_{H}}{B}$ se lo conoce como posición en la banda.

Como antes, se puede reconstruir la señal original utilizando la señal muestreada:
$$x_{a}(t)=\sum_{n=-\infty}^{\infty}x_{a}(nT)g_{a}(t-nT)$$
Con $g_{a}(t)=\frac{sen(\pi Bt)}{\pi Bt}\cos(2\pi f_{c}t)$

![[Pasted image 20250402121527.png#center|550]]

Tomando una señal pasabandas con sus dadas bandas espectrales. Para evitar alias, la frecuencia de muestreo debería ser tal, que las réplicas $k-1$ y $k$ de las banda espectral negativa, no se superpongan con la banda espectral positiva.

Esto será posible si existe un entero $k$ y una frecuencia de muestreo $f_{s}$ que cumplen las siguientes condiciones:
$$\begin{split}
2f_{H}\leq kf_{s} \\
(k-1)f_{s}\leq 2f_{L}
\end{split}$$
![[Pasted image 20250403093413.png#center|500]]
Utilizando las expresiones anteriores, se pueden combinar y obtenemos una condición para el valor de $k$:
$$\frac{2f_{H}}{k}\leq f_{s}\leq \frac{2f_{L}}{k-1} \to 
\begin{cases}

\frac{1}{f_{s}}\leq \frac{k}{2f_{H}} \\
(k-1)f_{s}\leq 2f_{H}-2B

\end{cases}
\to k_{max}\leq \frac{f_{H}}{B} \to k_{max}= \left\lfloor \frac{f_{H}}{B} \right\rfloor$$
La frecuencia de muestreo mínima para evitar alias será $f_{s_{max}}= \frac{2f_{H}}{k_{max}}$. Por lo que el rango aceptable de frecuencias de muestreo quedará determinado por $\frac{2f_{H}}{k}\leq f_{s}\leq \frac{2f_{L}}{k-1}$, y el rango de $k$ será $1\leq k \leq \left\lfloor \frac{f_{H}}{B} \right\rfloor$.

##### Elegir la frecuencia de muestreo adecuada
A partir de las condiciones para la frecuencia, se ha hecho un gráfico que representa las frecuencias posibles y las que no, de acuerdo con los demás parámetros.
![[Pasted image 20250403095126.png#center|550]]
La ecuación de diseño de este gráfico es la siguiente:
$$\frac{2}{k} \frac{f_{H}}{B}\leq \frac{f_{s}}{B} \leq \frac{2}{k-1} \left( \frac{f_{H}}{B}-1 \right)$$
Las áreas sombreadas del gráfico representan las frecuencias que producen alias. Las frecuencias de muestreo posibles que logran evitar alias son el espacio que queda en blanco. Por ejemplo, para $k=1$, se obtiene la relación: $2f_{H}\leq f_{s} \leq \infty$, que es el teorema de muestreo para señales pasabajos.

> **Observaciones:**
> Hay que tener en cuenta que si se utiliza una frecuencia de muestreo muy proxima a la zona sombreada (frecuencia que produce alias), una pequeña variación en la frecuencia de muestreo, o de la portadora de la señal, puede ocasionar que haya alias.
> Una solución posible es muestrear a una frecuencia mayor, que es equivalente a decir que la señal pasabanda tiene un ancho de banda mayor: $\Delta B = \Delta B_{L} + \Delta B_{H}$.
> $$\begin{split}f_{L}^{'} = f_{L}-\Delta B_{L} \\ f_{H}^{'} = f_{H}+\Delta B_{H} \\ B^{'} = B +\Delta B \end{split}$$
> Ahora la condición para la frecuencia de muestreo posible queda tal que:
> $$\frac{2f_{H}^{'}}{k^{'}}\leq f_{s}\leq \frac{2f_{L}^{'}}{k^{'}-1}$$
> Donde $k^{'} = \left\lfloor \frac{f_{H}^{'}}{B^{'}} \right\rfloor$.
> El rango de frecuencias de muestreo posibles se divide en un entorno alrededor del punto de trabajo calculado anteriormente:
> $$\Delta f_{s}= \frac{2f_{L}^{'}}{k{^{'}}-1}- \frac{2f_{H}^{'}}{k^{'}}=\Delta F_{sL}+\Delta f_{sH}$$
> A partir de las zonas sombreadas se obtiene:
> $$\begin{split}\Delta B_{L} &= \frac{k^{'}-1}{2}\Delta F_{sH} \\ \Delta B_{H} &= \frac{k^{'}}{2}\Delta F_{sL}	\end{split}$$
> Esto demuestra que la simetría de las bandas conduce a simetría en las tolerancias de la frecuencia de muestreo
> ![[Pasted image 20250403101917.png|400]]
> Si se elige el punto de trabajo en el medio de las zonas sombreadas, la frecuencia de muestreo será $f_{s} = \frac{1}{2} \left( \frac{2f_{H}^{'}}{k^{'}}+ \frac{2f_{L}^{'}}{k^{'}-1} \right)$. Por el punto elegido, $\Delta f_{sL}= \Delta f_{sH}= \frac{\Delta f_{s}}{2}$ → Las bandas de tolerancia se vuelven $\Delta B_{L} = \frac{k^{'}-1}{4}\Delta f_{s}$ y $\Delta B_{H} = \frac{k^{'}}{4}\Delta f_{s}$.