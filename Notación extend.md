#### venís de: [[Casos de uso]]

## Evaluar los casos de Uso para dependencias tipo extend

- Un Caso de Uso puede o no usar otro Caso de Uso dependiendo de una cierta condición. Cuando la condición se cumpla se llama al otro Caso de Uso, sino, no se llama. 
- Si en el ejemplo se quisiera aumentar un producto en el inventario sin tenerlo que colocar en una de las ubicaciones predefinidas, sin tener que pasar por el Caso AlmacenarProducto. El Caso RecibirProducto tendría que solicitar permiso para llamar ActualizarInventario.

![[Pasted image 20240527181345.png]]

