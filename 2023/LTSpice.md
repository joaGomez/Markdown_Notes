| Valor      | Unidad | Comando |
| ---------- | ------ | ------- |
| $10^{6}$   | Mega   | meg     |
| $10^{3}$   | Kilo   | k       |
| $10^{0}$   | Unidad | -       |
| $10^{-3}$  | Mili   | m       |
| $10^{-6}$  | Micro  | u       |
| $10^{-9}$  | Nano   | n       |
| $10^{-12}$ | Pico   | p        |

**Obs.** Shortcuts para parámetros → .param (nombre) = (valor), y la propiedad será {(nombre)} en el componente.

**Obs.** Para calcular el período/frecuencia de una oscilación, no me conviene usar el primer pico, sino el segundo y tercero para tener mejor precisión.

Análisis de montecarlo → Análisis para ver la tolerancia de los componentes → mc(valor, tolerancia)

.step param (nombre) (n_comienzo) (n_final) (steps)

Análisis en frecuencia → AC acmplitude = 1



Parte 2
Intentamos hacer una single supply, por lo que necesitamos un offset de 4,5V, pero al simularlo en el LTSpice, la tensión de salida se satura. 
![[Pasted image 20231108173620.png]]
