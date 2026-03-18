**Parámetros**
Media muestral: '$\bar{x}=\frac{1}{n}\sum\limits_{j=1}^{n}{x_{j}}$'. Es el promedio de los datos.
Mediana: '$m$'. En un ordenamiento de menor a mayor es el término central, a diferencia de la media no es sensible a los valores alejados de la media.

Cuartiles primero y tercero: '$q_{1}, q_{3}$'. En un ordenamiento de menor a mayor son mediana de la primera mitad y de las segunda mitad de los datos.

Rango muestral: '$R=\ MÁX-\ MÍN$'. Distancia entre el mínimo y el máximo de los datos muestrales.

Rango intercuartil: '$IQR= \ q_{3} - \ q_1$' .La distancia entre los cuartiles primero y tercero.

Desvío estándar muestral: '$s=\sqrt{\frac{1}{n-1} \sum\limits_{j=1}^{n}{[x_{j}-\bar{x}]^{2}}}$' .Medida típica de variación de estos datos, es nula si y sólo si todos los datos son iguales y es tanto mayor cuanto más dispersos están los datos.

Coeficiente de simetría: '$\gamma = \frac{1}{ns^{3}} \sum\limits_{j=1}^{n}{[x_{j}-\bar{x}]^{3}}$' .Medida típica de simetría de los datos respecto de la media. Es nulo si hay simetría. Si es positivo se dice que los datos tienen sesgo positivo y negativo en caso contrario.

Coeficiente de curtosis: '$k= \frac{1}{ns^{4}}\sum\limits_{j=1}^{n}[x_{j}-\bar{x}]^{4}-3$' .Mide la forma de la distribución de datos en torno del promedio. Es positivo si los datos tienen alta concentración en torno de la media y negativo en caso contrario.

Si las frecuencias de las variables en la muestra son distintas:
$$\bar{x}=\frac{1}{n}\sum\limits_{j=1}^{m}x_{j}f_{j}$$
$$s=\sqrt{\frac{1}{n-1} \sum\limits_{j=1}^{n}{[x_{j}-\bar{x}]^{2}f_{j}}} \to s=\sqrt{s^{2}} \cdots s>0$$
$$\gamma = \frac{1}{ns^{3}} \sum\limits_{j=1}^{n}{[x_{j}-\bar{x}]^{3}}f_{j}$$
$$k= \frac{1}{ns^{4}}\sum\limits_{j=1}^{n}[x_{j}-\bar{x}]^{4}f_{j}-3$$

Coeficiente de variación: '$CV= \frac{S}{|\bar{x}|}$'. Es una medida adimensional que indica qué proporción representa la desviación estándar respecto de la media aritmética. Se utiliza con frecuencia en la comparación de la variabilidad de dos o más conjuntos de datos que difieren en unidades y/o magnitudes.

**Boxplot**
![[Pasted image 20240305090902.png|500]]
![[Pasted image 20240305090923.png|500]]

Según el coeficiente de Kurtosis:
- $k=0:$ El peso de las colas es similar al de una distribución normal.
- $k>0:$ El peso de las colas es menor al de una distribución normal.
- $k<0:$ El peso de las colas es mayor al de una distribución normal.

![[Pasted image 20240308095230.png#center|300]]
#### Datos agrupados
![[Pasted image 20240308095319.png#center]]

![[Pasted image 20240308095425.png#center|450]]

$f:$ Frecuencia relativa de la muestra.
$F:$ Frecuencia acumulada, se va sumando cada frecuencia relativa en orden.