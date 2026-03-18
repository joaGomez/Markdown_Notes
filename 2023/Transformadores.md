### Transformador ideal:
- Los devanados no tienen resistencias
- El acoplamiento es máximo $\to$ $k=1$
- La relación entre las tensiones es cte al igual que las corrientes:
$$n= \frac{N_{2}}{N_{1}}=\frac{V_{2}}{V_{1}}=\frac{I_{1}}{I_{2}}=\sqrt{\frac{L_{2}}{L_{1}}}$$
- La inductancia $L_{1}$ y $L_{2}$ son infinitamente grandes porque la permitividad es infinita: $L= \frac{N{^{2}}~*~\mu~*~A_{e}}{L_{e}}, \mu \to \infty$
![[Pasted image 20231114194052.png|300]]
$$V_{1}=n ~V_{2}$$
$$I_{1}=\frac{I_{2}}{n}$$
Y el circuito equivalente quedará tal que:
![[Pasted image 20231114194752.png|250]]
![[Pasted image 20231114194822.png|250]]
![[Pasted image 20231114194836.png|250]]
$L_{1}$ es **MUY** grande y es como si no estuviera. Además, $Z_{2}$ quedará del lado primario.
### Transformador no ideal
- Los devanados tienen resistencias, pero las "aislamos", para que nos quede un transformador ideal y por fuera una impedancia de entrada/salida.
![[Pasted image 20231114195543.png|300]]
Resolviendo el sistema:
$$\begin{split}
& V_{1}=I_{1}R_{1}+I_{1}j\omega L_{1}-I_{2}j\omega M \\
& -V_{2}=I_{2}R_{2}+I_{2}j\omega L_{2}-I_{1}j\omega M \\
\Rightarrow V_{1}-V_{2} = & I_{1}(R_{1}+j\omega(L_{1}-M))+I_{2}(R_{2}+j\omega(L_{2}-M))
\end{split}$$
De acuerdo con las siguientes expresiones, podemos generar el siguiente circuito (con una impedancia $Z_{0}$ desconocida):
![[Pasted image 20231114200147.png|400]]
Haciendo el siguiente truco, hallo la impedancia $Z_{0}$:
![[Pasted image 20231114200837.png|300]]
El problema con este modelo aparece si $M$ es mayor a $L_{1}$ o $L_2$. Por lo que utilizamos la relación de transformación $n= \frac{N_{1}}{N_{2}}$.

- Inductancia de dispersión primaria referida al primario: $L_{d1} = L_{1}(1-k)$
- Inductancia de dispersión secundaria referida al primario: $L_{d2}' = L_{2}'(1-k)$
- Inductancia de magnetización del primario: $L_{p}=L_{1}.k$

Por último, para considerar todos los parámetros del transformador no ideal → tenemos que tener en cuenta las corrientes parásitas del núcleo. En el circuito, esto lo representamos como una consuctancia $G_{0}$
![[Pasted image 20231122162928.png|350]]
El modelo final referido al primario será:
![[Pasted image 20231122162959.png|350]]
Con este modelo podemos insertar el transformador en cualquier circuito:
![[Pasted image 20231122163120.png|400]]
Para determinar los parámetros de este modelo tengo dos ensayos:
- Ensayo de vacío: Esto implica tensión para la que se diseño el transformador y secundario en circuito abierto.
![[Pasted image 20231122163349.png|400]]
Por lo que la caída de tensión de $Z_{eq}$ es despreciable → $Z_{0}= \frac{V}{I}$. La tensión y corriente están dadas por el voltímetro y el amperímetro. El vatímetro nos va a brindar con el desfasaje:
$$P_{0}=V I cos(\phi_{0}) \to \phi_{0}=cos^{-1}\left(\frac{P_{0}}{V I}\right)\Rightarrow Z_{0}=Z_{0}\angle \phi_{0}$$
- Ensayo de corto circuito: 
![[Pasted image 20231122163956.png|300]]
Por lo que nos queda el siguiente circuito equivalente:
![[Pasted image 20231122164025.png|200]]
En este esquema, regulamos la tensión de la fuente hasta que la corriente alcance el valor al que fue diseñado el transformador en plena carga:
$$Z_{eq}= \frac{V}{I} \to P_{cc}=VIcos(\phi_{cc})\to \phi_{cc}=cos^{-1}(\frac{P_{cc}}{VI}) \Rightarrow Z_{eq}=Z_{eq}\angle \phi_{cc}$$
