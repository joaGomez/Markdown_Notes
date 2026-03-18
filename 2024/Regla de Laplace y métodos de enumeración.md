La regla de Laplace es muy útl para el cálculo de probabilidades cuando *todos los casos son igualmente probables*:
$$P(A)= \frac{\# \ casos\ favorables}{\# \ total \ de \ casos}$$

La combinatoria es una buena herramienta para calcular la cantidad de casos posibles como totales donde quiero distribuir $m$ cosas en $n$ espacios ($n > m$), sin importarme las permutaciones.
$$\binom{n}{m}=\frac{n!}{m!(n-m)!}$$
#### Métodos de enumeración
##### Permutaciones (interesa el orden)
- Si tenemos $n$ objetos diferentes, se pueden agrupar (permutar) en $nP_{n}=n!$ formas distintas.
- Si tenemos $n$ objetos diferentes y queremos escoger $r$ de esos objetos, $0 \leq r \leq n$, y permutamos el $r$ elegido → Hay $nP_{r}=V_{n,r}= \frac{n!}{(n-r)!}$
##### Combinaciones
Si tenemos $n$ objetos dferentes, y queremos contar el número de maneras como podemos escoger $r$ de esos objetos, sn considerar el orden → Hay $\binom{n}{r}= \frac{n!}{r!(n-r)!}$ posibilidades.
##### Permutaciones cuando no todos los objetos son diferentes
Si tenemos $n$ objetos tales que hay $n_{k}$ de $k$ clases distintas → El número de permutaciones de estos $n$ objetos está dado por:
$$P_{n}^{n_{1}n_{2}...n_{k}}= \frac{n!}{\prod_{i=1}^{k}n_{i}}$$
