### Sistemas realimentados
El diagrama de bloques de un sistema realimentado negativamente será:

![[Pasted image 20250808183655.png#center|300]]

Donde la transferencia a lazo abierto será:
$$
G(s) = \frac{Y(s)}{U(s)}
$$
La transferencia total del sistema será:
$$
T(s) = \frac{Y(s)}{R(s)} = \frac{G(s)}{1+G(s)H(s)}
$$
#### Respuesta al escalón
Al realizar la respuesta al escalón del sistema, habrá un error porcentual acorde al valor final de la respuesta. Idealmente, el error debe ser 0%.

![[Pasted image 20250808184027.png#center|400]]

#### Sistema regulador
Este tipo de sistemas cuentan con una entrada nula ($R(s)=0$). La salida no depende de la entrada. El objetivo de estos sistemas es obtener una respuesta ‘cte’ que no depende de la entrada.
#### Sistema de tracking
Estos sistemas tienen una entrada nula. El objetivo es analizar como responde el sistema a los cambios en la entrada.
### Sistemas de primer orden
La transferencia de un sistema de primer orden será de la forma:
$$
\frac{Y(s)}{R(s)} = G(s) = \frac{\frac{1}{T}}{s+ \frac{1}{T}}
$$
Donde la repuesta al escalón unitaria está dada por $R(s)=\frac{1}{s}$.
#### Parámetros
- Rise time: $T_{r}=2.2\cdot T$
- Tiempo de establecimiento: $T_{s} = 4\cdot T$
### Sistemas de segundo orden
La transferencia de un sistema de segundo orden será de la forma:
$$
G(s) = \frac{\omega_{n}^{2}}{s^{2}+2\xi \omega_{n}s+\omega_{n}^{2}}
$$
Donde $\xi$ es el factor de amortiguamiento y $\omega_{n}$ es la frecuencia natural del sistema. Los polos estarán dados por la siguiente expresión:
$$
S_{1,2} = -\xi \cdot \omega_{n} \pm j\cdot \omega_{n} \sqrt{ 1-\xi^{2} } = -\sigma \pm j\cdot \omega_{d}
$$
Donde $\sigma$ es el amortiguamiento exponencial, y $\omega_{d}$ es la frecuencia de amortiguamiento.
#### Casos para distintos valores del factor de amortiguamiento
1) Sobreamortiguado:

![[Pasted image 20250808190658.png#center|400]]

2) Crítico:

![[Pasted image 20250808190736.png#center|400]]

3) Subamortiguado:

![[Pasted image 20250808190825.png#center|400]]

4) Oscilatorio:

![[Pasted image 20250808190858.png#center|400]]

5) Cuasi inestable:

![[Pasted image 20250808191009.png#center|400]]

6) Inestable:

![[Pasted image 20250808191034.png#center|400]]
#### Respuesta al escalón unitario

![[Pasted image 20250808191146.png#center|450]]

##### Parámetros
- Tiempo pico: $T_{p} = \frac{\pi}{\omega_{n}\sqrt{ 1-\xi^{2} }}=\frac{\pi}{\omega_{d}}$
- Máximo sobrepico (porcentual): $OS\% = \frac{y_{max}-y_{final}}{y_{final}}\cdot 100$
- Factor de amortiguamiento: $\xi = \frac{-\ln\left( \frac{OS\%}{100} \right)}{\sqrt{ \pi^{2} + \ln^{2}\left( \frac{OS\%}{100} \right) }}$
- Tiempo de establecimiento: $T_{s} = \frac{4}{\xi \omega_{n}}$
- Tiempo de rise: $T_{r} = \frac{arcos(\xi)}{\omega_{d}}$
### Error permanente
El error estacionario es una medida de la exactitud de un sistema de control. Se juzga el estado estacionario por el error debido a entradas escalón, rampa y parábola.

Cualquier sistema de control sufre inherentemente un error estacionario o permanente en respuesta a cierto tipo de entradas. La única manera de eliminar este error es modificando la estructura del sistema. Si un sistema de control presenta o no error estacionario ante un tipo de entrada, depende del tipo de transferencia a lazo abierto del sistema.

Un sistema se denomina tipo 0, tipo 1, tipo 2, ..., si n=0, n=1, n=2, …, dependiendo de la multiplicidad de los polos. Al aumentar el número de tipo, aumenta la exactitud, pero empeora el problema de la estabilidad., por lo tanto, hay que establecer un compromiso entre la exactitud y la estabilidad.

![[Pasted image 20250808195732.png#center|250]]

Donde si $H(s)=1 \to E(s)=R(s)-Y(s)= \frac{R(s)}{1+G(s)}$

El error en régimen permanente o estado estacionario, aplicando el teorema del valor final, queda definido por:
$$
e_{ss} = \lim_{ t \to \infty } e(t)  = \lim_{ s \to 0 } s\cdot \frac{R(s)}{1+G(s)} 
$$
#### Escalón
Tomando $R(s)=\frac{R}{s}$, el error en régimen permanente será $e_{{ss}} = \frac{R}{1+K_{p}}$, siendo $K_{p}=\lim_{ s \to 0 } G(s)$ la constante estática de error de posición.

- $n=0$ → Sistema tipo 0 → $e_{ss}=\frac{R}{1+K_{p}}$
- $n \geq 1$ → Sistema tipo 1 o más → $e_{ss}=0$
#### Rampa
Tomando $R(s)=\frac{R}{s^{2}}$, el error en régimen permanente será $e_{{ss}} = \frac{R}{K_{v}}$, siendo $K_{v}=\lim_{ s \to 0 } s\cdot G(s)$ la constante estática de error de velocidad.

- $n=0$ → Sistema tipo 0 → $e_{ss} = \infty$
- $n = 1$ → Sistema tipo 1 → $e_{ss}= \frac{R}{K_{v}}$
- $n \geq 2$ → Sistema tipo 2 o más → $e_{ss}=0$
#### Parábola
Tomando $R(s)=\frac{R}{s^{3}}$, el error en régimen permanente será $e_{{ss}} = \frac{R}{K_{a}}$, siendo $K_{a}=\lim_{ s \to 0 } s^{2}\cdot G(s)$ la constante estática de error de aceleración.

- $n=0$ → Sistema tipo 0 → $e_{ss} = \infty$
- $n = 1$ → Sistema tipo 1 → $e_{ss}= \infty$
- $n = 2$ → Sistema tipo 2 → $e_{ss}=\frac{R}{K_{a}}$
- $n \geq 3$ → Sistema tipo 3 o más → $e_{ss}= 0$
#### Determinación del Error Permanente considerando la función de transferencia a lazo cerrado T(s)
$$
e_{ss} = \lim_{ s \to 0 } s\cdot R(s) \cdot (1-T(s)) 
$$
