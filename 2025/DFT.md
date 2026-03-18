La transformada discreta de Fourier (DFT) tiene como finalidad obtener el espectro de una señal mediante el uso de un hardware digital que puede ser una PC o un procesador digital de señales (DSP).

Dado que la memoria de un sistema digital es de naturaleza discreta no podemos almacenar una señal continua por lo tanto debemos muestrearla. Por otro lado sabemos que la memoria para almacenar es finita por lo que debemos acotar la duración de la señal. Este proceso se puede modelar mediante la multiplicación de la señal por una función ventana cuya duración equivale al número de posiciones de memoria disponible por el período de muestreo usado es decir: $T_{0} = NT$.

Como resultado de estas operaciones, se obtiene una señal y su espectro. Pero como su espectro es continuo en $f$, no puede ser almacenado en memoria. La solución en este caso, es muestrear el espectro de la señal con un tren de impulsos separados en $\frac{1}{T_{0}}$, siendo $T_{0}$ igual a la duración de la ventana temporal.

**Obs:** Si el período de muestreo en el dominio de la frecuencia es mayor que este último valor tendremos aliasing temporal.
#### Desarrollo analítico
1) Muestreo en el dominio del tiempo:
$$x^{*}(t)=x(t)\delta_{T}(t)=x(t)\sum_{n=-\infty}^{\infty}\delta(t-nT)=\sum_{n=-\infty}^{\infty}x(nT)\delta(t-nT)$$
2) Truncado en el dominio del tiempo:
$$x_{w}^{*}(t)=x^{*}(t)w(t)=\left(\sum_{n=-\infty}^{\infty}x(nT)\delta(t-nT)\right)w(t)=\sum_{n=0}^{N-1}x(nT)\delta(t-nT)$$
![[Pasted image 20250423104425.png#center]]
3) Muestreo en el dominio de la frecuencia: Al muestrear en el dominio de la frecuencia el espectro de la señal truncada con un tren periódico de deltas $\delta_{1}(w)$ separadas en $\omega_{0}= \frac{1}{T_{0}}$ es equivalente a convolucionar en el tiempo con un tren periódico de deltas $\delta_{1}(t)$ siendo la separación entre la mismas $T_{0}$.
$$\tilde{x}(t)=x_{w}^{*}(t)\ast\delta_{1}(t)=\left[\sum_{n=0}^{N-1}x(nT)\delta(t-nT)\right]\ast\left[ T_{0}\sum_{r=-\infty}^{\infty}\delta(t-rT_{0}) \right]$$
Recordando que $\delta(t-t_{1})\ast \delta(t-t_{2})=\delta(t-t_{1}-t_{2})$, tenemos que:
$$\tilde{x}(t)=T_{0}\sum_{r=-\infty}^{\infty}\left[\sum_{n=0}^{N-1}x(nT)\delta(t-nT-rT_{0})\right]$$
Dado que $\tilde{x}(t)$ es periódica, podemos desarrollarla como serie de Fourier:
$$\tilde{x}(t)\sum_{k=-\infty}^{\infty}F_{k}e^{jk\omega_{0}t} \qquad \text{donde } F_{k}= \frac{1}{T_{0}} \int_{-\frac{T}{2}}^{T_{0}-\frac{T}{2}}\tilde{x}(t)e^{-jk\omega_{0}t} \, dt $$
Los coeficientes de la serie serán:
$$F_{k}= \frac{1}{T_{0}}\int_{-\frac{T}{2}}^{T_{0}- \frac{T}{2}}\left[T_{0}\sum_{r=-\infty}^{\infty} \sum_{n=0}^{N-1}x(nT)\delta(t-nT-rT_{0}) \right]e^{-jk\omega_{0}t} \, dt$$
Como integramos en el intervalo $\left[ -\frac{T}{2} , T_{0} - \frac{T}{2}\right]$, solo queda el término para $r=0$. Por lo tanto:
$$F_{k}= \int_{-\frac{T}{2}}^{T_{0}- \frac{T}{2}}\left[ \sum_{n=0}^{N-1}x(nT)\delta(t-nT) \right]e^{-jk\omega_{0}t} \, dt $$
Por la propiedad de la delta, tenemos que:
$$F_{k} = \sum_{n=0}^{N-1}x(nT)e^{jk\omega_{0}nT}= \sum_{n=0}^{N-1}x(nT)e^{j \frac{2\pi}{N} nk}$$
Ya que $\omega_{0}T= \frac{2\pi}{T_{0}}T = \frac{2\pi}{NT}T = \frac{2\pi}{N}$.

Por lo tanto, el desarrollo en serie de la función queda tal que:
$$\tilde{x}(t)=\sum_{k=-\infty}^{\infty}\left( \sum_{n=0}^{N-1}x(nT)e^{-j \frac{2\pi}{N}nk} \right) e^{jk\omega_{0}t} $$
A la transformada de Fourier de esta función, la llamaremos $\tilde{X}\left( \frac{k}{NT} \right)$ y será:
$$\tilde{X}\left( \frac{k}{NT} \right)=\sum_{k=-\infty}^{\infty}\left( \sum_{n=0}^{N-1}x(nT)e^{j \frac{2\pi}{N}}nk \right) \delta(\omega -k\omega_{0})$$
**Obs:** $F_{k}$ tiene período $N$, por lo que para hallar el espectro de la señal sólo necesitamos evaluar los primeros $N$ valores de $F_{k}$.
![[Pasted image 20250423112743.png#center]]
##### DFT
$$X\left( \frac{k}{NT} \right) = \sum_{n=0}^{N-1}x(nT)e^{-j \frac{2\pi}{N}nk} \qquad k=0,1,\dots,N-1$$
Además:
$$X\left( \frac{k}{NT} \right)=X\left(\frac{k+N}{NT}\right) \qquad r=0, \pm 1, \pm 2,\dots$$
##### IDFT
$$x(nT)= \frac{1}{N}\sum_{k=0}^{N-1}\tilde{X}\left( \frac{k}{NT} \right)e^{j \frac{2\pi}{N}nk} \qquad n=0,1,\dots,N-1$$
$$x(nT)= x(nT+rNT) \qquad r=0, \pm 1, \pm 2, \dots$$
#### Recuperación de $x(n)$
La señal $x(n)$ puede recuperarse a partir de $\tilde{x}(n)$ siempre que no tengamos aliasing en el dominio del tiempo. Para que esto sea posible la duración de $x(n)$ debe ser finita. Si la duración de la señal $x(n)$ es de $L$ muestras se debe cumplir que $N\geq L$.

![[Pasted image 20250423113512.png#center]]
#### Resolución espectral
La resolución espectral esta dada por la separación entre las muestras en frecuencia que es $\frac{1}{T_{0}}$, es decir la recíproca del ancho de la ventana. Esto significa que podemos aumentar la resolución aumentando $T_{0}$. Como $T_{0}=NT$ tenemos dos posibilidades. Una es aumentar $T$ y la otra es aumentar $N$. El valor de $T$ normalmente es fijo dado que lo impone el hardware, así que sólo nos queda aumentar $N$ para obtener una mejor resolución. Si la señal es de duración finita $L$, un aumento en $N$ equivale a agregar $N-L-1$ ceros. Agregar ceros no nos modifica el espectro de la señal pero mejora la calidad visual del espectro. 

Para entender mejor esto supongamos que a la secuencia $x(n)$ la multiplicamos por una onda cuadrada cuyo período es $2N$. Al hacer esta operación estamos generando una nueva señal de período $2N$. Esta señal contiene un sólo período de la señal original $(N)$ más $N$ ceros. Como el período de la nueva señal es $2N$ tendemos que su DFT tiene el doble de muestras en frecuencia que la DFT de la original.

![[Pasted image 20250423114556.png#center]]

Debe enfatizarse que el hecho de agregar ceros no altera en nada el espectro de la señal original. Lo que ocurre es que es que el espectro ahora contiene muestras adicionales entre las originales. Dichas muestras adicionales tienen una amplitud dada por la función $W(f)$ que actúa como interpoladora.

**Ejemplo:**
![[Pasted image 20250423114815.png#center]]
A continuación ejemplo de la DFT en forma gráfica del caso a:

![[Pasted image 20250423114709.png#center]]
#### Uso de las ventanas en la DFT
Dada la DFT de una secuencia $x(n): X\left( \frac{k}{NT} \right) = \sum_{n=0}^{N-1}x(nT)e^{-j \frac{2\pi}{N}nk}$, se puede expresar de forma más compacta si se hace el siguiente cambio de variables:
$$\frac{n}{NT} \to n \qquad kT \to k  \qquad e^{-j \frac{2\pi}{N}} \to W$$
La DFT queda tal que:
$$X(n) = \sum_{k=0}^{N-1}x(kT)W_{N}^{nk}$$
![[Pasted image 20250424105424.png#center]]
**Ejemplo:**
![[Pasted image 20250424105556.png#center|600]]
![[Pasted image 20250424105621.png#center|600]]
![[Pasted image 20250424105645.png#center|600]]
![[Pasted image 20250424105705.png#center|600]]

![[Filter bank class notes.pdf]]