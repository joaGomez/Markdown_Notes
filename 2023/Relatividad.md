### Contracción de Lorentz
$$L=L_{0}\sqrt{1- \frac{V^{2}}{C^{2}}}$$
Siendo $L_{0}$ la longitud propia. Ésta es siempre mayor que la impropia. Los cuerpos en movimiento se ven contraídos.

### Teoría de la relatividad especial
Sus postulados son:
- La velocdad de la luz en el vacío es una cte. universal por lo tanto resulta independiente tanto de la velocidad de la fuente como del observador.
- Las leyes de la física son independientes del sistema de referencia inercial desde el que se las describa.
**Obs.** Se define el **tiempo propio** como $\Delta \tau = \Delta t' \sqrt{1 - \frac{V^{2}}{C^{2}}}$. Un intervalo de tiempo propio entre dos eventos es siempre más pequeño que uno impropio.

### Transformaciones de Lorentz
Las hipótesis de partida son:
- Los orígenes espaciotemporales de ambos sistemas están superpuestos.
- El movimiento entre ambos sistemas se da en dirección del eje x.

|             Directa             |             Inversa              |
|:-------------------------------:|:--------------------------------:|
|       $x'=\gamma (x-Vt)$        |       $x=\gamma (x'+Vt')$        |
|             $y'=y$              |              $y=y'$              |
|             $z'=z$              |              $z=z'$              |
| $t'=\gamma(\frac{t-Vx}{x^{2}})$ | $t=\gamma(\frac{t'+Vx'}{c^{2}})$ |

Donde $\gamma= \frac{1}{\sqrt{1-\frac{V^{2}}{c^{2}}}}$. Notar que $\gamma \geq 1$.

Dados dos eventos $E_{1}= (t_{1},x_{1},y_{1},z_{1})$ y $E_{2}= (t_{2},x_{2},y_{2},z_{2})$, estos serán **simultáneos** si $t_{1}=t_{2}$. Por otro lado, serán **coincidentes** si $(x_{1},y_{1},z_{1})=(x_{2},y_{2},z_{2})$. Y **superpuestos** si son tanto coincidentes como simultáneos.

### Contracción de Lorentz
Para poder medir la longitud de la barra desde el sistema S, necesito considerar eventos simultáneos.
Tengo $E_{1}$ y $E_{2}$, ambos en tiempo $t$ → $x_{2}^{'}-x_{1}^{'}=L_{0}=\gamma(x_{2}-x_{1})=\gamma L$
![[Pasted image 20231025183434.png|200]]
### Dilatación temporal
El tiempo propio es el intervalo temporal entre eventos coincidentes → $t_{2}^{'}-t_{1}^{'}=\gamma(t_{2}-t_{1})=\gamma \Delta\tau$

### Efecto Doppler relativista
Teniendo en cuenta que $f=\frac{1}{t}$ → En un marco donde la fuente se mueve a una velocidad $V$:
![[Pasted image 20231029105705.png|200]]
El período por definición será siempre un tiempo propio → $\lambda_{obs}=c\Delta t +V\Delta t=\Delta t(c+V)$, entonces obtenemos que:
$$\frac{1}{\tau'}=\frac{c}{\lambda_{obs}}\sqrt{\frac{c+V}{c-V}} \Rightarrow f'_{emisor}=f_{obs}\sqrt{\frac{c+V}{c-V}}$$
### Transformación en velocidades
$$\begin{split}
& u'_{x}= \frac{u_{x}-V}{1-\frac{Vu_{x}}{c^{2}}}\\
& u'_{y}= \frac{u_{y}}{\gamma(1-\frac{Vu_{x}}{c^{2}})}\\
& u'_{z}= \frac{u_{z}}{\gamma(1-\frac{Vu_{x}}{c^{2}})}
\end{split}$$
### Cantidad de movimiento
Se define la cantidad de movmiento relativista como:
$$p=m_{0}\gamma(u)u=\frac{mu}{\sqrt{1- \frac{u^{2}}{c^{2}}}}$$
Donde $u$ es la velocidad de una partícula y $v$ será la velocidad relativa en SRI.
Esta magnitud se transforma de la siguiente manera:
$$\begin{cases}
p'_{x}= \gamma(v)(p_{x}-m_{0}\gamma(u)v) \\
p'_{y}=p_{y} \\
p'_{z}=p_{z}
\end{cases}$$
**Obs.** Se puede recuperar la forma clásica de la cantidad de movimiento llamando:
$$m=\gamma(u)m_{0}=\frac{m_{0}}{\sqrt{1- \frac{u^{2}}{c^{2}}}}$$
Siendo $m_{0}$ la *masa en reposo* de la partícula y $m$ la *masa relativista*.
### Energía
Se define la energía relativista de una partícula como:
$$\oint_{A}^{B}dW=K=mc^{2}-m_{0}c^{2}$$
De esta ecuación se obtiene la expresión: $E=mc^{2}$. Y podemos deducir que una partícula en reposo y totalmente aislada tiene energía no nula $E_{0}=m_{0}c^{2}$ (*Energía en reposo*).

Por lo tanto, la energía puede escribirse como:
$$E=K+m_{0}c^{2}$$
$$E{^2}=p^{2}c^{2}+m_{0}^{2}c^{4}$$
### Fuerza
La expresión para la fuerza es:
$$F=\frac{F.u}{c^{2}}u+ma$$
Ésta será aplicada a los casos donde actúa la fuerza de Lorentz. Si solo tenemos fuerza magnética → $F=ma$, pero con la masa relativista.

> El fotón:
> - Partícula que se mueve a la velocidad de la luz → Su masa en reposo es 0 ($m_{0}=0$).
> - Su energía es tal que $E=p~c$
> - Su carga eléctrica es 0.

### Observaciones
- Desde un observador en reposo con respecto a un objeto, a mayor velocidad que vaya este objeto, más contraído lo veré.
- Para un observador en reposo con repecto a un objeto que se mueve a velocidades relativas a la velocidad de la luz, el tiempo pasará más rápido.
- Mientras mayor sea la velocidad de la partícula → Más grande será su masa relativista.