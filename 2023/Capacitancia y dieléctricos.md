---

---
La capacitancia $C$ de un capacitor se define como la razón de la magnitud de una carga cualquiera de los conuctores a la magnitud de la diferencia de potencial entre dichos conductores:
$$C \equiv \frac{Q}{\Delta V}, \qquad C>0$$
La capacitancia de un capacitor va a depender de la carga de los conductores, del potencial eléctrico entre estos, y de su geometría, que esta relacionada proporcionalmente a estos conceptos.
#### Capacitor cilíndrico
![[Pasted image 20230910162147.png|300]]
#### Capacitor plano
Un capacitor plano está hecho con dos placas conductoras, con cargas de igual magnitud y signo opuesto, por lo que el campo eléctrico entre las placas será: $E=\frac{\sigma}{\epsilon_{0}}=\frac{Q}{\epsilon_{0}A}$. Ya que el campo entre las placas es uniforme, la magnitud de la diferencia de potencial entre las placas es: $\Delta V = Ed = \frac{Qd}{\epsilon_{0}A}$.
Y como $C=\frac{Q}{\Delta V}$ → $C=\frac{\epsilon_{0}A}{d}$.
#### Capacitor esférico
![[Pasted image 20230910164956.png|300]]
#### Capacitores en paralelo
Para este tipo de conexiones de capacitores, se cumplen las siguientes prop.:
$$\begin{split}
& \Delta V = \Delta V_{1} = \Delta V_{2} \\
& C = C_{1} + C_{2} \\
& Q_{total}=Q_{1}+Q_{2} = C_{1}\Delta V_{1} + C_{2}\Delta V_{2} = \Delta V (C_{1}+C_{2}) = C~\Delta V
\end{split}$$

#### Capacitores en serie
Para este tipo de conexiones de capacitores, se cumplen las siguientes prop.:
$$\begin{split}
& Q = Q_{1}=Q_{2} \\
& \frac{1}{C} = \frac{1}{C_{1}}+\frac{1}{C_{2}} \\
& \Delta V = \Delta V_{1} + \Delta V_{2} = \frac{Q_{1}}{C_{1}} + \frac{Q_{2}}{C_{2}} = Q \left(\frac{1}{C_{1}}+\frac{1}{C_{2}}\right)= \frac{Q}{C}
\end{split}$$
### Energía almacenada en un capacitor
Sea $W = \Delta U_{E}$ → $dW = \Delta V ~ dq = \frac{q}{C}dq$, por lo que el trabajo invertido es: $W=\frac{Q^{2}}{2C}$, y la energía almacenada en el capacitor es: $U_{E}=\frac{Q^{2}}{2C}=\frac{1}{2}Q \Delta V=\frac{1}{2}C(\Delta V)^{2}$
Aunque el trabajo invertido y la energía almacenada también dependerá de la geometría del capacitor, por lo que es importante trabajar con la densidad de energía:
$$u_{E}=\frac{1}{2}\epsilon_{0}E^{2} \to W=U_{E}=\int_{S}u_{E}.ds$$
### Capacitores con material dieléctrico
Un dieléctrico es un material no conductor el cual tiene una cte dieléctrica adimensional $k >1$ que dependerá del material y mejora en ciertos aspectos a un capacitor sin dieléctrico.
$$\begin{split}
& \Delta V = \frac{\Delta V_{0}}{k} \\
& C=k~C_{0} \\
& Q = k ~ Q_{0}
\end{split}$$

Mediante el agregado de un dieléctrico entre las placas de un capacitor parece posible obtener un capacitor muy grande al reducir $d$, pero en la práctica se ve que hay un límite para esto, ya que puede haber una descarga eléctrica que puede presentarse por el medio dieléctrico que separa las placas. Para cualquier separación $d$, el voltaje máximo que puede aplicarse a un capacitor sin causar una descarga depende la **resistencia dieléctrica (Campo eléctrico máximo)**
### Dipolo eléctrico en un campo eléctrico
El *momento del dipolo eléctrico* está definido por el vector $\vec{p}$ dirigido desde $-q$ hasta $+q$, y con una magnitud $p \equiv 2aq$.
El **momento de torsión** está expresado como: $\vec{\tau} = \vec{p}\times \vec{E}$.

El trabajo requerido para girar el dipolo será: $dW=\tau d\theta$ → $U_{E}=-\vec{p}.\vec{E}$.

#### Obs de los materiales dieléctricos
Ya que la nclusión de un dieléctrico modifica el potencial entre las placas tambén modificará el campo eléctrico → $E=\frac{E_{0}}{k}$
El campo eléctrico debido a las placas está dirigido a la derecha, lo cual polariza al dieléctrico. El efecto neto sobre el dieléctrico es la formación de una densidad de carga superficial positiva $\sigma_{ind}$ sobre la cara izquierda. Por lo que se origina un campo eléctrico inducido $\vec{E}_{ind}$, con drección opuesta al campo externo $\vec{E}_{0}$, por lo que el campo eléctrico en el dieléctrico será:
$$E=E_{0}-E_{ind}$$
Y addemás:
$$\sigma_{ind}=(\frac{k-1}{k})\sigma$$

### Energía
- Si está conectado a una batería → $U=k U_{0}$ (*Cambia la carga dentro del capacitor*)
- Si *NO* está conectado a una batería → $U=\frac{U_{0}}{k}$ (*Cambia la tensión del capacitor*)
##### Obs
![[Pasted image 20230911081855.png|400]]
Cuando tengo un capacitor, cuyo dieléctrico esta delimitado de alguna forma horzontalmente, lo puedo pensar como un conjunto de capcaitores en paralelo. Éstos pueden estar delimitados por varios dieléctricos, o por algunos y el aire, cuyo $k=1$.
![[Pasted image 20230911082215.png|300]]
Ahora, si el dieléctrico está delimitado verticalmente como en la imagen, lo puedo pensar como un conjunto de capacitores en serie.

### Circuitos RC
- **Carga de un capacitor:**
Sabiendo que $q(t=0)=0$ y $I(t=0)= \varepsilon /R$, entonces a lo largo del tiempo:
$$\begin{split}
& q(t)=c\varepsilon (1-e^{\frac{-t}{RC}})=Q_{max}\left(1-e^{\frac{-t}{RC}}\right)\\
& i(t) = \frac{\varepsilon}{R}e^{\frac{-t}{RC}}
\end{split}$$
- **Descarga de un capacitor:**
Ahora, $q(t=0)=Q_{i}$, y cuando el capacitor ya no esté conectado a la batería se comenzará a descargar:
$$\begin{split}
& q(t)= Q_{i}e^{\frac{-t}{RC}} \\
& i(t)=\frac{-Q_{i}}{RC}e^{\frac{-t}{RC}}
\end{split}$$

