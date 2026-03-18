----
![[Pasted image 20230928144814.png|400]]
$$V=V_{m}e^{\sigma t} e^{j(\omega t+\theta)}=V_{m}e^{j\theta}e^{(\sigma+j\omega)t}=V_{m}e^{j\theta}e^{st} \quad (Ec.~de~excitación~gral)$$
Donde $s=\sigma+j\omega$

$\sigma:$ Frecuencia de decaimiento
$s:$ Frecuencia compleja
$\omega:$ Frecuencia real(angular)

![[Pasted image 20230928145326.png|500]]
![[Ejemplo, Respuesta en frecuencia_1]]
### Función de transferencia
Se define como:
$$H(s)= \frac{Respuesta}{Excitación}=(del~ej~anterior)\frac{I(1)}{V_{f}(1)}$$
**Obs.** Es una admitancia.
Si analizamos la tensión del capacitor $(V_{c})$ como nuestra respuesta → $\frac{V_{c}}{V_{f}}= G_{v}$ → Es una ganacia de potencia.

##### Obs
Hay 4 formas que puede tomar la función de transferencia:
$$\begin{split}
& Impedancia~(Z) \\
& Admitancia~(Y) \\
& Ganancia~de~Potencia~(G_{v}) \\
& Ganancia~de~corriente~(G_{i})
\end{split}$$
![[Ejemplo, Respuesta en frecuencia_2]]
##### Obs
No importa la excitación en el circuito, la ec. característica siempre será igual, ya que es propia del circuito.
![[Pasted image 20230928175533.png]]
##### Obs
Los polos siempre serán negativos para que en el transitorio no se quemen.
![[Pasted image 20230928181317.png|300]]
Si tengo un circuito ideal únicamente con inductor y capacitor, donde les doy un impulso pero luego los aislo de la fuente → Los polos van a estar en el eje imaginario, ya que $R=0~\ohm$.
![[Pasted image 20230928183620.png|500]]
![[Pasted image 20230928184614.png|500]]
El orden de la expresión en el denominador de la función de transferencia, es el número de componentes almacenadores independentes del circuito.
Recordamos:
$$H(S)= \frac{a_{n}S_{1}^{n}+a_{n+1}S_{1}^{n-1}+...}{b_{n}S_{2}^{m}+b_{n+1}S_{2}^{m-1}+...}= \frac{(S+C_{1})(S+C_{2})(S+C_{3})...}{(S+P_{1})(S+P_{2})(S+P_{3})...}$$
Entonces, $m$ es el número de almacenadores del circuito.
> $C_{j}$ son los ceros, y $P_{k}$ son los polos.
> Obs. Los polos deben ser negativos(su parte real).

**Obs.** Veo los polos en mi función transferencia y puedo saber como será el transitorio. Por ej, si tengo dos polos reales distintos, entonces se que el transitorio será sobreamortiguado.

**Obs.** La función transferencia se calcula en el régimen permanente, cuando ya paso mucho tiempo en el circuito.

**Obs.** Los ceros amplifican y los polos atenuan.

#### Ganancia en potencia
$$G_{POT}= \frac{P_{0}}{P_{i}} \quad G_{B}= log\left(\frac{P_{0}}{P_{i}}\right)\quad G_{dB}= 10~log\left(\frac{P_{0}}{P_{i}}\right)$$
Como $P_{0}= \frac{V_{0}{^{2}}}{Z_{0}}, P_{i}= \frac{V_{i}{^{2}}}{Z_{0}}$ → $G_{dB}=20~log(\frac{V_{0}}{V_{i}})$
Ej.![[Pasted image 20231003201112.png|300]]
#### Valores del módulo de la función transferencia
![[Pasted image 20231003203700.png|400]]
##### Diagramas del módulo de la función de transferencia
Se lo representa como dB en función de la frecuencia en escala logarítmica.

##### Diagramas de la fase de la función de transferencia
Se lo representa como grados en función de la frecuencia en escala logarítmica.

### Diagramas logaríitmicos
Se convierte la multiplicación de los módulos de amplitud en sumas algebraicas.

