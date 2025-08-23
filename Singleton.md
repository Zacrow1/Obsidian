- Nombre del patrón 
	- Singleton (único) 
- Problema 
	- Se asegura de que una clase tenga solo una instancia y cómo proporcionar un acceso global a esa instancia.

![[Pasted image 20240826181831.png]]

![[Pasted image 20240826181841.png]]

![[Pasted image 20240826181855.png]]

- Solución 
	- Singleton implica crear una clase con un constructor privado que evita que se instancie directamente. La clase también contiene una **variable estática** privada que almacena la única instancia de la clase. Se proporciona un método público estático para acceder a esta instancia, y si no existe, se crea la instancia antes de devolverla.
![[Pasted image 20240826182105.png]]

![[Pasted image 20240826182445.png]]

![[Pasted image 20240826182502.png]]

### Lazy Loading 
En el patrón Singleton se proporciona un método público estático para acceder a una instancia, y si no existe, se crea la instancia antes de devolverla. Este comportamiento se llama Lazy Loading (carga deferida). Puede ayudar a mejorar el rendimiento de una aplicación ya que reduce/retarda la utilización de recursos (posiblemente “caros”) hasta que realmente se necesiten (carga bajo demanda). Así se reduce la carga inicial y se optimiza el uso de recursos (por ejemplo, memoria).

##### **Consecuencias**
Control sobre la instancia única de una clase, la facilidad de acceso global a esta instancia y la posibilidad de diferir la creación de la instancia hasta que sea realmente necesario. Introduce acoplamiento a las partes relacionadas. Recordemos que una variable global es enemiga de la encapsulación.

![[Pasted image 20240826182610.png]]