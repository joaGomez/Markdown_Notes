### Álgebra de sucesos
Se define un evento o suceso como un caso que quieri evaluar, el cual puede ser una posibilidad o no  dentro del espacio muestral, pero si que es requisito poder definirlo con una probabilidad de que suceda, aun así si esta probabilidad es nula (no pertenece al espacio muestral).

**Def:**
Sea $S$ (espacio muestral) un conjunto y $\sum\limits$ una colección de subconjuntos (sucesos/eventos) de $S$. $\sum\limits$ es un $\sigma$ - álgebra de $\sum\limits$ si:
- $S \in \sum\limits$
- $A \in \sum\limits \Rightarrow A{^{c}} \in \sum\limits$ 
- $A_{1}, A_{2}, ... \in \sum\limits \Rightarrow A_{1} \cup A_{2} \cup ... \in \sum\limits$

**Def:** Dos eventos $A,B$ son **mutuamente excluyentes** $\leftrightarrow$ $A\cap B=\phi$.

**Def:** El triplete ($S, \sum\limits, P$) es un **espacio de probabilidad** si $S\neq \phi$, $\sum\limits$ es un $\sigma$ - álgebra de $S$ y $P:\sum\limits \to \mathbb{R}$ cumple las siguientes condiciones:
1. $P(A) \geq 0 \quad \forall A \in \sum\limits$
2. $P(S)=1$
3. $E_{1}, E_{2},...$ son mutuamente excluyentes en $\sum\limits \Rightarrow P(\bigcup_{i=1}^{\infty}E_{i})=\sum\limits_{i=1}^{\infty}P(E_{i})$ 
**Obs:** Sea un evento $A \in \sum\limits \Rightarrow A,A{^{c}}$ son mutuamente excluyentes → $P(A^{c})=1-P(A)$.

**Obs:** $P(A\cup B)=P(A)+P(B)-P(A\cap B)$
