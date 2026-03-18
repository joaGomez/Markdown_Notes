

![[Pasted image 20240312115430.png#center|500]]
Cálculo aproximado de la inductancia, sin tener en cuenta la dispersión del flujo, o la tensión del bobinado, etc.

![[Pasted image 20240312120606.png#center|400]]
Cálculo de la reluctancia total. Al añadirle un gap al transformador, si tengo un $\mu_{r}$ muy grande, sin importar que varía un poco, al agregarle el término del gap, esa variación se ve reducida.

> **Obs:**
> ![[Pasted image 20240312121433.png#center|400]]
> Aquí vemos como se ve el ciclo de histéresis corrido por el gap añadido.

|                                                                            Teoría                                                                             |                                                                                                                        Realidad                                                                                                                        |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                       Todo el flujo magnético se concentra en el núcleo                                                       |                                                                                            Hay flujo disperso alrededor de los cables, entrehierro y núcleo                                                                                            |
|                    Toda la tensión de entrada se reparte en las N espiras por igual. Todo el flujo magnético está encerrado en el núcleo.                     |                                                                Hay pérdidas de tensión por ley de Ohm en los cables ($R*i$). Hay FEM inducidas en el núcleo. Efectos Skin y proximidad.                                                                |
| Toda la corriente se concentra en el bobinado. Todo el H se reparte uniformemente por el núcleo. Todas las líneas de flujo magnético recorren el mismo camino | Hay corrientes parásitas en el núcleo por efecto Foucault (Eddy Currents). El núcleo no es uniforme (en forma y composición). Existen infinitos caminos distintos para que se cierren las líneas de campo, pero sólo  se toma la “promedio” $l_{mag}$. |


**Tarea:** 
- ¿Por qué se usan núcleos de hierro de hasta 400hz?
- Laminaciones de hierro para transformadores en el mercado local: Precio, tipos, proveedores, etc.
- ¿Cómo se especifican las pérdidas en el hierro?

