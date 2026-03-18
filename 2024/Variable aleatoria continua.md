Sea $X$ una variable aleatoria continua $\leftrightarrow F_{X}$ es continua. Además, $F_{x}$ cumple las mismas propiedades que para el dominio discreto:
1. $\alpha \leq \beta \Rightarrow F_{X}(\alpha) \leq F_{X}(\beta)$.
2. $\lim_{\alpha\to -\infty}F_{X}(\alpha)=0$.
3. $\lim_{\alpha\to +\infty}F_{X}(\alpha)=1$.

Se define la densidad de probabilidad como $f_{x}(x)= \frac{dF_{X}(x)}{dx} \forall x\in \mathbb{R}$ donde $F_{X}$ sea derivable. 

### Propiedades
1. $\int_{-\infty}^{\infty}f_{x}(x)dx = 1$.
2. $f_{x}(x)\geq 0$.
3. $E(X) = \mu_{x} = \int_{-\infty}^{\infty}x\cdot f_{x}(x)dx$.
4. $Var(X) = \sigma_{x}^{2} = \int_{-\infty}^{\infty}(x-\mu_{x})^{2}\cdot f_{x}(x)dx$.
5. $P(X\leq x)=\int_{-\infty}^{x}f_{x}(x)dx=F_{X}(X=x)$.

### Notables
|         Tipos          |                                            $F_{X}(x)$                                             |                                       $f_{x}(x)$                                       |       $\mu_{x}$       |     $\sigma_{x}^{2}$     |
| :--------------------: | :-----------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------: | :-------------------: | :----------------------: |
|    $Uniforme(a,b)$     | $$\begin{split}&0\quad &x\leq a\\ &\frac{x-a}{b-a}\quad &a<x<b \\ &1 \quad &x\geq b \end{split}$$ | $$\begin{split}&\frac{1}{b-a} \quad &x\in(a,b) \\ &0\quad &x\notin (a,b) \end{split}$$ |   $$\frac{a+b}{2}$$   | $$\frac{(b-a)^{2}}{12}$$ |
| $Exponencial(\lambda)$ |          $$\begin{split}&0 \quad &x<0 \\ &1-e^{-\lambda x} \quad &x\geq 0 \end{split}$$           |    $$\begin{split}&0 \quad &x<0 \\ &\lambda e^{-\lambda x} \quad &x>0 \end{split}$$    | $$\frac{1}{\lambda}$$ |  $$\frac{1}{\lambda}$$   |
| $Z\sim N(\mu,\sigma)$  |                             $$\phi\left(\frac{x-\mu}{\sigma}\right)$$                             |                  $$\frac{1}{\sqrt{2\pi}}\cdot e^{-\frac{z^{2}}{2}}$$                   |        $$\mu$$        |        $$\sigma$$        |
Notar que la normal estándar surge de la gaussiana mediante el cambio de variable $z=\frac{x-\mu}{\sigma}$.

#### Propiedades de la normal estándar
- $\phi(z)=1-\phi(-z)$.
- $z=\phi^{-1}(\alpha)$.
- $\phi(-z_{\alpha})=1-\alpha \to z_{1-\alpha}=-z_{\alpha}$.

