### Principio de la conservación de la energia mecánica
$$
\frac{dU_{em}}{dt} = - \int_{V} \left( \vec{E}\cdot \frac{ \partial\vec{D}}{\partial t} + \vec{H}\cdot \frac{ \partial\vec{B}}{\partial t} \right)  \, dV =\int_{V} \vec{E}\cdot \vec{J}  \, dV + \oint_{A} (\vec{E}\times \vec{H})\cdot d\vec{A}
$$
Donde $\vec{S}= \vec{E}\times \vec{H}$ es el **vector de poynting**, y es la potencia por unidad de área.

Dado que $u_{em} = \frac{1}{2} \varepsilon E^{2} + \frac{1}{2} \mu H^{2}$, entonces:
$$
\int_{V} \vec{E}\cdot \vec{J}  \, dV  = - \frac{d}{dt}\int_{V} (\frac{1}{2} \varepsilon E^{2} + \frac{1}{2} \mu H^{2})  \, dV - \oint_{A} \vec{S}\cdot d\vec{A}
$$
![[Pasted image 20250918211046.png#center|350]]
**Observaciones:**
- Si $J\cdot E>0$ → El sistema pierde energía (potencia disipada).
- Si $J\cdot E<0$ → El sistema gana energía energía electromagnética (generador).
### Polarización de un dieléctrico por ondas electromagnéticas
A partir del modelo de Lorentz, que vincula el campo en un dieléctrico con una respuesta armónica, tenemos que:
$$
\begin{split}
& \vec{P} = \varepsilon_{0}\mathcal{X}_{e}(\omega)\vec{E} \\ 
& \vec{D} = \varepsilon(\omega)\vec{E}
\end{split}
$$
Donde
$$
\varepsilon_{r}(\omega) = \frac{\varepsilon(\omega)}{\varepsilon_{0}} = 1 + \frac{\omega_{p}^{2}}{(\omega_{0}^{2}-\omega^{2})+j\omega \Gamma}
$$
Con $\omega_{p}^{2} = \frac{Nq^{2}}{\varepsilon_{0}m}$ la frecuencia del plasma.

Además, se cumple la siguiente relación de permitividad compleja:
$$
\varepsilon_{r}(\omega) = \varepsilon_{r}'(\omega)-j\varepsilon_{r}''(\omega)
$$
#### Comportamiento con la frecuencia
| Frecuencia |   $\omega$   |   $\phi_{e}$    |                 $\mathcal{X}_{e}$                  |                  $\varepsilon_{r}'$                  |            $\varepsilon_{r}''$             |
|:---------- |:------------:|:---------------:|:--------------------------------------------------:|:----------------------------------------------------:|:------------------------------------------:|
| Bajas      |     $0$      |       $0$       | $\left( \frac{\omega_{p}}{\omega_{0}} \right)^{2}$ | $1+\left( \frac{\omega_{p}}{\omega_{0}} \right)^{2}$ |                     0                      |
| Resonancia | $\omega_{0}$ | $\frac{\pi}{2}$ |     $\frac{\omega_{p}^{2}}{\Gamma \omega_{0}}$     |                         $1$                          | $\frac{\omega_{p}^{2}}{\Gamma \omega_{0}}$ |
| Altas      |   $\infty$   |   $0$ o $\pi$   |                        $0$                         |                         $1$                          |                    $0$                     |
La curva de variación de la permitividad en función de la frecuencia está dada por:
$$
\varepsilon_{r}'(\omega) = 1 + \frac{\omega_{p}^{2}(\omega_{0}^{2}-\omega^{2} )}{(\omega_{0}^{2}-\omega^{2} )^{2}+\Gamma^{2}\omega^{2}} 
\qquad \wedge \qquad \varepsilon_{r}''(\omega) = \frac{\omega_{p}^{2}\,\omega\, \Gamma}{(\omega_{0}^{2}-\omega^{2} )^{2}+\Gamma^{2}\omega^{2}}
$$
![[Pasted image 20250918230503.png#center|300]]
#### Variación armónica
Por Ampère-Maxwell se define la variación armónica como:
$$
\nabla \times \vec{H}= j\omega\varepsilon_{0}\vec{E}\left( \varepsilon_{r}-j \frac{\sigma}{\omega\varepsilon_{0}}\right) = j\omega\varepsilon_{0}\varepsilon_{c}\vec{E} = \sigma \vec{E}+j\omega\varepsilon_{c}\vec{E}
$$
Donde $\varepsilon_{c}=\varepsilon_{r}-j \frac{\sigma}{\omega\varepsilon_{0}}$.

**Conductividad efectiva:** Se define como $\sigma_{ef} = \sigma_{cc} +\omega\varepsilon'' \simeq \omega\varepsilon''$.
**Tangente del ángulo de pérdidas:** Se define como la habilidad de un determinado material para absorber la energía electromagnética y convertirla en calor a una determinada frecuencia y temperatura.
$$
tg(\delta_{c}) = \frac{\varepsilon''}{\varepsilon'}
$$
La potencia disipada por unidad de volumen en el medio está dada por:
$$
w = \vec{J}\cdot \vec{E} = \sigma_{ef} |E|^{2} = \sigma_{cc}|E|^{2}+\omega\varepsilon''|E|^{2}
$$
#### Horno de microondas
$$
\langle P\rangle_{abs} = \varepsilon''\omega E_{rms}^{2}\cdot Vol
$$
La tasa de aumento de temperatura en un dieléctrico debido a un campo electromagnético está dada por:
$$
\frac{dT}{dt} = k  \frac{\varepsilon''fE_{rms}^{2}}{\rho \,c_{p}}
$$
### Permeabilidad compleja
En forma similar al campo eléctrico, el campo magnético enfrenta fuerzas moleculares que requieren realizar un trabajo para magnetizar un determinado material. 

Se define la permeabilidad compleja como:
$$
\mu_{c} = \mu'-j\mu''
$$
#### Valor medio temporal
$$
\langle\vec{S}(t)\rangle = \frac{1}{T} \int_{0}^{T} \vec{E}(t)\times \vec{H}(t)  \, dt = \frac{1}{2} Re(\vec{E}\times \vec{H})
$$
#### Potencia disipada
Para un campo armónico
$$
\left\langle \frac{dP}{dV} \right\rangle = \frac{1}{2} Re(\vec{J}\cdot \vec{E}) = \frac{1}{2} \omega\varepsilon''|E_{0}|^{2}
$$
#### Vector de Poynting en una onda electromagnética
$$
\vec{S}(r,t) = \pm \frac{E^{2}(r,t)}{\eta_{0}} \hat{z} 
\to \langle \vec{S}(r,t) \rangle = \pm \frac{E^{2}(r)}{2\eta_{0}} \hat{z}
$$
