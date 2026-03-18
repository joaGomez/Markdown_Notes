### Símbolos de transitores MOS

![[Facultad/2026/Microelectrónica/Complementos/Simbolos_MOSFET.png#center|536]]

### Zonas de operación

![[Facultad/2026/Microelectrónica/Complementos/zonas_operacion_mosfet.png#center|282]]

|    Zona    |                    Condición                    |                               Corriente de Drain ($I_{D}$)                               |                   Función                   |
| :--------: | :---------------------------------------------: | :--------------------------------------------------------------------------------------: | :-----------------------------------------: |
|   Triodo   | $V_{GS}>V_{T} \, \wedge \, V_{DS}<V_{GS}-V_{T}$ | $K_{p}\cdot \frac{W}{L} \left( (V_{GS}-V_{T})\cdot V_{DS}- \frac{V_{DS}^{2}}{2} \right)$ |     Resistencia controlada por $V_{GS}$     |
| Saturación | $V_{GS}>V_{T} \, \wedge \, V_{DS}>V_{GS}-V_{T}$ |                $\frac{1}{2}\cdot K_{p}\cdot \frac{W}{L}(_{GS}-V_{T})^{2}$                | Fuente de corriente controlada por $V_{GS}$ |
### Inversor
