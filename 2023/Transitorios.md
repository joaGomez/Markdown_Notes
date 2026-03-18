---

---
----
$$V_{L}=L \frac{dI_{L}}{dt} \to I_{L}=\frac{1}{L}\int V_{L}dt$$
![[Pasted image 20230905191451.png]]

**Importante:**
$$\begin{split}
& I_{L}(t_{0}^{-})= I_{L}(t_{0}^{+}) \\
& V_{C}(t_{0}^{-})= V_{C}(t_{0}^{+})
\end{split}$$

Con el circuito abierto, la tensión y la corriente en un capacitor es 0. En el instante en el que se conecta el capcaitor actúa como un cable. la corriente y la tensión del circuito van a estar regidas por los demás componentes en el circuito. Si solo tengo un capacitor, al conectarlo tendré un *corto*. Cuándo el capacitor esté totalmente cargado, este actuará como un *abierto*.

### Circuitos RC
Para $t>0: V_{C}(t)=V(1-e^{\frac{-1}{RC}t})$, de lo que puedo despejar lo siguiente:
$$\begin{split}
&t \to 0 \quad V_{C}=0 \\
&t \to \infty \quad V_{C} = V
\end{split}$$
![[Pasted image 20230905200600.png]]
Para $t>0: I = \frac{V}{R}e^{\frac{-1}{RC}t}$, entonces:
$$\begin{split}
&t \to 0 \quad I = V/R \\
&t \to \infty \quad I = 0
\end{split}$$
![[Pasted image 20230905201014.png]]
Si tengo una **tensión inicial no nula** → $V_{C}(t)=V-K e^{\frac{-1}{RC}t}$ → $V_{0}=V-K$ → $K=V-V_{0}$
$V_{C}(t)=V_{final}-(V_{final}-V_{0})e^{\frac{-1}{RC}t}$, siendo $V_{final}$ la tensión del capacitor cuando $t\to \infty$.
### Circuitos RL
$$I(t)=\frac{V}{R}-Ke^{\frac{-R}{L}t}$$

Si mi **condición inicial** es $I(t=0)=0 \Rightarrow K = \frac{V}{R} \Longrightarrow  I(t)=\frac{V}{R}(1-e^{\frac{-R}{L}t})$

![[Pasted image 20230905205808.png]]

Si mi **condición inicial es no nula** y $I(t=0)=I_{0} \Longrightarrow I_{L}(t)=\frac{V}{R}-(\frac{V}{R}-I_{0})e^{\frac{-R}{L}t}$, por lo que a tiempos muy largos $I(t\to \infty)=\frac{V}{R}$.
#### Obs
Si la *inductancia* estuvo conectada a una batería por mucho tiempo, entra en **corto**. A su vez, la corriente que fluye antes y después en la inductancia será la misma.
### Transitorios de segundo orden
En este caso vamos a trabajar con circuitos con capacitores e inductancias en simultáneo.
![[Pasted image 20230912202002.png]]
Siendo la ec. en la derecha la ecuación asociada al circuito parametrizada.  
Para resolverlo planteamos la solución general, tal que: $I_{L}(t)=I_{Lh}(t)+I_{p}$.
**Obs.** $\xi = \frac{\alpha}{\omega_{0}}$
> **Resumen: Circuito RLC en paralelo**
> Un circuito RLC en paralelo nos da la sig. EDO: $\frac{dI_{L}^{2}}{dT}+ \frac{1}{CR} \frac{dI_{L}}{dT} + \frac{I_{L}}{LC} = \frac{I}{LC}$
> $$\frac{dI_{L}^{2}}{dT}+2\xi \omega_{0}\frac{dI_{L}}{dT}+I_{L}\omega_{0}^{2}=I\omega_{0}^{2}$$
> $\alpha= \frac{1}{2RC}$, $\omega_{0}=\sqrt\frac{1}{LC}$ y $\xi=\frac{1}{2R}\sqrt{\frac{L}{C}}$
> $\xi<1:$ Sub-amortiguado → Raíces de la ec. complejas conjugadas
> $B_{12} = -\xi \omega_{0} \mp j \omega_{0}\sqrt{1-\xi^{2}}$
> ![[Pasted image 20230918160347.png|350]]
> $\xi=0:$ **Resistencia infinita** → **NO** hay pérdida de energia. La energia se va pasando de inductor a capacitor periódicamente.
> $\xi > 1 :$ Sobre amortiguado → Raíces de la ecuación reales distintas.
> $B_{12} = -\xi \omega_{0} \mp \omega_{0}\sqrt{\xi^{2}-1}$
> ![[Pasted image 20230918155626.png|200]]
> ![[Pasted image 20230918155644.png|200]]
> $\xi = 1:$ Amortiguamiento crítico → Raíces de la ec. reales e iguales.
> $B_{12} = -\xi \omega_{0}$
> ![[Pasted image 20230918155818.png|300]]

> **Resumen: Circuito RLC en serie**
> Un circuito RLC en serie nos da la sig. EDO: $\frac{d^{2}V_{c}}{dt}+ \frac{L}{R} \frac{dV_{c}}{dt}+ \frac{V_{c}}{LC} = \frac{V}{LC}$
> $$\frac{d^{2}V_{c}}{dt^{2}}+ 2\xi \omega_{0} \frac{dV_{c}}{dt}+ \omega_{0}^{2}V_{c} = \omega_{0}^{2}V$$
> Con $\omega_{0}= \frac{1}{\sqrt{LC}}$, $\alpha= \frac{R}{2L}$ y $\xi= \frac{R}{2}\sqrt{\frac{C}{L}}$ 
> $\xi < 1:$ Sub amortiguado
> ![[Pasted image 20230918164536.png|200]]
> ![[Pasted image 20230918164557.png|400]]
> $\xi > 1 :$ Sobre amortiguado → Raíces de la ec. reales
> ![[Pasted image 20230918164649.png|250]]
> ![[Pasted image 20230918164707.png|200]]

#### Gráficos para cada caso
![[Gráficos dependiendo de la amortiguación]]
Resumen para resolver transtorios:
Pasos
1) Planteo ecuaciones adecuadas al circuito, relacionando las tensiones/corrientes en el circuito. Recuerdo que despues de un tiempo muy largo, el capacitor actua como una llave abierta y se "conserva" ese $V_{c}$, y el inductor actúa como una "cable" y mantiene la corriente $I_{L}$.
2) Mediante las expresiones: $V_{c}= \frac{1}{C}\int I dt$ → $I=C \frac{dV_{c}}{dt}$, $V_{L}=L \frac{dI}{dt}$ → $I= \frac{1}{L}\int V_{L}$, podemos asociar tensiones/corrientes y plantear una EDO para esa variable que asociamos.
3) Una vez planteo la EDO, con los coefiecientes para cada orden los asocio a la forma general normalizada, donde de esto puedo deducir $\xi$. Sabiendo $\xi$, puedo decir si el circuito es, amortiguado, subamortiguado, etc.
4) Una vez se como será el comportamiento del circuito, utilizo los resultados para la EDO de Euler. Estos resultados acorde a la variable que use para la EDO.
5) Por último, con las respuestas, puedo despejar las ctes.

