## 1. Dieléctricos

Un **dieléctrico** es un material sin cargas libres apreciables, pero con **cargas ligadas** que pueden desplazarse microscópicamente ante un campo eléctrico externo.

Ante un campo eléctrico:
- No se produce corriente
- Se genera separación de cargas
- Aparecen dipolos eléctricos inducidos

El material permanece globalmente neutro.

---
## 2. Polaización $\vec{P}$

La **polarización** se define como el **momento dipolar eléctrico por unidad de volumen**:
$$
\vec{P} = \frac{1}{V} \sum \vec{p}
$$
Interpretación física:
- Mide el grado de dipolarización del medio
- Resume macroscópicamente el comportamiento microscópico

Unidades:
$$
[\vec{P}] = \text{C/m}^2
$$

---
## 3. Polarizabilidad microscópica

A nivel atómico o molecular, un campo eléctrico $\vec{E}$ induce un dipolo eléctrico:

$$
\vec{p} = \alpha \vec{E}
$$
donde:
- $\vec{p}$ es el momento dipolar inducido
- $\alpha$ es la **polarizabilidad** del átomo o molécula

La polarizabilidad cuantifica qué tan fácilmente se deforma la distribución de cargas.
### Tipos de polarización
- **Electrónica**: deformación de la nube electrónica  
- **Iónica**: desplazamiento relativo entre iones  
- **Orientacional**: alineación de dipolos permanentes (dependiente de la temperatura)

---
## 4. Relación entre $\vec{P}$ y $\vec{E}$

Si hay $N$ dipolos por unidad de volumen:
$$
\vec{P} = N \alpha \vec{E}
$$
Se define la **susceptibilidad eléctrica** $\chi_e$:
$$
\vec{P} = \varepsilon_0 \chi_e \vec{E}
$$
Relación microscópica–macroscópica:

$$
\chi_e = \frac{N \alpha}{\varepsilon_0}
$$
---

## 5. Campo desplazamiento eléctrico $\vec{D}$

Se define el campo:
$$
\vec{D} = \varepsilon_0 \vec{E} + \vec{P}
$$
Su objetivo es separar el efecto de las **cargas libres** del de las **cargas ligadas**.

Ley de Gauss macroscópica:

$$
\nabla \cdot \vec{D} = \rho_{\text{libre}}
$$

---

## 6. Cargas de polarización

La polarización genera **cargas ligadas**.
### Densidad volumétrica de carga ligada
$$
\rho_p = - \nabla \cdot \vec{P}
$$

Aparece cuando la polarización no es uniforme.
### Densidad superficial de carga ligada
$$
\sigma_p = \vec{P} \cdot \hat{n}
$$
Aparece en superficies o interfaces del dieléctrico.

El dieléctrico es globalmente neutro; las cargas de polarización no producen corriente.

---

## 7. Medio lineal, isótropo y homogéneo

En este caso:
$$
\vec{D} = \varepsilon \vec{E}
$$
con:
$$
\varepsilon = \varepsilon_0 (1 + \chi_e)
$$
---
## Frases clave para el examen oral

- La polarización representa el efecto colectivo de dipolos inducidos en el material.
- Las cargas de polarización no son libres; aparecen donde varía la polarización.
- El campo $\vec{D}$ permite escribir las ecuaciones de Maxwell en función de cargas libres.
