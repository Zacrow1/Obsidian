---
"Venis de:":
---
Provenís de: [[1.11 Programación 2]]

> [!NOTE] Definición
> Un patrón de diseño es como una receta reutilizable para resolver problemas comunes en el diseño de software. Imagina que estás cocinando y sigues una receta para hacer galletas. La receta te dice los ingredientes que necesitas y los pasos a seguir en un orden específico.
 > De manera similar, un patrón de diseño es una guía que proporciona soluciones probadas y efectivas para desafíos típicos en la creación de software.

Los patrones de diseño ayudan a los desarrolladores a abordar problemas
comunes de manera consistente y eficiente, ya que han sido desarrollados y refinados a lo largo del tiempo por expertos en diseño de software. Cada patrón se enfoca en un problema específico y ofrece una estructura general una forma de organizar el código para resolver ese problema de manera efectiva. Adoptar patrones de diseño facilita la comunicación entre los miembros del equipo y permite crear sistemas más mantenibles y escalables. En esencia, los patrones de diseño son como "soluciones probadas" para desafíos recurrentes en el desarrollo de software.

# Patrones
### Creacionales

*Inicialización y configuración clases y objetos*
	- Abstraen el proceso de instanciación (creación de objetos): 
	- Encapsula información sobre las clases concretas. 
	- Esconde como estas clases concretas son creadas o combinadas 
	- Buscan mejorar la flexibilidad y la reutilización de código.
	- La flexibilidad se refiere a los cambios en los tipos de objetos creados o en la forma en que se crean. 	
	
	[[Singleton]]
	[[Factory Method]]
---
### Estructurales

*Composición y ensamblaje de objetos*
	- Se centran en cómo componer objetos y clases para formar estructuras más grandes y complejas. 
	- Definen relaciones y conexiones entre objetos, facilitando la organización y el diseño de sistemas más flexibles y eficientes.
	
	[[Facade]]
---
### Comportamiento

*Responsabilidad e interacción*
	- Se centran en cómo los objetos y las clases interactúan y comunican entre sí para lograr un comportamiento eficiente y flexible en un sistema. 
	- Abordan problemas relacionados con la comunicación, la responsabilidad y el flujo de control en el software.
	
	[[Strategy]]
	[[Observer (Patron de Diseño]]
--- 
# Estructura de un Patrón de Diseño

## Estructura 
El [[GoF]] propone estos elementos generales en un DP: 

- Nombre del patrón
	- Es un nombre descriptivo que identifica el patrón y facilita su comunicación y comprensión. 
- Problema 
	- Describe el contexto o la situación en la que se aplica el patrón. Explica qué problema o desafío común está tratando de resolver.
- Solución
	- Detalles de la solución general que aborda el problema. Esto incluye las clases y objetos involucrados, sus relaciones, estructura y colaboración.
- Consecuencias 
	- Indica las ventajas y desventajas de aplicar el patrón. Esto incluye cómo afecta al diseño, la flexibilidad, el rendimiento y otros aspectos del sistema.

> [!Example]
> - Nombre del patrón 
> 	- Singleton 
>  - Problema 
> 	 - Se asegura de que una clase tenga solo una instancia y cómo proporcionar un acceso global a esa instancia.
> - Solución 
> 	- Singleton implica crear una clase con un constructor privado que evita que se instancie directamente. La clase también contiene una variable estática privada que almacena la única instancia de la clase. Se proporciona un método público estático para acceder a esta instancia, y si no existe, se crea la instancia antes de devolverla. 
> - Consecuencias 
> 	- Control sobre la instancia única de una clase, la facilidad de acceso global a esta instancia y la posibilidad de diferir la creación de la instancia hasta que sea realmente necesario. Introduce acoplamiento a las partes relacionadas.

El libro de [[GoF]] identificó y describió 23 patrones de diseño (DP) diferentes, categorizándolos (principalmente) en tres grupos según su propósito: 





