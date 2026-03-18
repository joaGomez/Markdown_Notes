
----
## Fuentes de continua
---
Las fuentes ideales no tienen resistencia interna, mientras que las fuentes reales si que tienen. Todo lo que se conecta al circuito y no es una fuente se lo llama carga, y la fuente ideal entrega la corriente que le pide la carga.

El circuito ideal se quema tal que $i \to \infty$ 

### Ley de OHM $$V = R.I$$
En el circuito real:
$$\begin{cases} 
V_{C}=I.R_{c} \\
V_{F}=I.(R_{C}+R_{F})
\end{cases}
→ \begin{cases} 
\frac{V_{C}}{R_{C}}=\frac{V_{F}}{R_{C}+R_{F}} 
\end{cases}
→ V_{C}=\frac{V_{F}\ R_{C}}{R_{C}+R_{F}}$$
Siendo $V_{C}$ la tensión que recibe la carga. Cuánto mejor sea la fuente de tensión → Más chica será $R_{F}$.
## Fuentes de corriente
---
Fuente de corriente real → Conexión de resistencias en paralelo. Una buena fuente de corriente tiene un $R_F$ grande → La mayor parte de $I_{F}$ vaya para la carga.
![[Pasted image 20230905151701.png]]
En las fuentes de tensión y continua reales → La tensión y la corriente son 'ctes', son las prestablecidas, y no dependen de $R_{C}$.
## Leyes de Kirchoff
---
- 1ra Ley:
La sumatoria de corrientes que pasan por los nodos, teniendo en cuenta las corrientes que entran y salen, es 0. Por convención, las corrientes entrantes son positivas, y las salientes son negativas.
- 2da Ley:
La sumatoria de las diferencias de potencial en una malla es 0.

La corriente $(I)$ al pasar por las resistencias $(R)$ sufre una caída de potencial.
##### Def.
El nodo es donde se juntan dos componentes (No necesariamente) distintas corrientes
##### Def.
Si un cable es ideal → No es resistivo.
## Potencia
---
$$P=V.I \to P = R.I^{2}$$
- Los componentes pasivos consumen potencia → $P>0$ 
- Los componentes activos pueden consumir/aportar potencia. Si aportan potencia → $P<0$ 
- Para la potencia de la batería de los componentes activos, que no estoy seguro si están consumiendo o aportando potencia, analizo por donde ingresa la corriente. Si es por el signo (-) → $P<0$, y si ingresa por el signo (+) → $P>0$.
- Idealmente, se debe cumplir que: $\sum P=0 \ W$.
##### Tip
Al resolver con mallas, nunca recorro una malla con una tensión de corriente, ya que no puedo calcular su caída de potencial.
#### Prop.
Por kirchoff puedo resolver usando nodos o mallas. Es más conveniente usar nodos cuando tengo más fuentes de tensión en el circuito. Por otro lado, es más conveniente usar mallas cuando tengo más fuentes de corriente.

- Fuentes de corriente y tensión (reales e ideales) → Son fuentes independientes → No dependen de lo que pase en el circuito

Ej de la clase → Resuelto por nodos y aplicando super-nodos
![[Pasted image 20230804123010.png]]

![[Pasted image 20230804124201.png]]

Si bien con las fuentes controladas se pueden hacer transistores → No toda fuente controlada es un transistor

### Trabajar con fuentes reales
---
Sustitución de fuentes **reales** → fuentes **ideales**

   ![[Pasted image 20230808221026.png|700]]

Al sustituir de fuentes, se cumple que:
$$V_{1}=I_{2}R_{2} \ \wedge \ R_1=R_{2}$$
## Thevenin/Norton
---
Ambos plantean un crcuito abierto con nodos extremos A, B con una diferencia de potencial $V_{AB}$ que nos servirá para discretizar un circuito ya que por mas que le agregue una parte más compleja al circuito unida a A, B, su diferencia de potencial se mantendrá igual y podremos trabajar con la carga y analizarla como queramos.
   
   ![[Pasted image 20230811153430.png|600]]
- Por Thevenin:
   ![[Pasted image 20230811154757.png|600]]
- Por Norton:
   ![[Pasted image 20230811154833.png|600]]

###### Obs
- De ambos podemos deducir $$R_{Tn}=R_{N}=\frac{V_{Tn}}{I_{N}}$$
Donde deducimos el primer método para despejar $R_{Tn}$ o $R_{N}$ y sirve hasta para fuentes controladas.

- El segundo método consiste en pasivar el circuito. Donde se cambian las fuente de tención por cables (cortocircuito), y las fuentes de corriente se quitan y se deja abierto.
   → Para calcular $R_{Tn}$ o $R_{N}$ se cuenta la resistencia total mirando desde el terminal positivo (A).
   Éste método no funciona con fuentes controladas.
- El tercer método consiste en conectar una fuente (con valor elegido arbitrariamente, dependiendo la fuente que elijo, si es de tensión o corriente).
![[Pasted image 20230811161245.png|200]]
   → Despejamos el valor de la resistencia de Thevenin/Norton: $R_{N}=R_{Tn}=\frac{V_{F}}{I_{F}}$
   