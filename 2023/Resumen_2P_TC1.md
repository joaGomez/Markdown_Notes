### Tema 1: Potencia en alterna
##### Potencia activa
$$P=V_{ef}I_{ef}cos(\varphi)\qquad [W]$$
##### Potencia aparente
$$|S|=V_{ef}I_{ef} \qquad [VA]$$
##### Potencia reactiva
$$Q=V_{ef}I_{ef}sen(\varphi) \qquad [VAR]$$
El valor medio en un período es igual a cero, pero para poder dimensionar la misma se adopta:
![[Pasted image 20230824183759.png|250]]
##### Potencia compleja
$$S=P+jQ=\frac{V_{ef}^{2}}{Z^*}$$
##### Factor de potencia
$$cos(\theta_{v}-\theta_{i})=cos(\varphi)=\frac{P}{S}=\frac{R}{Z}$$
##### Triángulo de potencias
![[Pasted image 20230824184101.png|300]]
![[Pasted image 20230824184244.png|300]]
**X**: Parte reactiva (*Imaginaria*)
**R**: Parte resistiva (*Real*)

##### Aumentar el factor de potencia
Para aumentar el valor de del factor de potencia, hay que achicar el valor de $\varphi$. Para esto, lo que se hace es conectar un capacitor en paralelo a la carga. 
![[Pasted image 20230831224158.png|200]]
De este modo se consigue un $Q_{c}$ (Potencia reactiva de la capacitancia) que reduce el valor de $\varphi$ ya que ahora $Q' = Q - Q_{c}$.
![[Pasted image 20230831224253.png|100]]
Donde en módulo:
$$\begin{split}
& Q_{c}= X_{c}I_{c}^{2}=\frac{V^{2}}{X_{c}}=\frac{V^{2}}{\frac{1}{\omega C}} \\
& Q_{c}= \omega C V^{2} \\
& C =\frac{Q_{c}}{\omega V^{2}} = \frac{Q_{c}}{(2\pi f)V^{2}}
\end{split}$$
Además:
$$
\begin{split}

& Q_{c}= Q - Q' = P ~ (tg(\varphi) \ - \ tg(\varphi '))

\end{split}
$$
Por lo que podemos deducir la expresión:
$$C = \frac{P ~ (tg(\varphi) \ - \ tg(\varphi '))}{2\pi f V^{2}}$$

##### Máxima transferencia de potencia
![[Pasted image 20230831231705.png|300]]
![[Pasted image 20230831231810.png|300]]
Y se deben cumplir la siguiente condición:
$$X_{L}=-X_{Th} \qquad R_{Th}=R_{L} \qquad Z_{L}=Z_{Th}^{*}$$
![[Pasted image 20230831232107.png|150]]
Entonces:
$$P_{L}= \frac{|V_{th}|^{2}.R_{Th}}{4R_{Th}^{2}+X_{Th}^{2}}$$
Y para tener la máxma transferencia de potencia:
$$\frac{dP_{L}}{dR_{L}}=0$$
Donde para este circuito en particular se debe cumplir que:
$$R_{L}= \sqrt{ R_{Th}^{2} +X_{Th}^{2}}$$
### Tema 2: Transtorios
**Importante:**
$$\begin{split}
& I_{L}(t_{0}^{-})= I_{L}(t_{0}^{+}) \\
& V_{C}(t_{0}^{-})= V_{C}(t_{0}^{+})
\end{split}$$

Con el circuito abierto, la tensión y la corriente en un capacitor es 0. En el instante en el que se conecta el capcaitor actúa como un cable. la corriente y la tensión del circuito van a estar regidas por los demás componentes en el circuito. Si solo tengo un capacitor, al conectarlo tendré un *corto*. Cuándo el capacitor esté totalmente cargado, este actuará como un *abierto*.

#### De primer orden
Para las EDO de orden 1, debo plantear las ecuaciones asociadas al circuito y me quedará una ecuación integrable en función de una variable, y de acuerdo a las condiciones iniciales, puedo obtener su forma de carga y descarga.

#### De segundo orden
**Obs.** $\xi = \frac{\alpha}{\omega_{0}}$

Pasos para resolver una EDO de orden 2:
1) Planteo ecuaciones adecuadas al circuito, relacionando las tensiones/corrientes en el circuito. Recuerdo que despues de un tiempo muy largo, el capacitor actua como una llave abierta y se "conserva" ese $V_{c}$, y el inductor actúa como una "cable" y mantiene la corriente $I_{L}$.
2) Mediante las expresiones: $V_{c}= \frac{1}{C}\int I dt$ → $I=C \frac{dV_{c}}{dt}$, $V_{L}=L \frac{dI}{dt}$ → $I= \frac{1}{L}\int V_{L}$, podemos asociar tensiones/corrientes y plantear una EDO para esa variable que asociamos.
3) Una vez planteo la EDO, con los coefiecientes para cada orden los asocio a la forma general normalizada, donde de esto puedo deducir $\xi$. Sabiendo $\xi$, puedo decir si el circuito es, amortiguado, subamortiguado, etc.
**Obs.** La edo de forma general normalizada es:
$$\frac{dI_{L}^{2}}{dT}+2\xi \omega_{0}\frac{dI_{L}}{dT}+I_{L}\omega_{0}^{2}=I\omega_{0}^{2}$$
$\xi=0:$ **Resistencia infinita** → **NO** hay pérdida de energia. La energia se va pasando de inductor a capacitor periódicamente.

