#### Definición
$$
\mathcal{F}(\omega) = \int_{-\infty}^{\infty} f(t)e^{-j\omega t} \, dt
$$
$$
f(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty}\mathcal{F}(\omega) e^{j\omega t}  \, d\omega = \int_{-\infty}^{\infty}\mathcal{F}(f) e^{j_{2}\pi f t}  \, df
$$
#### Propiedades de la transformada de Fourier para funciones reales
$$
\begin{align*}
\mathcal{F}(-\omega) &= \mathcal{F}{^{*}(\omega)} \\
|\mathcal{F}(-\omega)| &= |\mathcal{F}(\omega)| \\
\theta(-\omega) &= -\theta(\omega) \\
\Re\{ \mathcal{F}(-\omega) \} &= -\Im \{ \mathcal{F}(\omega) \}
\end{align*}
$$
![[Pasted image 20260305165511.png#center]]
![[Pasted image 20260305165704.png#center]]
#### Transformada de funciones periódicas
Si la función es periódica → El espectro es discreto → Los coeficientes sólo son no nulos en las frecuencias $\frac{n}{T}$.
$$
\mathcal{F}(\omega) = \sum_{-\infty}^{\infty} C_{n}\delta(\omega-n\omega_{0})
$$
 Donde los coeficientes pueden calcularse mediante una serie de Fourier, tal que:
 $$
C_{n} = \frac{1}{T_{0}} \int_{a}^{a+T}f(t)e^{-jn\omega t}  \, dt 
$$
Si la onda es real → $C_{n} = C_{-n}^{*}$
Para ondas físicas, la serie de Fourier en cuadratura se representa por:
$$
\begin{align*}
a_{0} &= \frac{1}{T_{0}} \int_{\alpha}^{\alpha+T} f(t)  \, dt\\
a_{n} &= \frac{2}{T_{0}} \int_{\alpha}^{\alpha+T} f(t)\, \cos(n\omega_{0}t)  \, dt \qquad n>0 \\
b_{n} &= \frac{2}{T_{0}} \int_{\alpha}^{\alpha+T} f(t) \, sen(n\omega_{0}t)  \, dt \qquad n>0 \\
f(t) &= \sum_{n=0}^{\infty}a_{n}\cos(n\omega_{0}t) + \sum_{n=1}^{\infty} b_{n}\, sen(n\omega_{0}t)
\end{align*}
$$
En forma polar será:
$$
\begin{align*}
f(t) &= D_{0} + \sum_{n=1}^{\infty}\cos(n\omega_{0}t+\varphi_{n})\\
D_{0} &= a_{0} \qquad \qquad \qquad \quad \,  n=0\\
D_{n} &= \sqrt{ a_{n}^{2}+ b_{n}^{2} } \qquad \qquad n>0\\
\varphi_{n} &= -\arctan\left( \frac{b_{n}}{a_{n}} \right) \quad \, \, \, n>0
\end{align*}
$$
Para una señal de entrada discreta (DFT):
$$
\begin{align*}
X_{n} &= \sum_{k=0}^{N-1} x_{k}\, e^{-j\frac{2\pi nk}{N}}\\
x_{k} &= \sum_{n=0}^{N-1} X_{n}\, e^{j\frac{2\pi nk}{N}}
\end{align*}
$$
La DFT representa la transformada de una función periódica con período $NT_{0}$.
#### Convolución
La convolución de dos funciones está dada por:
$$
g(t) = \int_{-\infty}^{\infty} f_{1}(\tau)\cdot f_{2}(t-\tau)  \, d\tau 
$$
##### Interpretación gráfica
![[Pasted image 20260306110300.png#center]]

La convolución es conmutativa, distributiva, y asociativa.

**Obs:** La convolución de una función cualquiera por la función delta da como resultado la función en la posición de la delta. Este fenómeno se utiliza en modulación, demodulación, y muestreo.
#### Sistemas LTI
La salida de un sistema LTI se puede escribir como la convolución entre la entrada del sistema, y la respuesta impulsiva del mismo:
$$
y(t) = x(t)\ast h(t)
$$
#### Distorsión
Si buscamos que la señal de salida sea una copia fiel a la entrada, solo debemos admitir que la salida sea una representación escalada y desplazada de la entrada, tal que:
$$
y(t) = A\cdot x(t-T_{d})
$$
Aplicando Fourier, para un retardo $T_{d}$ cte, implica que la fase sea lineal y la amplitud sea constante → Salida sin distorsión.

**Demo**
$$
\begin{align*}
& \qquad Y(f)=X(f)\cdot H(f) = A \cdot F(f)\cdot e^{-j 2\pi fT_{d}} \\
\text{Entrando con } x(t)=\delta(t) \qquad  \to & \qquad H(f)= A\cdot e^{-j 2\pi fT_{d}} \\
\text{Condiciones sin distorsión}:\,\, \qquad & \qquad |H(f)|=A=cte \quad \wedge \quad \theta(f) = -2\pi fT_{d}
\end{align*}
$$
#### Correlación
La correlación entre dos funciones está definida por:
$$
\psi_{fg} = \int_{-\infty}^{\infty} f(\tau)\cdot g(t+\tau)  \, d\tau 
$$
La función de autocorrelación es cuando $g(t)=f(t) \to \psi_{fg}=\psi_{f} = \int_{-\infty}^{\infty} f(\tau)\cdot f(t+\tau)  \, d\tau$
#### Densidad espectral de energía
La relación entre la energía de una señal y su espectro está dado por el teorema de Parseval.
$$
\begin{align*}
E_{f} &= \int_{-\infty}^{\infty} f(t)f^{*}(t)  \, dt = \frac{1}{2\pi} \int_{-\infty}^{\infty}\mathcal{F}(\omega)\mathcal{F}^{*}(\omega)  \, d\omega\\
&= \frac{1}{2\pi} \int_{-\infty}^{\infty}|\mathcal{F}(\omega)|^{2}  \, d\omega = \int_{-\infty}^{\infty} |\mathcal{F}(f)|^{2} \, df    < \infty
\end{align*}
$$
**Obs:** En el caso de señales periódicas la integral es infinita y el concepto de energía no tiene sentido, se los denomina señales de potencia.

$E_f$ indica el valor de energía disipado sobre una resistencia de $1\,\Omega$.

Si $f(t)$ representa una señal de tensión:
$$
E_f = \frac{1}{R} \int_{-\infty}^{\infty} f(t)\,f^*(t)\,dt
$$
Si $f(t)$ representa una señal de corriente:
$$
E_f = R \int_{-\infty}^{\infty} f(t)\,f^*(t)\,dt
$$
Aplicando una señal $f(t)$ a un filtro con transferencia $H(\omega)$ → $Y(\omega) = H(\omega)\cdot F(\omega)$

La función densidad espectral de energía a la salida será:
$$
|Y(\omega)|^{2}=|H(\omega)|^{2}\cdot|F(\omega)|^{2} \quad \to \quad \psi_{y}(\omega) = |H(\omega)|^{2}\cdot \psi_{f}(\omega)
$$
#### Densidad espectral de potencia
Para una señal de potencia (cuya densidad espectral de energía es infinita), se puede calcular el promedio de la energía sobre un intervalo de tiempo finito:
$$
P_{f} = \lim_{ T \to \infty } \frac{1}{T} \int_{-\frac{T}{2}}^{\frac{T}{2}}  f^{2}(t)\, dt = \lim_{ T \to \infty } \frac{E_{T}}{T}   
$$
Además, se denomina $S_{f}(\omega)$ a la función de densidad espectral de potencia, tal que:
$$
S_{f}(\omega) = \lim_{ T \to \infty } \frac{|F_{t}(\omega)|^{2}}{T} \qquad \to \qquad P_{f} = \frac{1}{2\pi}\int_{-\infty}^{\infty}S_{f}(\omega)  \, d\omega
$$
Para señales de potencia, la correlación se define como:
$$
\mathcal{R}_{f}(t) = \lim_{ T \to \infty } \int_{-\infty}^{\infty}f(\tau)\cdot f(t+\tau) \, d\tau  
$$
#### Ancho de banda de señales
Si la señal es limitada en el tiempo → Es limitada en la frecuencia → Para todas las señales reales, el ancho de banda es infinito.
- Ancho de banda absoluto: Es el intervalo de frecuencias fuera del cual la señal es nula.
- Ancho de banda de 3dB: Es el intervalo entre las freciencias donde la amplitud se reduce a $\frac{1}{\sqrt{ 2 }}$ del valor máximo en la banda (en potencia, esto significa que se reduce al 50%).
- Ancho de banda equivalente: Es el ancho de un espectro rectangular ficticio de amplitud igual a la máxima dentro de la banda. Este representa el mismo contenido de potencia.
- Ancho de banda entre cruces por cero: Es el ancho del espectro entre los dos cruces por cero de la envolvente del espectro de magnitud.
- Ancho de banda de potencia: Es el ancho del espectro dentro del cual reside el 99% de la potencia total.
- Ancho de banda de espectro acotado: Está definido por las frecuencias fuera de la cual el espectro es ak menos $x$ dB bajo el máximo.
#### Filtros físicamente realizables
Dado un circuito que represneta una respuesta al impulso $h(t)$, la misma debe ser causal. En el espactro, esta condición implica cumplir con el criterio de Paley-Wiener:
$$
\int_{-\infty}^{\infty} \frac{|\ln(H(\omega))|}{1+\omega^{2}} \, d\omega < \infty \qquad \wedge \qquad \int_{-\infty}^{\infty}|H(\omega)|^{2}   \, d\omega < \infty  
$$