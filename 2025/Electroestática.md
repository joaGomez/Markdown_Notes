**Definición:** Campos constantes en el tiempo (independiente del tiempo).
$$
\text{Carga eléctrica:} \qquad q_{e = -1.6\cdot 10{^{-19}}C}
$$
Donde $1C = 1 A.s = 6.241509 \cdot 10^{18}\cdot q_{e}$
### Ley de Coulomb
La ley de Coulomb establece la fuerza ejercida por la carga puntual $q_{a}$ sobre la carga puntual $q_{b}:$
$$
\vec{F}_{AB} = k\cdot \frac{q_{a}q_{b}}{|\vec{r}_{B}-\vec{r}_{A}|^{3}} (\vec{r}_{B}-\vec{r}_{A})
$$
Donde $\varepsilon_{0}=8.85\cdot 10^{-12} \frac{F}{m}$ es la permitividad del vacío, y $k = \frac{1}{4\pi \varepsilon_{0}}=8.991\cdot 10^{9} \frac{Nm^{2}}{C^{2}}$ es la cte. de Coulomb.

**Obs:** La ley de Coulomb es válida solo para cargas puntuales, y en condiciones estacionarias o con movimiento lento y rectilíneo uniforme.
#### Principio de superposición
La fuerza neta ejercida sobre una carga es la suma vectorial de las fuerzas individuales ejercidas sobre dicha carga por cada una de las cargas del sistema.
$$
\vec{F}_{total} = \sum_{i=1}^{N}\vec{F}_{i} = \sum_{i=1}^{N} k\cdot \frac{q_{i}q_{0}}{|\vec{r}_{i}-\vec{r}_{0}|^{3}} (\vec{r}_{i}-\vec{r}_{0})
$$
### Campo eléctrico
Se define el concepto de campo eléctrico, como el campo que vería una carga en un punto, por las demas cargas en el sistema. Matemáticamente, esto se consigue a partir de dividir la fuerza de Coulomb por la carga, cuya posición es el punto donde quiero calcular el campo eléctrico. Es decir, el concepto nace de ver que campo generan las cargas de un sistema en una carga en un punto específico.
$$
\vec{E}(P) = \lim_{ q_{B} \to 0 } \frac{\vec{F}}{q_{B}} \Longrightarrow \vec{E}(\vec{r}) = k \frac{q_{A}}{|\vec{r}-\vec{r}_{A}|^{3}}(\vec{r}-\vec{r}_{A}) 
$$
Donde $[E] = \frac{N}{C}$.

**Obs:** En un sistema de cargas, se aplica nuevamente el principio de superposición.
$$
\vec{E}_{total}=\sum_{i=1}^{N} \vec{E}_{i} = \sum_{i=1}^{N} k \frac{q_{i}}{|\vec{r}-\vec{r}_{i}|^{3}}(\vec{r}-\vec{r}_{i})
$$
#### Densidades de carga
Dependiendo de la forma de la distribución, se definen las siguientes distribuciones de carga (campo escalar):

