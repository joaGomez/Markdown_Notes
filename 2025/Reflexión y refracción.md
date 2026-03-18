### Incidencia normal
![[Pasted image 20251102214830.png#center|350]]
**Onda Incidente**
$$
\begin{split}
E^i(z) &= E_0^i \, \hat{x} \, e^{-j \beta_1 z} \\
H^i(z) &= \hat{z} \times \frac{E^i(z)}{\eta_1} = \hat{y} \, \frac{E_0^i}{\eta_1} \, e^{-j \beta_1 z}
\end{split}
$$
**Onda Reflejada**
$$
\begin{split}
E^r(z) &= E_0^r \, \hat{x} \, e^{j \beta_1 z} \\
H^r(z) &= (-\hat{z}) \times \frac{E^r(z)}{\eta_1} = -\hat{y} \, \frac{E_0^r}{\eta_1} \, e^{j \beta_1 z}
\end{split}
$$
**Onda transmitida**
$$
\begin{split}
E^t(z) &= E_0^t \, \hat{x} \, e^{-j \beta_2 z} \\
H^t(z) &= \hat{z} \times \frac{E^t(z)}{\eta_2} = \hat{y} \, \frac{E_0^t}{\eta_2} \, e^{-j \beta_2 z}
\end{split}
$$
Una vez planteadas las expresiones, se deben cumplir las condiciones de controno en $z=0$.

A partir de esto, se deducen los coeficientes de reflexión y transmisión.
$$
\begin{split}
\Gamma = \frac{\eta_{2}-\eta_{1}}{\eta_{2}+\eta_{1}} = \frac{n_{1}-n_{2}}{n_{1}+n_{2}} \\
\tau = \frac{2\eta_{2}}{\eta_{2}+\eta_{1}} = \frac{2n_{1}}{n_{1}+n_{2}}
\end{split}
$$
Si los medios no tienen pérdidas → $\Gamma$ y $\tau$ son reales. En cambio, si uno o los dos medios tienen pérdidas → $\Gamma$ y $\tau$ son complejos.

A partir del concepto de onda estacionaria, se deduce la relación de onda estacionaria (ROE) como:
$$
ROE = \frac{1+|\Gamma|}{1-|\Gamma|}
$$
#### Densidad de potencia
$$
\begin{split}
\langle\vec{S}^{i}\rangle= \frac{1}{2} \frac{|E_{0}^{i}|^{2}}{2\eta_{1}}(1-|\Gamma|^{2}) \, \hat{z} \\
\langle\vec{S}^{r}\rangle = -|\Gamma|^{2}\langle\vec{S}^{i}\rangle \, \hat{z} \\
\langle\vec{S}^{t}\rangle =  \frac{\eta_{1}}{\eta_{2}}|\tau|^{2}\langle\vec{S}^{i}\rangle \, \hat{z}
\end{split}
$$
Cuando los medios no tienen pérdidas, se conserva la densidad de potencia normal en la interfase:
$$


1 - |\Gamma|^2 = \frac{\eta_1}{\eta_2} |\tau|^2 
\quad \Rightarrow \quad 
1 = \frac{\eta_1}{\eta_2} |\tau|^2 + |\Gamma|^2

$$
$$
R = |\Gamma|^2
\qquad
T = \frac{\eta_1}{\eta_2} |\tau|^2
\quad \to \quad
1 = T + R \qquad 1 = \tau - \Gamma
$$
**Casos generales:**
1) Dieléctrico - Conductor perfecto: $\Gamma=-1 \text{ y } \tau=0$
2) Aire - Conductor real: $\Gamma=-1 \text{ y } \tau=0$
#### Múltiples interfases
![[Pasted image 20251102221125.png]]
Donde $\psi= \beta_{2}d= \frac{2\pi}{\lambda_{2}}d$
#### Antireflectante
Si $2\psi = \pi \Rightarrow \Gamma_{12} = \Gamma_{23} \Rightarrow \boxed{\eta_2 = \sqrt{\eta_1 \eta_3}}$
$$2\beta_2 d = \pi \Rightarrow 
\boxed{d = \frac{\pi}{2\beta_2} = \frac{\lambda_2}{4}}
\quad \text{lámina de un cuarto de longitud de onda}$$

