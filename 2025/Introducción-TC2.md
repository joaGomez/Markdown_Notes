**Obs:** Una mala fuente de tensión, es una buena fuente de corriente y viceversa. Lo podemos visualizar con la relación de los circuitos equivalentes de Thevenin y Norton.

![[Pasted image 20240801105135.png#center|500]]

![[Pasted image 20240801105246.png#center|350]]

Para cualquier valor de $V_{T}$ puedo hallar la impedancia. Es más cómodo trabajar con $V_{T}=0$, por lo que esa es la razón por la que se pasivan las fuentes para calcular la impedancia correspondiente.

![[Pasted image 20240801161303.png#center|500]]

Puedo utilizar estos modelos (aunque estén superpuestos) de la siguiente forma:

![[Pasted image 20240801164334.png#center|500]]
#### Teorema de Miller
El circuito equivalente cuando la relación de tensión entre dos nodos puede expresarse por una constante $K$ es el siguiente:

![[Pasted image 20240801170014.png#center|400]]

Donde se cumple que:
$$\begin{split}
& V_{2}= K\cdot V_{1} \\
& Z_{1}= Z\cdot (1-K) \\
& Z_{2}= Z\cdot \left(1- \frac{1}{K}\right)
\end{split}$$ 
![[Pasted image 20240801170354.png#center|400]]
