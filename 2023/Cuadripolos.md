---

---
---
**Obs.** Dentro del cuadripolo NO debe haber *fuentes independentes*, de tenerlas, la debo quitar del circuito que es el cuadripolo
![[Pasted image 20231017192944.png|300]]
Por convención, las corrientes de arriba son entrantes y las de abajo salientes.
![[Pasted image 20231017193154.png]]
$$Parámetros~~impedancias\begin{cases}
& V_{1}=Z_{11}I_{1}+Z_{12}I_{2} \\
& V_{2}=Z_{21}I_{1}+Z_{22}I_{2} \\
& Z=\begin{pmatrix}
Z_{11} & Z_{12} \\
Z_{21} & Z_{22}
\end{pmatrix}
\end{cases}$$
Donde puedo despejar las impedancias:
$$\begin{split}
Z_{11}=\frac{V_{1}}{I_{1}}|_{I_{2}=0} \quad & \quad Z_{21}=\frac{V_{2}}{I_{1}}|_{I_{2}=0} \\ Z_{12}=\frac{V_{1}}{I_{2}}|_{I_{1}=0} \quad & \quad Z_{22}=\frac{V_{2}}{I_{2}}|_{I_{1}=0}
\end{split}$$
$$Parámetros~~admitancias\begin{cases}
& I_{1}=Y_{11}V_{1}+Y_{12}V_{2} \\
& I_{2}=Y_{21}V_{1}+Y_{22}V_{2} \\
& Y=\begin{pmatrix}
Y_{11} & Y_{12} \\
Y_{21} & Y_{22}
\end{pmatrix}
\end{cases}$$
Donde puedo despejar las admitancias:
$$\begin{split}
Y_{11}=\frac{I_{1}}{V_{1}}|_{V_{2}=0} \quad & \quad Y_{21}=\frac{I_{2}}{V_{1}}|_{V_{2}=0} \\ Y_{12}=\frac{I_{1}}{V_{2}}|_{V_{1}=0} \quad & \quad Y_{22}=\frac{I_{2}}{V_{2}}|_{V_{1}=0}
\end{split}$$
Si mezclo $Z$ e $Y$, son parámetros:
- Híbridos H: ($V_{1}$ e $I_{2}$ indef, $V_2$ e $I_1$ def)
- Híbridos G: ($V_{2}$ e $I_{1}$ indef, $V_1$ e $I_2$ def)
- Transmisión: ($V_{2}$ e $I_{2}$ indef, $V_1$ e $I_1$ def)
- Transmisión inversa: ($V_{1}$ e $I_{1}$ indef, $V_2$ e $I_2$ def)

#### Transmisión (T)
$$\begin{split}
& V_{1}=A.V_{2}-B.I_{2} \\ 
& I_{1}=C.V_{2}- D.I_{2} \\
& \begin{bmatrix}
V_{1} \\
I_{1}
\end{bmatrix} = \begin{bmatrix}
A & B \\
C & D
\end{bmatrix}
\begin{bmatrix}
V_2 \\
-I_2
\end{bmatrix}
\end{split}$$
Si uno de los valores da infinito decimos que no es representable con esos parámetros. En cualquier otro caso no hay problema.

Un cuadripolo es *recíproco*, si solo está conformado por componentes pasivos. $Z_{21}=Z_{12},\ Y_{21}=Y_{12},\ A.D~-~C.B=1,\ H_{12}=-H_{21}$
Un cuadripolo es *simétrico*: $Z_{11}=Z_{21},\ Y_{11}=Y_{22}, \ A=D,\ H_{11}.H_{22}-H_{12}H_{21}=1$

**Obs.** Si tengo cuadripolos en serie, los parámetros del cuadripolo total es la suma de los parámetros de cada cuadripolo.

El **test de Brune** me ayuda a saber si puedo "separar" un cuadripolo en varios cuadripolos en serie. Si esto no se cumple, tengo que analizar el cuadripolo grande.

Condiciones de test de Brune(En serie):
1) Test de Brune a las entradas y hago corto en las salidas.
2) Hago corto en las entradas y el test de Brune en la salida.

Condiciones de test de Brune(Paralelo):
1) Test de Brune a las entradas y dejo abierto las salidas.
2) Dejo abierto las entradas y el test de Brune en la salida.

![[Pasted image 20231019184437.png|500]]
![[Pasted image 20231019185116.png|500]]
**Obs.**
En serie me conviene trabajar con parámetros de impedancia. En paralelo me conviene trabajar con parámetros de admitancia. En cascada me conviene trabajar con parámetros de transmisión.
### Tabla
![[Pasted image 20231101105809.png]]
**Obs.** Si los parámetros $Z$ y los parámetros $Y$ existen → $Z^{-1}=Y$.
### Circuitos con cuadripolos
![[Pasted image 20231102093441.png|300]]
$$G_{v}= \frac{V_{0}}{V_{i}}=H_{v} \qquad G_{i}= \frac{I_{0}}{I_{i}}=H_{i}$$
#### Impedancia de entrada
Si tengo el siguiente circuito:
![[Pasted image 20231102093828.png|250]]
La impedancia de entrada será $H=Z_{inp}= \frac{V_{1}}{I_{1}}$.
#### Impedancia de salida
Para calcular la impedancia de salida, tomo $V_{g}=0$, tal que: $Z_{out}= \frac{V_{2}}{I_{2}}|_{V_{g}=0}$.
**Obs.** El $Z_{out}$ es el $Z_{th}$.