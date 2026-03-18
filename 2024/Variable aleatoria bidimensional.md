#### Discretas
Sean $X,Y$ dos variables aleatorias discretas. Su comportamiento puede ser descripto por la **función de probabilidad conjunta**.
$$p_{X,Y}(x,y)=P(X=x, Y=y) \qquad x\in R_{X}, y\in R_{Y}$$
Las funciones de probabilidad marginales pueden ser obtenidas como:
$$\begin{split}

	p_{X}(x) = P(X=x)= \sum\limits_{y\in R_{Y}}p_{X,Y}(x,y) \qquad x\in R_{X} \\
	p_{Y}(y) = P(Y=y)= \sum\limits_{x\in R_{X}}p_{X,Y}(x,y) \qquad y\in R_{Y}
\end{split}$$
**Obs:** Las variables aleatorias son independientes si:
$$p_{X,Y}(x,y)=p_{X}(x)p_{Y}(y) \qquad x\in R_{X},y\in R_{Y}$$
El valor esperado de una función $h$ de ambas variables aleatorias ($h:\mathbb{R}^{2}\to\mathbb{R}$) viene dado por:
$$E[h(X,Y)]=\sum\limits_{x\in R_{X}, y\in R_{Y}}h(x,y)p_{X,Y}(x,y)=\sum\limits_{x\in R_{X}}\sum\limits_{y\in R_{Y}}h(x,y)p_{X,Y}(x,y)$$
Sean dos funciones $k,m:\mathbb{R}\to \mathbb{R}$. Luego, si $X$ e $Y$ son independientes:
$$E[k(X)\cdot m(Y)]=E[k(X)]\cdot E[m(Y)]$$
#### Continuas
El comportamiento de dos variables aleatorias continuas $X$ e $Y$ es descrito por una **densidad de probabilidad conjunta** $f_{X,Y}: \mathbb{R}^{2}\to \mathbb{R_{\geq 0}}$. A partir de ésta, se pueden calcular todas las posibilidades relacionadas a ambas variables como:
$$P((X,Y)\in B)=\iint_{(x,y)\in B}f_{X,Y}(x,y)~dxdy \qquad B\subseteq\mathbb{R}^{2}$$
La densidad de las probabilidades marginales es tal que:
$$f_{X}=\int_\mathbb{R}f_{X,Y}(x,y)~dy \qquad f_{Y}=\int_\mathbb{R}f_{X,Y}(x,y)~dx$$
Si éstas son independientes $\to f_{X,Y}(x,y)=f_{X}(x)\cdot f_{Y}(y)$.

El valor esperado de una función $h$ de ambas variables aleatorias ($h:\mathbb{R}^{2}\to\mathbb{R}$) viene dado por:
$$E[h(X,Y)]=\iint_{\mathbb{R}^{2}} h(x,y)f_{X,Y}(x,y)$$
Sean dos funciones $k,m:\mathbb{R}\to \mathbb{R}$. Luego, si $X$ e $Y$ son independientes:
$$E[k(X)\cdot m(Y)]=E[k(X)]\cdot E[m(Y)]$$
La covarianza de dos variables aleatorias está definida por:
$$Cov[X,Y]=E[X\cdot Y]- E[X]\cdot E[Y]$$
El coeficiente de correlación de dos variables aleatorias está definido como:
$$\rho (X,Y)= \frac{Cov[X,Y]}{\sqrt{Var[X]\cdot Var[Y]}}$$
Sean $X$ e $Y$ dos variables aleatorias, se cumple que:
$$E[X+Y]=E[X]+E[Y] \qquad E[(X+Y)^{2}]=E[X^{2}]+2\cdot E[X\cdot Y]+E[Y^{2}]$$
La varianza está dada por: $Var[X+Y]=Var[X]+2\cdot Cov[X,Y]+Var[Y]$. Pero si $X$ e $Y$ son independientes $\to Var[X+Y]=Var[X]+Var[Y]$.

**Caso práctico:**
$$\begin{align*}
P(X+Y=z)&= \sum\limits_{x\in R_{X},~y\in R_{Y}: x+y=z} p_{X,Y}(x,y) \\
\textbf{Independencia} \qquad &= \sum\limits_{x\in R_{X}}p_{X}(x)p_{Y}(z-x) = \sum\limits_{x\in R_{Y}}p_{X}(z-y)p_{Y}(y) 
\end{align*}$$
Para variables aleatorias continuas:
$$P(X+Y=z)=\int_\mathbb{R}f_{X}(x)f_{Y}(z-x)dx=\int_\mathbb{R}f_{X}(z-y)f_{Y}(y)dy$$
#### Distribuciones condicionales
##### Discreta
$$p_{X|Y}(x|y)=P(X=x|Y=y)=\frac{p_{X,Y}(x,y)}{p_{Y}(y)}$$
##### Continua
$$f_{X|Y}(x|y)=\frac{f_{X,Y}(x,y)}{f_{Y}(y)}$$
