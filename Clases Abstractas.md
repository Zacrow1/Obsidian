## Clases Abstractas e Interfaces
- Abstracción: es un proceso para esconder detalles de implementación y exponer solo funcionalidad al usuario.
- Dos maneras de abstracción son:
	- Clase Abstracta
	- Interface

### Clase Abstracta 

- Supongamos que empezamos haciendo algún trabajo con la idea de que el trabajo restante lo haga alguien mas.
- De manera similar, una clase abstracta es una clase incompleta. No podemos instanciar objetos de este tipo de clases.
- Una sub clase de esta clase abstracta debe completar el "trabajo pendiente", redefiniendo algunos de los métodos (usando sobreescritura overriding)
- Una clase abstracta espera que sus clases **concretas complementen** su estructura y comportamiento, implementando las **operaciones abstractas**.
- Una clase se declara con el keyword **abstract** 
- Es una clase restringida de la cual no se puede instanciar objetos (debe usarse **herencia** mediante una sub clase).
- Una clase abstracta puede tener métodos abstractos y no-abstractos.
- No puede ser instanciada. Necesitar ser extendida y sus métodos implementados.
- Puede tener constructores y métodos estáticos.
- Puede tener métodos finales, quelas sub clases **no pueden extender**.

```java
abstract class 
	ClassName{
		...
	}
```
![[Pasted image 20240715180345.png]]
![[Pasted image 20240715180938.png]]
![[Pasted image 20240715181711.png]]
![[Pasted image 20240715181744.png]]
La clase abstractaAnimal permite reutilizar el mismo c0digo base (emitSound , que no puede ser modificado.)
Las sub clases deben simplemente implementar los métodos abstractos requeridos.

Clase Abstracta — Principio Open Closed 
(Abierto / Cerrado)

En OOP, el principio open—closed (OCP) indica:

- "Las entidades de Software (clases, módulos, funciones, etc.) deberían estar abiertas para extensión, pero cerradas para modificación' 
- Una entidad debería permitir que su comportamiento pueda ser **extendido**, sin modificar su **código fuente**.
### Interfaces

- En Java, una interfaces es una plantilla de una clase.
- La interface es un mecanismo para **articularla abstracción**.
- Solamente pueden existir métodos abstractos en una interface Java, sin implementación de los mismos.
- Una clase hija extiende una clase padre (extends).
- En una interface, declaramos que queremos hacer (implementar), pero no especificamos como lo haremos.
- Son similares a las clases, pero sin atributos de instancia y con métodos sin implementación (como métodos abstractos).

![[Pasted image 20240715183944.png]]
![[Pasted image 20240715184728.png]]
![[Pasted image 20240715184937.png]]
![[Pasted image 20240715185716.png]]
![[Pasted image 20240715190030.png]]
![[Pasted image 20240715190155.png]]
![[Pasted image 20240715190922.png]]
![[Pasted image 20240715191027.png]]

```
interface
	InterfaceName{
	...
	}
```

## Diferencias entre clases e interfaces
| Característica            | Clase                                                                               | Interfaz                                                                             |
| ------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Instanciación             | Se pueden instanciar                                                                | No se pueden instanciar                                                              |
| Métodos                   | Pueden tener métodos concretos (con implementación) y abstractos                    | Solo métodos abstractos                                                              |
| Especificadores de acceso | Se pueden definir diferentes especificadores de acceso (private, protected, public) | Solo el especificador public                                                         |
| Herencia                  | Una clase solo puede heredar de una clase padre                                     | Una clase puede implementar múltiples interfaces                                     |
| Implementación            | La implementación de los métodos se define en la clase                              | La implementación de los métodos se define en las clases que implementan la interfaz ||
## Interfaces vs. Abstract Class

- Cuando usar una clase abstracta?
	- Cuando se quiere aplicar el concepto de herencia (para compartir código entre clases), brindando métodos de clase base que pueden ser extendidos por las subclases (override) 
	- Cuando nuestro problema implica "A es un B" (IS-A) 
	- Si se tienen requerimientos y solo algunos detalles parciales de implementación.

![[Pasted image 20240715192340.png]]