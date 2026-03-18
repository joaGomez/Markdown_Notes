### Series de Fourier
#### Forma trigonométrica
$$f(t)=a_{0} + \sum_{n=1}^{\infty}(a_{n} \cos(n\omega_{0}t)+b_{n} sen(n\omega_{0}t)$$
Donde $t_{0}<t<t_{0}+T$, y $T= \frac{2\pi}{\omega_{0}}$.

Los coeficientes de la función están dados por:
$$\begin{split}
a_{0} = \frac{1}{T}\int_{t_{0}}^{t_{0}+T}f(t) \, dt \\
a_{n} = \frac{2}{T}\int_{t_{0}}^{t_{0}+T}f(t)\cdot\cos(n\omega_{0}t) \, dt\\
b_{n} = \frac{2}{T}\int_{t_{0}}^{t_{0}+T}f(t)\cdot sen(n\omega_{0}t) \, dt
\end{split}$$
#### Forma compacta
$$f(t)= \sum_{n=0}^{\infty}C_{n}\cdot\cos(n\omega_{0}t+\varphi_{n})$$
Donde $C_{n}=\sqrt{ a_{n}^{2}+ b_{n}^{2} }$, y $\varphi_{n} = - acrtg\left( \frac{b_{n}}{a_{n}} \right)$.
#### Forma exponencial
$$f(t)=\sum_{n=-\infty}^{\infty}F_{n}e^{jn\omega_{0}t}$$
Donde $t_{0} < t < t_{0}+T$. Y el coeficiente $F_{n}$ está dado por la siguiente expresión:
$$F_{n} = \frac{1}{T} \int_{t_{0}}^{t_{0}+T}f(t)\cdot e^{-jn\omega_{0}t} \, dt $$
##### Relación entre los coeficientes de la forma trigonométrica y la exponencial
$$a_{0}=F_{0} \quad a_{n}=F_{n}+F_{-n} \quad b_{n}=j(F_{n}-F_{-n}) \quad F_{n} = \frac{1}{2}(a_{n}-jb_{n})$$
> **Observación:**
> Si $T\to \infty$ el espectro discreto de la transformada de Fourier pasa a ser epectro continuo:
> ![[Pasted image 20250306104311.png]]

### Muestreo ideal
Para muestrar una función desconocida, el proceso ideal de muestreo consta en la convolución de la función, junto con un tren de deltas. De esta forma, al realizar la transformada de la convolución, se obtiene la multiplicación de las transformadas y es más sencillo de trabajar.
Sea la convolución de estas tal que:
$$x(t)\circledast \delta_{T}(t)=X^{*}(t)$$
Al transformar esta expresión:
$$X^{*}(\omega) = \frac{1}{2\pi}X(\omega)\cdot\mathcal{F}\{\delta_{T}(t)\}= \frac{1}{2\pi}X(\omega)\cdot \omega_{s} \sum_{n=-\infty}^{\infty}\delta(\omega-n\omega_{s}) = \frac{1}{T} \sum_{n=-\infty}^{\infty}X(\omega-n\omega_{s})$$
> **Observación:**
> ![[Pasted image 20250306111155.png]]

### Muestreo natural
Dado que en la práctica es imposible crear un tren de deltas, se utiliza un tren de pulsos. Realizando el mismo procedimiento, pero con el tren de pulsos, la transformada de la convolución entre el tren de pulsos y la función desconocida es:
$$X_{N}^{*}(\omega)= \frac{\tau}{T}\left( \sum_{n=-\infty}^{\infty} sinc\left( \frac{\tau n\omega_{s}}{2} \right) \cdot X(\omega-n\omega_{s}) \right) $$
> **Observación:**
> ![[Pasted image 20250306113342.png]]

![[Relaciones Utiles.pdf]]

### Muestreo ideal con ZOH
![[ZOH Muestreo instantaneo.pdf]]
### Transformada de Fourier
Definición:
$$X(\omega) = \int_{-\infty}^{\infty}x(t)\cdot e^{-j\omega t} \, dt \qquad \qquad \text{Ecuación de análisis}$$
$$x(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty}X(\omega)\cdot e^{j\omega t} \, d\omega \qquad \qquad \text{Ecuación de síntesis}$$
**Obs:** Se puede trabajar en el dominio de la frecuencia a partir de $\omega = 2\pi f$.
#### Convolución
Definición:
$$x_{1}(t)\cdot x_{2}(t)\longleftrightarrow \frac{1}{2\pi}\cdot X_{1}(\omega)\circledast X_{2}(\omega)$$
### Beat of signals aliasing effect
![[4 - Beat of signals Aliasing Efect.pdf]]

