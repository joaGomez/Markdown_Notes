Una función de una variable aleatoria es una variable aleatoria ($Y$) compuesta de otra variable aleatoria ($X$).

Por ejemplo, tengo una variable aleatoria $V\sim N(0,1)$, y otra variable aleatoria $W= \frac{V^{2}}{R}$, siendo $R$ una cte.
Si quiero hallar la función de densidad de probabilidad de $V$, puedo arrancar por la función de distribución acumulada:
$$F_{W}(w)=P(W\leq w)=P(\frac{V^{2}}{R}\leq w)=P(V\leq \sqrt{w\cdot R})=F_{Y}(\sqrt{w\cdot R})$$
De esta forma ya conocemos $F_{W}(w)$, teniendo en cuenta los intervalor para cada $w$, y además podemos conocer la función de densidad de probabilidad, tal que $f_{W}(w)= \frac{dF_{W}(w)}{dw}$.

#### Transformaciones útiles
Si tengo dos variables aleatorias $Y, X$, tal que $Y=a\cdot X + b$:
- $\mu_{Y}=a\cdot \mu_{X}+b$
- $\sigma_{Y}^{2}=a^{2}\cdot \sigma_{X}^{2} \rightarrow \sigma_{Y}=|a|\cdot \sigma_{X}$
- $\gamma_{Y}= sign(a)\cdot \gamma_{X}$
- $K_{Y}=K_{X}$