![[Pasted image 20250806224750.png#center|500]]

#### Campo de una distribución de carga
Para un objeto con distribución continua de carga volumétrica, el diferencial de campo estará dada por:
$$
dE\bigg{|}_{P} = \frac{1}{4\pi\varepsilon_{0}} \frac{dq'(r-r')}{|r-r'|^{3}} = \frac{1}{4\pi\varepsilon_{0}} \frac{\rho ~dv'(r-r')}{|r-r'|^{3}}
$$
Aplicando el principio de superposición:
$$
\vec{E}(\vec{r}) = \int_{\tau}  \, d\vec{E} \Longrightarrow \vec{E}(\vec{r}) = \frac{1}{4\pi \varepsilon_{0}}\int_{\tau} \frac{\rho(\vec{r}')}{|\vec{r}-\vec{r}'|^{3}} (\vec{r}-\vec{r}') \, dv' 
$$
Para una distribución de carga en superficie $dq'=\rho_{s}~d\vec{S}:$
$$
\vec{E}(\vec{r}) = \frac{1}{4\pi \varepsilon_{0}}\int_{S} \frac{\rho_{s}(\vec{r}')}{|\vec{r}-\vec{r}'|^{3}} (\vec{r}-\vec{r}') \, dS' 
$$
### Ley de Gauss
Dado una objeto con densidad de carga $dq'$, aplicando una superficie gaussiana conveniente, el flujo del campo eléctrico generado por el objeto será:
$$
\phi= ∯_{S}\vec{E}.d\vec{S} = \frac{Q_{enc}}{\varepsilon_{0}}
$$
**Observaciones:**
- La ley de Gauss simplifica los cálculos de campo eléctrico en casos de alta simtría.
- La ley de Gauss es una consecuencia directa de la ley de Coulomb → Válida para cargas puntuales, en reposo o similar.
##### Caso particular: Simetría esférica
- El campo es independiente de $\theta$ y $\varphi$ → $\phi=∯_{s}\vec{E}.d\vec{S}=\int_{r_{a}}^{r_{b}}E\cdot 4\pi r^{2} \, dr$
- Las componentes de $\hat{\theta}$ y $\hat{\varphi}$ se anulan → $\vec{E}(\vec{r})=E_{r}(r)\hat{r}$

El resultado a partir de estas dos consecuencias será:
$$
\vec{E}(r)= \frac{Q}{4\pi \varepsilon_{0}r^{2}}\hat{r}
$$
#### Forma diferencial
A partir del teorema de la divergencia y la expresión para la carga encerrada por un objeto:
$$
∯_{S} \vec{E}.d\vec{S} = \iiint_{V} (\nabla.\vec{E}) ~ dv
\qquad \qquad Q_{enc} = \iiint_{V} \rho ~ dv
$$
Por lo tanto, reemplazando estas expresiones en la ley de Gauss:
$$
\iiint_{V} (\nabla.\vec{E}) ~ dv = \frac{1}{\varepsilon_{0}}\iiint_{V}\rho ~ dv \Longrightarrow \iiint_{V} \left( \nabla.\vec{E} - \frac{\rho}{\varepsilon_{0}} \right) ~ dv = 0
$$
Por lo tanto, queda la siguiente expresión:
$$
\text{Primera ecuación de Maxwell}  \qquad \nabla.\vec{E} = \frac{\rho}{\varepsilon_{0}}
$$
### Potencial electroestático
En una curva cerrada:
$$
\oint\vec{E}.d\vec{l}=0
$$
Por el teorema de Stokes $\oint_{c}\vec{E},d\vec{l}=\iint_{s}(\nabla \times \vec{E}).d\vec{S}=0$. Por lo tanto, para el caso electroestático, se cumple que:
$$
\nabla \times \vec{E} = 0
$$
**Propiedades:**
- La intensidad de campo eléctrico $E$ es conservativa (no hay disipación de energía).
- Es un caso particular (caso estacionario) de la tercer ecuación de Maxwell.

De la tercer ec. de Maxwell, para el caso estacionario: $\nabla \times \vec{E} = 0$. Existe una función potencial $V(r)$, tal que:
$$
\vec{E}=-\nabla ~ V(\vec{r})
$$
El potencial en un punto r está dado por:
$$
V(\vec{r}) = - \int_{\infty}^{r} \vec{E}.d\vec{l} \Rightarrow V = -\int E(r) \, dr + cte
$$
Se elige la cte arbitrariamente para decidir donde queremos el cero de potencial.

![[Pasted image 20250807100016.png#center|400]]

#### Principio de superposición
Para el potencial es equivalente la aplicación del principio de superposición. En un sistema de cargas, el potencial total será:
$$
V_{total} = \sum_{i}V_{i} = \frac{1}{4\pi\varepsilon_{0}}\sum_{i} \frac{q_{i}}{|\vec{r}-\vec{r}_{i}|}
$$
Para el caso de un objeto con densidad de carga continua:
$$
V(\vec{r})= \frac{1}{4\pi\varepsilon_{0}} \int_{\tau} \frac{\rho (\vec{r}')}{|\vec{r}-\vec{r}_{i}|} \, dv'
$$
