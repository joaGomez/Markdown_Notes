Se describe una antena como aquella parte de un sistema transmisor o receptor, diseñado específicamente para radiar o recibir ondas electromagnéticas.

Una antena transmisora permite la transición eficiente de la energía electromagnética desde el transmisor hacia el espacio libre. Mientras que una antena receptora realiza el proceso inverso.
### Gauge de Lorenz
Las ec. de Maxwell no imponen ninguna condición sobre la divergencia de $\vec{A}$. Se la puede elegir para resolver el problema, esta elección se denomina elegir un calibración o gauge.
$$
\text{Gauge de Lorenz} \qquad \nabla\cdot \vec{A} = - u_{0}\varepsilon_{0} \frac{\partial V}{\partial t}
$$
La solución está dada por:
$$
\vec{A}(\vec{r},t) = \frac{\mu}{4\pi} \iiint_{v'} \frac{J'(\vec{r}')e^{j(\omega t-\vec{k}\cdot \vec{r})}}{R} dv'
$$
**Obs:** Existe generación de ondas electromagnéticas sólo si J es función del tiempo.
### Dipolo de Hertz
Se considera dipolo de Hertz si $\Delta L < \frac{\lambda}{50}$, y el radio del alambre $a \ll \lambda$. Para este caso, el campo $\vec{A}$ será:
$$
\vec{A}(\vec{r}) = A_{z}(r) = \frac{\mu_{0}}{4\pi r}\cdot I\cdot \Delta L\cdot e^{-jkr} \hat{z}
$$
Trabajando con coordenadas esféricas, se consiguen las siguientes expresiones para los campos:
$$
\begin{align}
& \vec{E} = E_{r}\hat{r} + E_{\theta}\hat{\theta} + E_{\phi}\hat{\phi} \to \begin{cases}
E_{r} = - \frac{\eta_{0}}{2\pi}\cdot I\cdot \Delta L\cdot k^{2}\cos \theta\cdot e^{-jkr}\left( \left( \frac{1}{jkr} \right)^{2} + \left( \frac{1}{jkr} \right)^{3} \right) \\
E_{\theta} = - \frac{\eta_{0}}{4\pi}\cdot I\cdot \Delta L\cdot k^{2}\,sen \theta\cdot e^{-jkr}\left( \frac{1}{jkr}+\left( \frac{1}{jkr} \right)^{2} + \left( \frac{1}{jkr} \right)^{3} \right) \\
E_{\phi} = 0
\end{cases} \\
& H = - \frac{1}{4\pi}\cdot I\cdot \Delta L\cdot k^{2}\, sen\theta\cdot e^{-jkr}\left( \frac{1}{jkr} + \left( \frac{1}{jkr} \right)^{2}\right)
\end{align}
$$
#### Campo cercano reactivo
**Condición:** $\vec{k}\cdot \vec{r}\ll 1$ o $r\ll \frac{\lambda}{2\pi}$
$$
\begin{align}
&E_{r} = - j\frac{\eta_{0}\cdot I\cdot \Delta L\cdot \cos \theta}{2\pi kr^{3}} \\
&E_{\theta} = - j\frac{\eta_{0}\cdot I\cdot \Delta L\cdot \, sen\, \theta}{4\pi kr^{3}} \\
&E_{\phi} = 0  \\
& H_{\phi} = \frac{I\cdot \Delta L\cdot \, sen\, \theta}{4\pi r^{2}}
\end{align}
$$
*Hay un desfasaje de 90° entre $E$ y $H$*.

El vector de Poynting es imaginario puro, lo que indica energía almacenada en los campos (potencia reactiva) → $\langle \vec{S} \rangle = 0$
#### Campo cercano de radiación
**Condición:** $\vec{k}\cdot \vec{r}> 1$ o $r > \frac{\lambda}{2\pi}$
$$
\begin{align}
&E_{r} = \frac{\eta_{0}\cdot I\cdot \Delta L\cdot e^{-jkr}\cos \theta}{2\pi r^{2}} \\
&E_{\theta} = j\frac{\eta_{0}\cdot I\cdot k\cdot \Delta L\cdot e^{-jkr} \, sen\, \theta}{4\pi r} \\
&E_{\phi} = 0  \\
& H_{\phi} = j\frac{I\cdot k\cdot \Delta L\cdot \, e^{-jkr}sen\, \theta}{4\pi r}
\end{align}
$$
$E_{\theta}$ y $H_{\phi}$ están en fase → Radiación.

Además, predominan los campos de radiación ($E_{\theta}$ y $H_{\phi}$), pero todavía $E_{r}$ no es despreciable.
#### Campo lejano de radiación
**Condición:** $\vec{k}\cdot \vec{r}\gg 1$ o $r \gg \frac{\lambda}{2\pi}$
$$
\begin{align}
&E_{r} = 0 \\
&E_{\theta} = j\frac{\eta_{0}\cdot I_{0}\cdot k\cdot \Delta L\cdot e^{-jkr} \, sen\, \theta}{4\pi r} \\
&E_{\phi} = 0  \\
& H_{\phi} = j\frac{I_{0}\cdot k\cdot \Delta L\cdot \, e^{-jkr}sen\, \theta}{4\pi r}
\end{align}
$$
**Obs:** Los campos cercano y lejano son del mismo orden si:
$$
\frac{k}{r} = \frac{1}{r^{2}} \to r = \frac{\lambda}{6}
$$
En campo lejano, el vector de Poynting será:
$$
\langle \vec{S} \rangle = \frac{\eta_{0}k^{2}I_{0}^{2}\Delta L^{2}}{32\pi r^{2}}\cdot sen^{2}\theta \, \hat{r}
$$
#### Dipolo corto
**Condición:** $\Delta L< \frac{\lambda}{10}$
$$
\begin{align}
& E(r,\theta) = j \frac{\eta kI_{0}L}{8\pi}\cdot \frac{e^{-jkr}}{r} sen\,\theta \, \hat{\theta} \\
& H(r,\theta) = j \frac{kI_{0}L}{8\pi}\cdot \frac{e^{-jkr}}{r} sen \, \theta \, \hat{\varphi} \\
&\langle \vec{S} \rangle = \hat{r} \frac{\eta(kI_{0}L)^{2}}{128\pi^{2}}\cdot \frac{sen^{2}\,\theta}{r^{2}}
\end{align} 
$$
### Diagrama de radiación
**Diagramas absolutos:** Representan el campo eléctrico o la densidad de potencia para una potencia entregada a la antena y una distancia constante: $S(r,\theta,\phi) \to S(\theta,\phi)$

**Diagramas relativos:** Son como los diagramas abolutos, pero normalizados respecto al máximo valor de la función presentada.
$$
F(\theta,\phi) = \frac{S(\theta,\phi)}{S_{max}(\theta,\phi)} \qquad E_{n}(\theta,\phi) = \frac{E(\theta,\phi)}{E_{max}(\theta,\phi)}
$$
### Planos del dipolo de Hertz
El plano $E$ es el definido por la dirección de máxima radiación($\theta= \frac{\pi}{2}$), y el campo eléctrico en dicha dirección (vector paralelo al eje z). Por lo tanto, el plano $E$ es cualquier plano $\phi=cte$.

El plano $H$ está definido por la dirección de máxima radiación y la orientación del campo magnético en dicha dirección. El diagrama en dicho plano es omnidireccional.
### Tipos de diagrama
**Antena isotrópica:** Antena ideal, sin pérdidas que irradia de forma uniforme en todas las direcciones.

**Antena omnidireccional:** Una antena que irradia de forma uniforme en todas las direcciones, en un determinado plano.

**Antena direccional:** Una antena que irradia más eficientemente en determinadas direcciones con respecto a otras.
### Ancho de haz
Es el ancho angular determinado por el haz. Este se utiliza para determinar el ancho de banda de una antena.
#### Ángulo sólido
El ángulo sólido $\Omega$ es el área que cubre un haz sobre la superficie de una esfera unitaria:
$$
\Omega = \int_{\Delta \theta}\int_{\Delta \phi} sen\, \theta \, d\phi   \, d\theta 
$$
Si la superficie fuera una esfera → $\Omega = 4\pi$
### Intensidad de radiación
Es la potencia radiada por unidad de ángulo sólido:
$$
U \equiv \frac{dP_{r}}{d\Omega} \to U(\theta, \phi) = \vec{S}(r, \theta, \phi) r^{2}
$$
La intensidad de radiación (U) es independiente de la distancia a la antena (r) , sólo depende de los parámetros inherentes a la misma.
#### Directividad
Se define como la medida de la habilidad de una antena para concentrar la densidad de potencia en una determinada dirección.
$$
D(\theta, \phi) = \frac{U(\theta, \phi)}{\langle U\rangle} = \frac{F(\theta, \phi)}{\frac{1}{4\pi}\iint_{s}F(\theta, \phi)d\Omega} = D_{max}\cdot F(\theta, \phi)
$$
Para un dipolo de Hertz → $F(\theta, \phi) = sen^{2} \theta$
$$
D_{max} = \frac{3}{2} \to D(\theta, \phi) = \frac{3}{2}\cdot sen^{2}\theta
$$
#### Ganancia
Se define como la relación entre la intensidad de radiación producida por la antena en una dada dirección respecto de la producida por una antena isotrópica para la misma potencia de entrada.
$$
g(\theta, \phi) = \frac{U(\theta, \phi)}{U_{\text{isotrópica}}(\theta, \phi)}
$$
Una antena Tx con 6dB de ganancia en una dirección, emite 4 veces más que la isotrópica en dicha dirección.
### Resistencia de radiación
Es el valor de una resistencia ‘ficticia’ que disipa una potencia igual a la potencia radiada por la antena, cuando por la misma circula la misma intensidad de corriente que circula por la antena.
$$
R_{r} = \frac{2P_{r}}{I_{0}^{2}}
$$
Para un dipolo de Hertz → $R_{r} = 80\pi^{2}\left( \frac{\Delta L}{\lambda} \right)^{2} [\Omega]$
### Eficiencia de radiación
Se define la eficiencia de radiación como:
$$
\xi = \frac{P_{r}}{P_{em}} = \frac{R_{r}}{R_{r}+R_{p}}
$$
Donde $\xi=1$ para una antena sin pérdidas.

A partir de este factor, se puede reescribir la ganancia de una antena como:
$$
g(\theta, \phi) = \xi\cdot D(\theta, \phi)
$$
En general: $P_{r}\leq P_{en} \to G\leq D$
### Directividad y ancho de haz
Dado $\Omega_{p} = \iint F(\theta, \phi) d\Omega \simeq BW_{\theta}\cdot BW_{\phi}$, para una antena con un sólo máximo principal, la directividad máxima será:
$$
D_{max} = \frac{4\pi}{\Omega_{p}} \simeq \frac{4\pi}{BW_{\theta}\cdot BW_{\phi}}
$$
Para una antena omnidireccional → $\Omega_{p} = BW_{\theta}\cdot 2\pi$
### Impedancia de la antena
Se define la impedancia de la antena como:
$$
Z_{A} = \frac{V(0)}{I_{\text{antena}}} = R_{A} + jX_{A} = R_{r} + R_{p} + jX_{A}
$$
### Ancho de banda
$$
\begin{align} \\
& \text{Banda angosta} \qquad & B= \frac{f_{s}-f_{i}}{f_{c}}\cdot 100 \\
& \text{Banda ancha} & B= \frac{f_{s}}{f_{i}}
\end{align}
$$
### Integración con línea de transmisión
![[Pasted image 20251116161149.png#center|350]]
Por máxima transferencia de potencia: $R_{r}+R_{p} = R_{g}$ y $X_{A}=-X_{g}$, entonces:
$$
I = \frac{V_{g}}{Z_{g}+Z_{A}} = \frac{V_{g}}{(R_{r}+R_{p}+R_{g})+j(X_{A}+X_{g})} \underset{\text{máx. potencia}}{\longrightarrow} I = \frac{V_{g}}{2(R_{r}+R_{p})}
$$
La potencia que irradia la antena será:
$$
P_{r} = \frac{1}{2}|I|^{2}\cdot R_{r} = \frac{1}{4} \frac{|V_{g}|^{2}}{(R_{r}+R_{p})^{2}}R_{r} \simeq \frac{|V_{g}|^{2}}{4R_{r}}
$$
Además
$$
\begin{align}
& \text{Disipada en el generador} \qquad & P_{g} = \frac{P}{2} \\
& \text{Radiada por la antena} & P_{r} = \frac{\xi}{2}P \\
& \text{Disipada en la antena} & P_{L} = \frac{P}{2}(1-\xi)
\end{align}
$$
**Obs:** En un sistema de dos antenas, el cociente entre las potencias no depende de cual antena transmite y cual recibe.

El diagrama de radiación y la resistencia de radiación de una antena transmisora son los mismos cuando actúa como receptora si el sistema es lineal → Cuanto más eficiente es una antena como transmisora más eficiente será como receptora para la misma frecuencia.

El teorema de reciprocidad no es válido para antenas activas.
### Polarización de la antena
La polarización de una antena transmisora (Tx) es la polarización de la onda radiada en la zona de campo lejano. Cuando no se indica la dirección, se considera que la polarización es la polarización en la dirección de máxima ganancia.

La polarización de una antena receptora (Rx) es la polarización de una onda plana incidente, que, para una densidad de flujo de potencia (Poynting) dada, resulta en la máxima potencia disponible en los terminales de la antena.
$$
\text{Versor de polarización} \qquad \hat{\rho}_{a} = \left( \frac{E_{x}}{|E_{a}|} \hat{x} + \frac{E_{y}}{|E_{a}|} e^{j\delta} \, \hat{y}\right)
$$
Si $\hat{\rho}_{a}\cdot \hat{\rho}_{0} = 1$ → La antena Rx y la onda incidente están acopladas en polarización.

Se define el desacople en polarización o factor de pérdida por desacople en polarización (PLF) como:
$$
PLF = |\hat{\rho}_{a}\cdot \hat{\rho}_{0}|^{2}
$$
### Ecuación de Fris
La potencia disponible en los bornes de la antena Rx con acople ideal en polarización es:
$$
\frac{P_{dr}}{P_{eT}} = \left( \frac{\lambda}{4\pi r} \right)^{2}g_{t}(\theta_{t},\phi_{t})\cdot g_{r}(\theta_{r},\phi_{r})
$$
$$
\frac{P_{er}}{P_{dT}} = \left( \frac{\lambda}{4\pi r} \right)^{2}g_{t}(\theta_{t},\phi_{t})\cdot g_{r}(\theta_{r},\phi_{r})\cdot PLF\cdot(1-|\Gamma_{T}|^{2})\cdot(1-|\Gamma_{R}|^{2})
$$
