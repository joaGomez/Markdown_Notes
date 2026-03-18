## Theory

##### Programming styles for managing complexity
**Imperative**(procedural): 
- Focus on step-by-step instructions to accomplish any task.
- Organize programs using structured conditionals and loops.
**Functional**:
- Focus on procedures that mimic mathematical functions producing outputs from inputs without side effects.4
- Functions are *first-class objects* used in data structures, arguments to procedures, and can be returned by procedures.
**Object-oriented**
- Focus on collections of related procedures and data.
- Organize programs as hierarchies of related classes and instances.

#### Fast exponentiation
$$b^{n}=
\begin{cases}
1  & n=0\\
b.b^{n-1}  & n~is~odd  \\
(b^\frac{n}{2})^{2} & otherwise
\end{cases}$$
Functional notation:
$$f(n)=
\begin{cases}
1  & n=0\\
b.f(n-1) & n~is~odd \\
(f(\frac{n}{2}))^{2}  & otherwise
\end{cases}$$
```python 
Code implementation
def fastExponent(b,n): 
	if n==0: 
		return 1 
	elif n%2==1: 
		return b*fastExponent(b,n-1) 
	else: 
		return fastExponent(b,n/2)**2
```




## Quizes

#### Quiz 1
(Se trata de mecionar la instancia y el valor que arrojaria)
