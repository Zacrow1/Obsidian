---
banner: Areas/Universidad/All things/attachments/Pasted image 20240819184235.png
sticker: emoji//2692-fe0f
---
Este principio es solo uno de los principios SOLID en el OOP.
- S - Single Responsibility Principle
- O - Open/Closed Principle (Principio de Código Abierto/Cerrado)
- L - Liskov Substitution Principle (Principio de Sustitución de Liskov) 
- I - Interface Segregation Principle (Principio de Segregación de Interfaz)
- D - Dependency Inversion Principle (Principio de Inversión de Dependencias)

Los principios SOLID son un conjunto de cinco principios guía para diseñar software de manera más eficiente, flexible y mantenible.
Cada letra en SOLID representa un principio específico que se enfoca en diferentes aspectos del diseño de software.

![[Pasted image 20240819191721.png]]

### S - Single Responsibility Principle

Este principio sugiere que una clase o módulo debería tener una única razón para cambiar. 
En otras palabras, una clase debería tener una única responsabilidad o tarea.
Esto ayuda a mantener el código más organizado y facilita el mantenimiento y la comprensión.

Este principio esta relacionado a otro principio llamado Separation Of Concerns (SOC separacion de preocupaciones).

El SOC permite dividir el software en partes más pequeñas y cohesivas, cada una responsable de una tarea concreta

![[Pasted image 20240819191858.png]]

![[Pasted image 20240819191920.png]]
![[Pasted image 20240819191936.png]]


### O - Open/CIosed Principle
Este principio establece que las entidades de software (clases, módulos, etc.) deberían estar abiertas para la extensión pero cerradas para la modificación.
Esto significa que puedes agregar nuevas funcionalidades sin modificar el código existente.

Esto promueve la reutilización y evita cambios que puedan introducir errores en partes ya funcionales.

![[Pasted image 20240819192059.png]]

### L - Liskov Substitution Principle
Introducido por Barbara Liskov (1987). Según este principio, las clases derivadas deben ser sustituibles por sus clases base sin cambiar el comportamiento deseado del programa.
En otras palabras, una subclase debe poder usarse en lugar de su clase base sin causar
problemas.

![[Pasted image 20240819192153.png]]

![[Pasted image 20240819192201.png]]![[Pasted image 20240819192245.png]]

### I - Interface Segregation Principle

Este principio propone que las interfaces de una clase deberían estar enfocadas en las necesidades específicas de los clientes.
 
No se debería obligar a las clases a implementar métodos que no necesitan.

Esto ayuda a evitar interfaces sobrecargadas y promueve una estructura más clara y modular. 

Para esto podemos segregar comportamiento mediante interfaces

![[Pasted image 20240819192335.png]]

![[Pasted image 20240819192343.png]]

![[Pasted image 20240819192417.png]]

### D - Dependency Inversion Principle

Este principio plantea que las dependencias de alto nivel no deberían depender de detalles de bajo nivel. 

En lugar de eso, ambos niveles deberían depender de abstracciones.

Esto ayuda a reducir la interdependencia entre componentes y hace que el sistema sea más flexible y adaptable.

![[Pasted image 20240819192553.png]]
![[Pasted image 20240819192652.png]]