$\xi<1:$ Sub-amortiguado → Raíces de la ec. complejas conjugadas
→ $B_{12} = -\xi \omega_{0} \mp j \omega_{0}\sqrt{1-\xi^{2}}$
$\xi = 1:$ Amortiguamiento crítico → Raíces de la ec. reales e iguales.
→ $B_{12} = -\xi \omega_{0}$
$\xi > 1 :$ Sobre amortiguado → Raíces de la ecuación reales distintas.
→ $B_{12} = -\xi \omega_{0} \mp \omega_{0}\sqrt{\xi^{2}-1}$

4) Una vez se como será el comportamiento del circuito, utilizo los resultados para la EDO de Euler. Estos resultados acorde a la variable que use para la EDO.
5) Por último, con las respuestas, puedo despejar las ctes.

### Tema 3: Respuesta en frecuencia
La notación sera tal que: $s=\sigma+j\omega$
Donde: 
$\sigma:$ Frecuencia de decaimiento
$s:$ Frecuencia compleja
$\omega:$ Frecuencia real(angular)

Donde:
$$V=V_{m}e^{\sigma t} e^{j(\omega t+\theta)}=V_{m}e^{j\theta}e^{(\sigma+j\omega)t}=V_{m}e^{j\theta}e^{st} \quad (Ec.~de~excitación~gral)$$
Se define la función de transferencia como:
$$H(s)=\frac{respuesta}{excitación}$$
Hay 4 formas que puede tomar la función de transferencia:
$$\begin{split}
Impendancia(Z)= & \frac{I(s)}{V_{f}(s)} \\
Admitancia(Y)= & \frac{V_{R}(s)}{V_{f}(s)} \\
Ganancia~de~potencia(G_{v})= & \frac{V_{C}(s)}{V_{f}(s)} \\
Ganancia~de~corriente(G_{i})= & \frac{V_{L}(s)}{V_{f}(s)}
\end{split}$$
**Obs.** No importa la excitación en el circuito, la ec. característica siempre será igual, ya que es propia del circuito.

**Obs.** En una función de transferencia, los valores de $s$ que anulan el numerador son los **ceros**, y en el denominador los **polos**.

| Polos                                         | Tipo de circuito       | valor de $\xi$ |
| --------------------------------------------- | ---------------------- | -------------- |
| $s_{1}=\bar{s_{2}}, s_{1},s_{2}\in\mathbb{Z}$       | Subamortiguado | < 1              |
| $s_{1}={s_{2}}, s_{1},s_{2}\in\mathbb{R}$ | Críticamente amortiguado        | 1            |
| $s_{1}\neq{s_{2}}, s_{1},s_{2}\in\mathbb{R}$  | Sobreamortiguado      | > 1               |

**Obs.** La función transferencia se calcula en el régimen permanente, cuando ya paso mucho tiempo en el circuito.

**Obs.** Los ceros amplifican y los polos atenuan.

##### Ganancia en potencia
$$G_{POT}= \frac{P_{0}}{P_{i}} \quad G_{B}= log\left(\frac{P_{0}}{P_{i}}\right)\quad G_{dB}= 10~log\left(\frac{P_{0}}{P_{i}}\right)$$
Como $P_{0}= \frac{V_{0}{^{2}}}{Z_{0}}, P_{i}= \frac{V_{i}{^{2}}}{Z_{0}}$ → $G_{dB}=20~log(\frac{V_{0}}{V_{i}})$

### Tema 4: Resonancia
Este tema consta de buscar la frecuencia de resonancia indicada para que el circuito sea puramente resistivo. Es decir, en el caso de que el circuito involucre inductores y/o capacitores, buscar que la parte imaginaria de la impedancia total en el circuito sea nula.

| Circuito RLC |     Frecuencia de resonancia      |                Factor de calidad                 | Ancho de banda |
|:------------:|:---------------------------------:|:------------------------------------------------:|:--------------:|
|   Paralelo   | $\omega_{0}= \frac{1}{\sqrt{LC}}$ |      $Q=\omega_{0}RC=\frac{R}{\omega_{0}L}$      | $\frac{1}{RC}$ |
|    Serie     | $\omega_{0}= \frac{1}{\sqrt{LC}}$ | $Q=\frac{1}{\omega_{0}RC}=\frac{\omega_{0}L}{R}$ | $\frac{R}{L}$  |

**Obs.** Si $Q \geq 10$ → $\omega_{1}\cong \frac{\omega_{0}-B}{2}$ y $\omega_{2}\cong \frac{\omega_{0}+B}{2}$, por lo que B quedó centrado en $\omega_{0}$.
**Obs.** $Q=\frac{\omega_{0}}{B}$
##### Ancho de banda de mitad de potencia
![[Pasted image 20231024090005.png|350]]
Además, se cumple que: $\omega_{0}^{2}=\omega_{1}\omega_{2}$
**Obs.**
![[Pasted image 20231024090122.png|100]]
### Útil
![[Pasted image 20231024001538.png|200]]