#### Trazado de curvas asintóticas
En forma rápida y sencilla, información del comportamiento del sistema. Para valores exactos, corrección de las curvas

### Propiedad
La función de transferencia se puede expresar como el producto de factores. Los factores que se pueden encontrar son:
![[Pasted image 20231003203023.png|500]]

### Diagrama de Bode
1) $H(j\omega)=K(cte)$
- $K>1 \Rightarrow H_{dB} > 0$
- $K<1 \Rightarrow H_{dB} < 0$
El gráfico de Bode del módulo es una **línea recta de valor cte para todo $\omega$**. El gráfico de fase es 0 para todo $\omega$.
**Obs.** El variar la función transferencia por una cte (K) aumenta o disminuye la amplitud de salida del sistema en forma cte para todas las frecuencias sin producir desfasaje alguno.
2) $H(j\omega)=(j\omega)^{\pm n}$
La amplitud de la señal de salida crecerá o decaerá a razón de $20*n$ dB/década($6*n$ dB/Octava) a medida que aumenta la frecuencia y la salida estará desfasada ($90*n$)° para todas las frecuencias.
3) $H(j\omega)=(1+ \frac{j\omega}{T})^{\pm n}$
![[Pasted image 20231003205336.png|400]]
![[Pasted image 20231003205315.png|400]]
![[Pasted image 20231003205302.png|400]]
4) $H(j\omega)=[1+2\xi (j\omega/\omega_{0})+(j\omega/\omega_{0})^{2}]^{\pm 1}$
**Obs.** El gráfico del módulo de la función transferencia está conformado por dos asíntotas:
- Una que vale **cero** hasta $\omega=T$
- Otra que decae a razón de 40 dB/década (6 dB/Octava) para $\omega>T$
![[Pasted image 20231005181715.png|300]]
![[Pasted image 20231005181750.png|400]]
Se determinan las asíntotas de baja y alta frecuencia independientemente del valor de $\xi$. Cerca de $\omega_{0}$ se produce un pico de la señal y depende de $\xi$. A menor $\xi$, mayor valor del pico, y por ende mayor el error de trazar el gráfico según las asíntotas.
Si $\xi>1$ se puede expresar la ecuación como una multiplicación de binomios con dos raíces y planteo el diagrama de Bode de cada uno. Se simplifican a diagramas de Bode de *orden 1*.
**Obs.** Si $\omega=\omega_{0} \Rightarrow |H(dB)|=-20.log\sqrt{(2.\xi)^{2}}$
![[Pasted image 20231005182236.png|300]]
![[Pasted image 20231005182257.png|300]]
- La fase según $\xi$:
![[Pasted image 20231005182406.png|200]]
**Obs.** El menos del arcotangente aparece porque estamos considerando la función transferencia en el denominador.
![[Pasted image 20231005183136.png|400]]
### Resumen
![[Pasted image 20231005183536.png|400]]
#### Tabla para diagramas de Bode
|                           $H(j\omega)$                           |  Octavas   |   Décadas   |                   Polaridad                    |   Fase    | Error |
|:----------------------------------------------------------------:|:----------:|:-----------:|:----------------------------------------------:|:---------:| ----- |
|                              K(cte)                              | $6*log(K)$ | $20*log(K)$ | $\|H(dB)\|<0$ si $K<1$, $\|H(dB)\|<0$ si $K>1$ |           |       |
|                       $(j\omega)^{\pm n}$                        |  $6*n$ dB  |  $20*n$ dB  |                     $\pm$                      | $(90*n)°$ |       |
|                 $(1+ \frac{j\omega}{T})^{\pm n}$                 |  $6*n$ dB  |  $20*n$ dB  |                     $\pm$                      |           |       |
| $[1+2\xi (j\omega/\omega_{0})+(j\omega/\omega_{0})^{2}]^{\pm 1}$ |  $6*n$ dB  |  $20*n$ dB  |                     $\pm$                      |           |       |

El signo '+' corresponde a los ceros de la función transferencia, y el signo '-' a los polos.
