Los dispositivos opto-electrónicos como fotodiodos, células solares, LED y diodos láser están diseñados específicamente para optimizar la absorción y emisión de luz, lo que resulta en una alta eficiencia de conversión.

En los SC de tipo indirecto predomina el R-G center o el R-G térmico. Ya que al ser indirecto no predomina el band to band.

En los SC de tipo directo predomina el band to band recombination-generation.

Si la energia del foton es:
- mayor → Hay fotogeneración y R-G de portadores.
- menor → El SC actúa como si fuera transparente para la luz. La respuesta del fotodiodo baja.
- Cuando la longitud de onda baja  a la longitud de onda del gap → Aumenta el coeficiente de absorción y la luz es absorbida en la superficie.
#### Fotodiodos de juntura P-N
Se puede utilizar en tres modos:
1. Polarizado inverso como fotodetector (diodo PIN).
2. Fotovoltaico como célula solar.
3. Polarizado directo como LED.

Aplicaciones: Cámaras, instrumentos médicos, equipos industriales, etc.

La zona n (media) al ser menos contaminada tendrá una mayor longitud de, lo que implicará una mayor eficiencia cuántica de esa zona. Tiene un tiempo de respuesta pobre. Los portadores generados en las zonas neutras se mueven por difusión, y los generados en las zonas de deplexión por corrimiento a la veloc. de sat. de los portadores ($10^5 \frac{cm}{seg}$).

En directa:
La energía del fotón que llega a la zona de carga de espacio la usa un e- de la banda de valencia para pasar a la banda de conducción. Cada fotón al llegar a la zona de carga de espacio produce un par electrón hueco, donde debido al campo eléctrico presente, los portadores libres son arrastrados para formar parte de la corriente del circuito eléctrico.

En inversa (fotodiodo PIN):
Se trata de incrementar la velocidad de respuesta de los portadores generados por la luz. Se produce un difusión de huecos+ hacia la zona N y de e- hacia la P. Aparece barrera de potencial que evita que continúe  la difusión. En una unión PN con polarización INVERSA aumenta la barrera de potencial.

Zona de Carga de Espacio = $W_{p}+W_{n}$ : Es una zona desprovista de portadores libres.

Este ancho depende de la tensión aplicada a la unión PN
- La cara donde incide la luz debe tener un material anti-reflectante
- El material tipo P debe ser transparente a la longitud de onda incidente para que los fotones lleguen a la zona de Carga de espacio
- Los fotones atraviesan la zona P sin sufrir absorción, y llegan a la zona de Carga de Espacio donde son absorbidos.

La mayor parte de la fotocorriente se debe a portadores generados en la zona intrínseca ( zona i). La ventaja es la adaptabilidad de la zona i.
1. Se puede ajustar el ancho de la zona i a la inversa del coefic de absorc. $\alpha$ para una determinada $\lambda$
2. Mejora mucho la respuesta en frecuencia debido a que el campo E, que es grande en la zona i, rápidamente colecta a los portadores generados.
3. $f_{max}\simeq \frac{v_{sat}}{w_{i}}$

**Eficiencia cuántica:** Relación entre la cantidad de pares e- h+ obtenidos y el nro. de fotones utilizado. Es el cociente entre el nro. de $e^-$, $h^+$ generados y el nro. medio de fotones.

**Respuesta óptica (responsividad):** Es la corriente obtenida en un fotodiodo por unidad de energía luminosa incidente.
$$\mathcal{R}= \frac{I_{L}}{P_{opt}}$$


Fotones por unidad de tiempo que se aborben = $\frac{P(1-R)[1-e^{-\alpha W}]}{hv}$.


##### Celda solar BSF (Back Surface Field)
Añado otra juntura y esta me aumenta el potencial. Al aumentar el potencial, el campo eléctrico se ve beneficiado para mover electrones por la celda.
##### Celda solar con heterojuntura p-n
![[Pasted image 20240418185900.png#center|250]]
- Los fotores con energía mayor a Eg1 son absorbidos en el semiconductor A. 
- Los fotores con energía menor a Eg1 pero mayor a Eg2 son absorbidos en el semiconductor B, luego de atravesar la primera capa
#### Tecnologías de paneles solares
1. Policristalino: Tiene un proceso de fabrcación más económico (Si tipo-p). Mayor rendimiento, menor tasa de degradación y coeficiente de temperatura mejorado (Si tipo-n).
2. Mono perc half cell: 
3.  HJT - Tipo N: Se utilizan para lugares de muy altas temperaturas. Hay de tipo-p, pero las de tipo-n tiene mayor rendimiento, menor tasa de degradación y coeficiente de temperatura mejorado (como los policristalino). Ej: Panasonic.
4. IBC - Tipo N: Mismas ventajas en el tipo-n. Ej: LG.

#### Fotoconductores
Pastilla semiconductora tipo-p o tipo-n.
$$\sigma =q(\mu_{n}n_{0}+\mu_{p}p_{0}) \quad \sigma'=q(\mu_{n}(n_{0}+n')+\mu_{p}(p_{0}+p')) → \Delta\sigma=\sigma'-\sigma = q(\mu_{n}+\mu_{p})n'$$
$$R= \frac{L}{\sigma A} → \Delta R= \frac{L}{\Delta\sigma A}$$
$$\Delta I=qA(\mu_{n}+\mu_{p})n' \frac{V}{L}$$
- La potencia óptica ($P_{opt}$) es la energía de todos los fotones incidentes por unidad de tiempo. 
- ℎ𝑓 es la energía de un fotón. 
- 𝐺𝐿 son los pares electron hueco generados. 
- 𝐺𝐿 ⋅ 𝐴 ⋅ 𝐿 es la fotogeneración en toda el área del fotoconductor, es decir la cantidad de pares e-h generados. 
- La eficiencia cuántica (𝜂) que representa la relación entre pares e-h y fotones incidentes se podría escribir como:
$$\eta =G_{L}\cdot A\cdot L\cdot \frac{hf}{P_{opt}} \qquad [G_{L}]= \frac{cm^{-3}}{s}$$
- La carga total generada por unidad de tiempo tiene unidades de $[A]$ y será llamada $I_{n}$, y se define tal que: $$I_{n}=q\cdot \eta \cdot \frac{P_{opt}}{hf}$$
- Se define como ganancia óptica (𝐺𝑜𝑝𝑡) a la relación entre la variación de corriente Δ𝐼 (o $I_{D}$) e $I_{n}$. 
- Es decir, la ganancia óptica es la relación entre la corriente capaz de entregar el dispositivo y la cantidad total de carga por unidad de tiempo generada por la luz.
$$G_{opt}= \frac{\tau_{n}\mu_{n}E}{L}$$
