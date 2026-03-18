### Método de asignación de polos
Si el sistema es completamente controlable, es decir, $rango(C)=n$, se puede determinar la matriz ganancia mediante la igualdad:
$$
|sI-A+BK| = (s-p_{1})\cdot(s-p_{2})\dots(s-p_{n})
$$
Para asignar los polos de lazo cerrado, se tendrá en cuenta que:
- Un par de polos debe dominar la respuesta. En general, serán complejos, salvo los casos en que, por limitaciones físicas no se admita el sobrepaso
- El resto de los polos (para sistemas de orden 3 o mayor) se ubicarán de cuatro a seis veces hacia la izquierda de los dominantes.

**Obs:** Aunque en teoría pueda parecer que los polos de lazo cerrado de un sistema de control se pueden ubicar en cualquier lugar del semiplano izquierdo s , se ha de tener en cuenta que el incremento de la velocidad de respuesta (aumento del ancho de banda) producen en general un incremento de los efectos adversos de las perturbaciones y del ruido de las mediciones.

Vamos con un ejemplo para entender el funcionamiento de este procedimiento:

El objetivo es reubicar el polo del integrador de manera que esté en -1.

![[Pasted image 20251021133143.png#center|150]]

Aplicando realimentación lineal de estados:

![[Pasted image 20251021151213.png#center|150]]

De esta forma, las ecuaciones quedan tal que:
$$
\begin{split}
& U = R - KY = R - K \cdot\frac{U}{s} \to \frac{Y}{R} = \frac{1}{s+K}
\end{split}
$$
Si se busca que el polo se encuentre en $s=-1$ → $K=1$.

Los polos a lazo cerrado son las raíces de la ecuación característica o polinomio denominador de $T(s)$ o los autovalores de la matriz $A$. Conociendo los polos a lazo cerrado y la performance del sistema, podemos modificar la posición de los polos de dicho sistema a lazo cerrado.
### Control integral
Si bien con Pole Placement puedo modificar la respuesta transitoria del sistema, no puedo modificar la respuesta en régimen permanente, es decir, no puedo cambiar o mejorar el tipo del sistema.

 En el siguiente esquema, tengo el diseño del controlador Pole Placement ya implementado, al cual se le ha realimentado la salida y, que con la entrada r, dan lugar al error e, el cual es la señal de entrada al controlador mediante un integrador. Este integrador aumenta el tipo del sistema.

![[Pasted image 20251021154058.png#center|]]

El espacio de estado del sistema a lazo abierto (sin efectuar el Pole Placement ni incorporar el Control Integral) es:

$$
\begin{split}
& \dot{x} = Ax + Bu \\
& y = Cx + Du
\end{split}
$$
Al efectuar el Pole Placement, el nuevo espacio de estado del sistema realimentado es:
$$
\begin{split}
& \dot{x} = (A-Bk)x + Br \\
& y = Cx + Du
\end{split}
$$
El orden del sistema es el mismo, pero con los polos reubicados para cumplir con las especificaciones de respuesta transitoria. La incorporación del integrador aumenta el orden del sistema, o también se incorpora un estado extra al sistema, que es la integral de la salida.
$$
\dot{x}_{N} = r -y \to \dot{x}_{N} = r - Cx - Du
$$
Entonces, el nuevo espacio de estado será:
$$
\begin{bmatrix}
\dot{x} \\
\dot{x}_{N}
\end{bmatrix}
= \begin{bmatrix}
A & 0 \\
-C & 0
\end{bmatrix}
\cdot \begin{bmatrix}
x \\
x_{N}
\end{bmatrix}
+
\begin{bmatrix}
B \\
-D
\end{bmatrix}
u
+
\begin{bmatrix}
0 \\
1
\end{bmatrix}
r
\qquad y = \begin{bmatrix}
C & 0
\end{bmatrix}
\begin{bmatrix}
x \\
x_{N}
\end{bmatrix}
+ Du
$$
### Observador de estado
A veces la implementación de una realimentación lineal de estados completo no es muy práctica. Para un sistema de $n$ dimensiones, se requieren n mediciones, lo que a su vez, se requieren $n$ transductores, esto hace que el sistema sea muy caro y también voluminoso.

El sistema que realiza la observación de las variables de estado a partir de las informaciones recibidas de las medidas de las entrada y de la salida recibe el nombre de Observador.

El diagrama completo con la planta física, controlador y observador es:
![[Pasted image 20251021160320.png#center]]

El Observador debería tener la misma ecuación de estado que el sistema original, y debe ser capaz de minimizar el error entre $x(t)$ y $\hat{x}(t)$. Puesto que no podemos medir directamente $x(t)$, se compara $y(t)$ e $\hat{y}(t)$ donde:
$$
\begin{split}
& \hat{x}(t) = A x(t) + Bu(t)+L(y(t)-\hat{y}(t)) \\
& \hat{y}(t) = C\hat{x}(t)
\end{split}
$$
Si desarrollamos, la ecuación característica de un ibservador de estado queda tal que:
$$
|sI - (A-LC)| = 0
$$