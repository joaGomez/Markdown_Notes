Sean $D\subset\mathbb{R}^{n},n\geq2$ un dominio y $F:D\times\mathbb{R}\times\mathbb{R}^{k}\to\mathbb{R}, k>1$ una función continua. Una ecuación diferencial en derivadas parciales es tal que:
$$F(x_{1},x_{2},...,x_{n},u,\frac{\partial u}{\partial x_{1}},...,\frac{\partial u}{\partial x_{n}},\frac{\partial^{2} u}{\partial x_{1}^{2}},\frac{\partial^{2} u}{\partial x_{1}\partial x_{2}},...,\frac{\partial^{j} u}{\partial x_{1}^{l_{1}}...\partial x_{m}^{l_{m}}},...)=0$$
Donde se vincula una función $u$ con $k$ de sus derivadas.

**Def.** La ecuación diferencial es *lineal* si $F$ es lineal respecto de $u$ y todas sus derivadas.

**Def.** La ecuación diferencial es *homogénea* si es lineal y si en todo término de $F$ aparece ya sea $u$ o alguna de sus derivadas.

**Def.** Una función $u=u(x_{1},...,x_{n})$ es solución de la ecuación en el dominio $D$, si en él admite las derivadas que aparecen en $F$, si $u$ y esas derivadas son continuas en $D$ y si allí se verifica idénticamente la ecuación diferencial.

**Obs.** Para poder obtener unicidad en la solución, debemos suponer que $u$ o sus derivadas asumen valores específicos en el borde del dominio $D$. En el caso en que una de las variables independientes sea el tiempo, una parte de ese borde será la (hiper)superficie $t=0$.

### Ecuaciones diferenciales en derivadas parciales de segundo orden
Las ecuaciones diferenciales en derivadas parciales de segundo orden son de la forma:
$$F(x_{1},x_{2},...,x_{n},u,\frac{\partial u}{\partial x_{1}},...,\frac{\partial u}{\partial x_{n}},\frac{\partial^{2} u}{\partial x_{1}^{2}},\frac{\partial^{2} u}{\partial x_{1}\partial x_{2}},...,\frac{\partial^{2} u}{\partial x_{n-1}\partial x_{n}})=0$$
Trataremos las ecuaciones lineales, que se escribirán de la forma:
$$\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}a_{ij}(x_{1},...,x_{n}) \frac{\partial^{2}u}{\partial x_{i}x_{j}}+\sum\limits_{k=1}^{n}b_{k}(x_{1},...,x_{n}) \frac{\partial u}{\partial x_{k}}+c(x_{1},...,x_{n})u=d(x_{1},...,x_{n})$$
**Obs.** Es la ecuación en forma canónica si $a_{ij}=0$ en $D$ si $i\neq j$.

**Def.** Sea la ec. en la forma canónica 
$$\sum\limits_{i=1}^{n}a_{ii}(x_{1},...,x_{n}) \frac{\partial^{2}u}{\partial x_{i}^{2}}+\sum\limits_{k=1}^{n}b_{k}(x_{1},...,x_{n}) \frac{\partial u}{\partial x_{k}} + c(x_{1},...,x_{n})u=d(x_{1},...,x_{n})$$
entonces:
- Será *elíptica* si $\forall ~~1\leq i\leq n$, y para todo $(x_{1},...,x_{n})$ en $D,~a_{ii}(x_{1},...,x_{n})\neq 0$ y además todos tienen el mismo signo.
- Será *parabólica* si existe $i^{*}$ tal que:
	- Para todo $(x_{1},...,x_{n})$ en $D, ~ a_{i^{*}i^{*}}(x_{1},...,x_{n})=0$ y $b_{i^{*}}(x_{1},...,x_{n})\neq 0$.
	- Para todo $1\leq i \neq i^{*} \leq n$, y para todo $(x_{1},...,x_{n})$ en $D$, $a_{ii}(x_{1},...,x_{n})\neq 0$ y además todos tienen el mismo signo.
- Será *hiperbólica* si $\forall~~ 1\leq i \leq n$, y para todo $(x_{1},...,x_{n})$ en $D,~ a_{ii}(x_{1},...,x_{n})\neq 0$ y $\exists ~~ i^{*}$ tal que para todo $(x_{1},...,x_{n})$ en $D$, $signo(a_{i^{*}i^{*}}(x_{1},...,x_{n}))\neq signo(a_{ii}(x_{1},...,x_{n}))$ cualquiera sea $1\leq i\neq i^{*}\leq n$.

Ejemplos.
**Ecuación de onda** → Hipebólica
$$\sum\limits_{i=1}^{n-1} \frac{\partial^{2} u}{\partial x_{i}^{2}}-\frac{\partial^{2} u}{\partial x_{n}^{2}}=0$$
**Ecuación de Poisson** → Elíptica
$$\sum\limits_{i=1}^{n} \frac{\partial^{2} u}{\partial x_{i}^{2}}=d(x_{1},...,x_{n})$$
**Ecuación de difusión** → Parabólica
$$\sum\limits_{i=1}^{n-1} \frac{\partial^{2} u}{\partial x_{i}^{2}}-\frac{\partial u}{\partial x_{n}}=0$$
### Aplicaciones de la transformada de Fourier a las ecuaciones diferenciales en derivadas parciales
La Transformada de Fourier se puede aplicar para resolver ecuaciones diferencial no se transforma), con condiciones iniciales. Una vez resuelta esta, la solución $u(x, t) (u(x, y))$ se obtiene a partir de la antitransformada de Foues en derivadas parciales con el procedimiento que mostraremos a continuación. La idea consiste en aplicar una transformada a $u(x, t)~ (u(x, y))$ de forma tal que como resultado de transformar ambos miembros de la ecuación y de las condiciones de borde, quede una ecuación diferencial ordinaria (en la variable sobre la que no se transforma).
![[Pasted image 20231106084755.png|550]]
![[Pasted image 20231106084812.png|500]]
### La ecuación de difusión unidimensional en una región no acotada
![[Pasted image 20231106085205.png]]
### La ecuación de la onda unidimensional para el espacio libre
![[Pasted image 20231106085334.png]]
![[Pasted image 20231106085319.png]]
### Problema del potencial en regiones no acotadas
Para tratar el problema del potencial, tanto la ec. de Laplace como la de Poisson, asumiremos que $\mathcal{F}[\frac{\partial u}{\partial y}(x,y)](f)=\frac{\partial u}{\partial y} (f,y)$, y que $\mathcal{F}[\frac{\partial^{2} u}{\partial y^{2}}(x,y)](f)=\frac{\partial^{2} u}{\partial y^{2}} (f,y)$.
![[Pasted image 20231106091751.png]]
