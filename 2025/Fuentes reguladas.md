El objetivo es generar una salida constante de tensión ante la modificación de cargas.

Idealmente, para cualquier corriente que me pida la carga, la salida debe mantener la tensión constante.

![[Pasted image 20250828194046.png#center]]
### Reguladores paralelos
Este método consta de colocar un componente que regule la tensión, en paralelo a la carga. En este caso, usamos un diodo zener.
$$
\text{Factor absoluto de estabilidad de tensión} \qquad  K_{s} = \frac{\Delta V_{o}}{\Delta V_{R}} \bigg{|}_{R_{L}=cte} = \frac{R_{L}\parallel r_{z}}{R_{L}\parallel r_{z}+R_{o}} \simeq \frac{r_{z}}{r_{z}+R_{o}}
$$
Este método tiene varias contras:
- La tensión debe coincidir con un valor normalizado de $V_{z}$.
- En vacio no debe tener problemas. Desconectar la carga puede dañar el circuito.
- Alimentar más circuitos (pedir más corriente) sin problema. Dependemos del rango de carga para los limites de corriente del diodo zener.

![[Pasted image 20250911095138.png#center|250]]
### Regulador serie
Este método utiliza un transistor para aprovechar la ganancia de corriente y no necesitar que el zener de toda la corriente que pide la carga.

![[Pasted image 20250911095653.png#center|300]]

La carga puede tomar valores tal que: $R_{L} \in \left[ \frac{R_{L_{min}}  }{\beta+1}, \frac{R_{L_{max}}  }{\beta+1} \right]$. El rango fue desplazado y achicado en $\beta+1$. La ventaja de esto es que logro trabajar con cargas de menor valor.

Si quiero valores de carga mayores, simplemente desconecto Q1.
### Algunos ejemplos de fuentes más complejas

![[Pasted image 20250911142429.png#center|350]]

![[Pasted image 20250911142630.png#center|350]]

![[Pasted image 20250911142845.png#center|350]]

![[Pasted image 20250911143237.png#center|350]]

![[Pasted image 20250911144448.png#center|350]]

![[Pasted image 20250911090438.png]]
Es importante a la hora de analizar estos circuitos, entender las condiciones de funcionamiento extremas, no solo en regulación. Se nos pedirá que busquemos valores máximos y mínimos de $R_{L}$, de la alimentación, de alguna resistencia que configure una fuente de corriente, y las expresiones para hallar esto dependerá del circuito. Por eso mismo es importante definir los bloques, quien entrega toda la corriente, quien satura, o quien se puede quemar.

Generalmente, para analizar los límites de la carga, vamos a utilizar estas expresiones:
$$
\begin{split}
R_{L}\bigg{|}_{max} = \frac{V_{o}\bigg{|}_{reg}}{i_{o}\bigg{|}_{min}} \\
R_{L}\bigg{|}_{min} = \frac{V_{o}\bigg{|}_{reg}}{i_{o}\bigg{|}_{max}} 
\end{split}
$$
### Circuitos de protección contra cortocircuito
El objetivo de estos circuitos es ‘activarse’ cuando la corriente de salida es máxima, debido a que la carga es menor a la mínima calculada. 
#### Lineal
![[Pasted image 20250911093711.png#center|300]]

El valor de $R_{1}$ es elegido de la corriente máxima que puede circular. Si queremos que el transistor $T_{p}$ sólo se active si la corriente que pasa por $R_{1}$ es la máxima, entonces:
$$
V_{BE_{on}}= R_{1}I_{o_{max}}
$$
#### Foldback
En este tipo de protecciones, lo que ocurrirá es que bajará la corriente de salida, causando que disminuya la tensión de salida.
![[Pasted image 20250911094225.png#center|300]]
Si $R_{3}$ en lugar de conectarse a tierra, se conecta a una tensión $V_{x}$, se puede desplazar el punto de $I_{o_{cc}}$.
### Reguladores integrados
Estos son fuentes reguladas que ya vienen armadas. La contra de esto es que vienen para un valor de tensión de salida fijo. Tienen 3 terminales, y garantizan que entre la terminal de control y de salida, tengan la diferencia de tensión de ese modelo.

Esto es útil cuando queremos tener una alimentación constante y con el menor ruido posible. También, si en la terminal de control se conecta un generador, se puede conseguir un generador con un offset.