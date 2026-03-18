----
En este caso analizaremos circuitos con frecuencia variable.
### Circuito resistivo
Solo en este caso el circuito parecerá no variar, ya que la impedancia solo dependerá de la resistencia y está no tiene relación con la frecuencia del circuito.
#### Obs
En todo otro caso, el cambio de frecuencias en un circuito si que tendrá implicaciones ya que modificará nuestra impedancia del circuito, ya que en este hay componentes como bobinas, capacitores, que tienen relación directa y expresiones relacionadas con la frecuencia del circuito. Visulamente, podemos ver esta correlación con la frecuencia:
![[Pasted image 20230922095337.png|300]]
### Def
Se define el estado de resonancia, $\omega_{0}=$ frecuencia de resonancia, tal que $Im(z)=0$.
#### Obs
Por lo que en un circuito RLC Serie, tendríamos lo siguiente:
- $|z|=\sqrt{R^{2}+(\omega L - \frac{1}{\omega C})^{2}}$
- $\varphi = arctg(\frac{\omega L - \frac{1}{\omega C}}{R})$
Por lo que obtenemos, la siguiente expresión para la impedancia del circuito: $z= |z| ~ \angle ~ \varphi$
![[Pasted image 20230922100555.png|500]]
### Props.
- Circuito capacitivo: $\omega < \omega_{0} \Rightarrow \frac{1}{\omega C} > \omega L$
- Circuito inductivo: $\omega > \omega_{0} \Rightarrow \frac{1}{\omega C} < \omega L$
#### Obs
![[Pasted image 20230922101019.png|350]]
### Ancho de banda
Se define como $B=\omega_{2} - \omega_{1}$, y **NO** necesariamente debe estar centrado en $\omega_{0}$. *Si es débilmente amortiguado → **SI** ($Q \geq 10$)*.
#### Obs
Otras fórmulas obtenidas del RLC Serie:
- $\omega_{0}^{2}=\omega_{1}.\omega_{2}$
- $B=\omega_{2}-\omega_{1}= \frac{R}{L}$
### Factor de calidad Q
$$\frac{Potencia ~Q ~(\omega_{0})}{Potencia ~P ~(\omega_{0})}=Q$$
Además, las potencias del capacitor y del inductor en resonancia, son iguales, es decir, almacenan la misma energía.
$$I^{2}X_{L}=I^{2}X_{C} \to I^{2}\omega_{0}L=I^{2} \frac{1}{\omega_{0}C}$$
Debido a esto, para RLC Serie, $Q=\frac{\omega_{0}}{B}$
##### Obs
Si $Q \geq 10$ → $\omega_{1}\cong \omega_{0}-\frac{B}{2}$ y $\omega_{2}\cong \omega_{0}+\frac{B}{2}$, por lo que B quedó centrado en $\omega_{0}$
### RLC Paralelo
![[Pasted image 20230925110127.png|200]]
En este caso, definimos la admitancia: $Y= \frac{1}{Z}$ → $\omega_{0}= \frac{1}{\sqrt{LC}}$
![[Pasted image 20230925110109.png|200]]
Y obtenemos que, $Q=\omega_{0}CR$ y $B= \frac{1}{RC}$, que se comporta de la siguiente manera:
![[Pasted image 20230925110258.png|350]]