Si $2\psi = 2\pi \Rightarrow \Gamma_{12} = -\Gamma_{23} \Rightarrow \boxed{\eta_1 = \eta_3}$
$$2\beta_2 d = 2\pi \Rightarrow 
\boxed{d = \frac{\pi}{\beta_2} = \frac{\lambda_2}{2}}
\quad \text{lámina de media longitud de onda}$$
#### Coeficiente de reflexión en una interfaz plana
El coeficiente de reflexión a una distancia $l_{1}$ de la interface estará dado por:
$$
\Gamma(z = -d_1) = \left. \frac{E^{r}(z)}{E^{i}(z)} \right|_{z = -d_1}
= \left. \frac{\Gamma E_0 e^{j \beta_1 z}}{E_0 e^{-j \beta_1 z}} \right|_{z = -d_1}
= \Gamma e^{-2 j \beta_1 d_1}
$$
La impedancia intrínseca de entrada será:
$$
\eta_{in}(z) = \eta_{1}\cdot \frac{\eta_{2}+\eta_{1}\tanh(\gamma z)}{\eta_{1}+\eta_{2}\tanh(\gamma z)}
$$
#### Eficiencia de apantallamiento
$$
\begin{split}
EA_{E}(dB)= 20\cdot \log\left( \bigg{|} \frac{E^{i}}{E^{t}} \bigg{|} \right) \\
EA_{H}(dB)= 20\cdot \log\left( \bigg{|} \frac{H^{i}}{H^{t}} \bigg{|} \right)
\end{split}
$$
$\text{Si } \frac{\delta}{d} \ll 1 \Rightarrow d \gg \delta$ → Se considera sólo el primer rayo transmitido:
$$E^t = \tau_{12} \tau_{23} e^{-\alpha d} E^{i}\quad\wedge\quad q= \frac{E^i}{E^t} = \frac{E^i}{\tau_{12} \tau_{23} e^{-\alpha d} E^i}$$
$$|q| = \left| \frac{(\eta_1 + \eta_2)(\eta_2 + \eta_3)}{4 \eta_2 \eta_3} \, e^{\alpha d} \right|$$
$\text{Si } \eta_1 = \eta_3 \Rightarrow |q| = \left| \frac{(\eta_0 + \eta_2)^2}{4 \eta_2 \eta_0} \, e^{\alpha d} \right|$
$\text{Si } \eta_2 \ll \eta_0 \, (\text{conductor}) \Rightarrow EA_E = 20 \log \left| \frac{\eta_0}{4 \eta_2} e^{\alpha d} \right|$

$$
\begin{split}
& R(\text{dB}) = 20 \log \left| \frac{(\eta_m + \eta_0)^2}{4 \eta_m \eta_0} \right|
\simeq 20 \log \left| \frac{\eta_0}{4 \eta_m} \right| \quad \text{Pérdida por reflexión} \\
& A(\text{dB}) = 20 \log (e^{\alpha d}) = \alpha d \, 20 \log e = 8{,}68 \, \alpha d 
= \alpha_{dB} d = \frac{d}{\delta} \quad \text{Pérdida por atenuación o absorción} \\
& M(\text{dB}) = 20 \log \left| 1 - 
\left( \frac{\eta_0 - \eta_m}{\eta_0 + \eta_m} \right)^2 
e^{- \frac{2d}{\delta} (1 + j)} \right|
\simeq 20 \log \left| 1 - e^{- \frac{2d}{\delta} (1 + j)} \right| \quad \text{Pérdidas por múltiples reflexiones}
\end{split}
$$
$$
EA_E(\text{dB}) = R(\text{dB}) + A(\text{dB}) + M(\text{dB})
$$