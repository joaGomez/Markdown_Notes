Dados dos sucesos $A, B$ con $P(B)>0$, la probabilidad de que suceda $A$ sabiendo que sucedió $B$, se conoce como **probabilidad condicional** y se define tal que:
$$P(A|B)= \frac{P(A\cap B)}{P(B)} \Rightarrow P(A\cap B)=P(A|B).P(B)=P(B|A).P(A)$$
Esta última relación dado el caso inverso, y como $P(A\cap B)=P(B\cap A)$ → Llegamos a esa expresión.
**Prop:** $P(A)=P(B).P(A|B)+P(B^{c}).P(A|B^{c})$

> **Obs:**
> ![[Pasted image 20240315185202.png#center|400]]
> ![[Pasted image 20240319094609.png|350]]
#### Sucesos independientes
Dos sucesos $A, B$ son **independientes** $\leftrightarrow$ $P(A\cap B)=P(A).P(B)$. Además, al ser independientes entre sí, tambiés se cumple que: $A,B{^{c}}$ ; $A{^{c}},B$ ; $A{^{c}}, B{^{c}}$ serán independientes entre sí.

**Prop:** Sean los sucesos $A_{1}, \ ... \ , A_{n}$ independientes $\Rightarrow$ $P(A_{1}\cap \ ... \ \cap A_{n})=P(A_{1})\cdot \ ...\ \cdot P(A_{n})$

**Prop:** Si $A$ y $B$ son sucesos independientes $\Rightarrow P(A|B)=P(A) \wedge P(B|A)=P(B)$.

Se define los sucesos $A_{1}, A_{2},...,A_{k}$ como una partcón del espacio muestral $S$ si:
- $A_{i}\neq \phi \quad i=1,...,k$
- $A_{i}\cap A_{j}=\phi \quad i\neq j \quad i,j \in [1,k]$
- $S= \bigcup\limits_{i=1}^{k}A_{i}$
##### Teorema de la probabilidad total
Sea $A_{1}, A_{2},...,A_{k}$ una partición del espacio muestral $S$, y $B$ un suceso cualquiera, entonces:
$$P(B)= \sum\limits_{i=1}^{k}P(B\cap A_{1})=\sum\limits_{i=1}^{k} P(B|A_{i})\cdot P(A_{i})$$
$$P(A_{i}|B)=\frac{P(B|A_{i})\cdot P(A_{i})}{\sum\limits_{i=1}^{k} P(B|A_{i})\cdot P(A_{i})}$$
