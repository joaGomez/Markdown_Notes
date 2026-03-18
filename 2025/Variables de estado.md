### El modelo de estado continuo
A partir de la función transferencia:
$$
G(s) = \frac{Y(s)}{U(s)} = \frac{N(s)}{D(s)} \longrightarrow D(s)\cdot Y(s) = N(s) \cdot U(s)
$$
Antitransformando por Laplace $(\text{con } N(s)=K):$
$$
\frac{d{^{n}y(t)}}{dt}+\dots+a_{0}~y(t) = K\cdot u(t)
$$
Con $n=3$, las variables de estado serán:
$$
\begin{cases}
x_{1} = y \\
x_{2} = \dot{y} = \dot{x_{1}} \\
x_{3} = \ddot{y} = \dot{x_{2}}
\end{cases}
$$
Despejando de la derivada de mayor orden de expresión completa:
$$
\dddot{y} = -a_{2}\ddot{y} - a_{1}\dot{y} - a_{0}y +Ku
$$
Las ecuaciones de estado se definen como:
$$
\begin{cases}
\dot{x_{1}} = x_{2} \\
\dot{x_{2}} = x_{3} \\
\dot{x_{3}} = -a_{0}x_{1}-a_{1}x_{2}-a_{2}x_{3}+Ku
\end{cases} \quad
\Longrightarrow
\begin{bmatrix}
\dot{x_{1}} \\
\dot{x_{2}} \\
\dot{x_{3}}
\end{bmatrix}
=
\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-a_{0} & -a_{1} & -a_{2} 
\end{bmatrix}
\cdot
\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}
+
\begin{bmatrix}
0 \\
0 \\
K
\end{bmatrix}
\cdot u

$$
Los sistemas que están representados por ecuaciones diferenciales con coeficientes constantes, se denominan sistemas invariables en el tiempo. Los sistemas físicos representados por ecuaciones diferenciales a coeficientes no constantes, dependientes del tiempo, se denominan sistemas variables en el tiempo.

> Observaciones:
> **Diagrama en bloques:**
> ![[Pasted image 20250818182126.png#center|400]]
> Para un sistema, se puede llegar a la siguiente expresión: $$X(s) = [sI-A]^{-1}x(0)+[sI-A]^{-1}B\cdot U(s)$$
> Donde $[sI-A]^{-1}$ es el denominador y es la ecuación caraterística. Cuando este es igual a cero, sus raíces son los polos/autovalores de $X(s)$.

### Sistemas instantáneos o estáticos
Son aquellos que su salida $y(t_{0})$ depende únicamente del valor de entrada aplicada en el instante $t_{0}$.
### Sistemas dinámicos
La salida del sistema en el instante $t_{0}$ depende de los valores pasados, presentes y/o futuros.
### Represantaciones alternativas en el espacio de estado
##### Forma variable de fase
Sea $G(s) = \frac{Y(s)}{U(s)} \frac{20s+8}{s^{3}+21s^{2}+24s+8}$, se puede descomponer tal que: $\frac{Y(s)}{U(s)}=\frac{X_{1}(s)}{U(s)}\cdot\frac{Y(s)}{X_{1}(s)}$
De esta manera, queda el siguiente sistema de ecuaciones:
$$
\begin{split}
& X_{1}s^{3}+21X_{1}s^{2}+24X_{1}s+8X_{1} = U \\
& Y = 20X_{1}s+8X_{1}
\end{split}
$$
De esta forma, las matrices de estado quedarán definidas como:
$$
A=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-8 & -24 & -21
\end{bmatrix}
\quad B= \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
\quad C=
\begin{bmatrix}
8 & 20 & 0
\end{bmatrix}
\quad D = 0
$$
##### Forma canónica de controlabilidad
A partir de la forma Canónica de Variable de fase, la matriz $A_{c}$ se obtiene de invertir el orden de las filas y el orden de las columnas de la matriz $A$, la matriz $B_{c}$ se obtiene de invertir el orden de las filas de $B$, y la matriz $C_{c}$ el orden de las columnas de la matriz $C$.
$$
A_{c}=\begin{bmatrix}
-21 & -24 & -8 \\
1 & 0 & 0 \\
0 & 1 & 0
\end{bmatrix}
\quad B_{c}= \begin{bmatrix}
1 \\
0 \\
0
\end{bmatrix}
\quad C_{c}=
\begin{bmatrix}
0 & 20 & 8
\end{bmatrix}
\quad D_{c} = 0
$$
##### Forma canónica de observabilidad
A partir de la forma canónica de controlabilidad, la matriz $A_{o}$ es la traspuesta de $A_{c}$, la matriz $B_{o}$ es la traspuesta de $C_{c}$, y la matriz $C_{o}$ es la traspuesta de $B_{c}$.
$$
A=\begin{bmatrix}
-21 & 1 & 0 \\
-24 & 0 & 1 \\
-8 & 0 & 0
\end{bmatrix}
\quad B= \begin{bmatrix}
0 \\
20 \\
8
\end{bmatrix}
\quad C=
\begin{bmatrix}
1 & 0 & 0
\end{bmatrix}
\quad D = 0
$$
### Tansformación de estados o transformación de similaridad
Llamamos $T$ a la matriz de transformación de estados, tal que $x(t) = Tz(t)$, por lo tanto:
$$
\begin{split}
& \dot{z}(t) = T^{-1}ATz(t)+T^{-1}Bu(t) \\
& y(t) = CTz(t) + Du(t)
\end{split}
$$
Si los valores propios o autovalores de $A$ son todos distintos entre sí, la matriz $A_{d} = T^{-1}AT$ es una matriz diagonal, y el modelo transformado se encuentra en el denominado formato modal.
