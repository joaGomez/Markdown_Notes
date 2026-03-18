Las Etapas de Salida de Potencia se clasifican de acuerdo a que porción o porcentaje de la Señal de entrada total manejan los transistores involucrados en el trabajo.

Las razones por las cuales se necesita contar con distintas configuraciones de Etapas de Salida, están relacionadas con el rendimiento de potencia de las mismas, o sea que porcentaje de la potencia de corriente contínua entregada a la etapa por la o las fuentes, se convierte en potencia efectiva a la salida, y que porcentaje se pierde como disipación de energía en forma de calor hacia el medio ambiente.
### Clase A
La Etapa de Salida Clase A , cuya forma de onda asociada en el colector del transistor amplificador se ve en la figura de abajo (supuesta entrada senoidal) tiene fijado su punto de polarización de modo que ICQ sea mayor que la amplitud de pico de la señal de corriente, o sea $I_{CQ} > \hat{I}_{C}$.

De esta forma, el transistor trabajando en clase A conducirá corriente durante el ciclo completo de la señal de entrada. El ángulo de conducción del transistor es 360°.

![[Pasted image 20241031100114.png#center]]
### Clase B
Las etapas de clase B operan utilizando dos transistores. A diferencia de la etapa de clase A, se polariza con una corriente $I_{CQ}=0$. Por lo tanto, un transistor en una etapa de clase B conduce solamente durante medio ciclo de la señal de entrada, resultando en un ángulo de conducción de 180°. El otro medio ciclo será suministrado por el otro transistor, que también operará en clase B.

![[Pasted image 20241031113133.png#center]]
### Clase AB
El transistor se polariza en un valor de $I_{CQ}$ tal que: $0 < I_{CQ} < \hat{I}_{CQ}$. Como resultado, cada transistor conduce durante un intervalo levemente mayor que medio ciclo. El ángulo de conducción resulta ser mayor que 180° pero mucho menor que 360°. El segundo transistor, conduce durante otro intervalo levemente mayor que el semi-ciclo negativo de la señal, combinándose ambas corrientes provenientes de ambos transistores en la carga, de lo que se observa que durante los intervalos cercanos al cruce por cero de la señal de entrada, ambos transistores conducen.

![[Pasted image 20241031113346.png#center|300]]
### Clase C
El transistor conduce durante un intervalo de tiempo menor que medio ciclo, por lo que el ángulo de conducción será menor a 180°. Como resultado, se obiene a la salida un tren periódico de pulsos de corriente.

Para recuperar la señal original, estos pulsos se pasan por un circuito tanque (LC paralelo) sintonizado a la frecuencia de la senoidal de entrada, actuando como un filtro pasabanda entregando una tensión de salida proporcional a la amplitud de la fundamental correspóndiente a su representación en serie de Fourier.

Para lograr esto, se polariza el transistor en la zona de corte: $|I_{CQ}|< \hat{I}_{CQ}$.

![[Pasted image 20241031114339.png#center|300]]
### Protección contra sobrecargas
![[Pasted image 20241031114747.png#center|300]]
