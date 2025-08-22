> [!Definition]
>Es una estructura que ayuda a los analistas a trabajar con los usuarios para determinar la forma en que se usará un sistema. Con una colección de casos de uso se puede hacer el bosquejo de un sistema en términos de lo que los usuarios intentan hacer con él

Este tipo de análisis es crucial para la fase de análisis de requisitos en el proceso de desarrollo de un sistema. La forma en que los usuarios utilicen un sistema le da la pauta para lo que diseñará y creará. De lo que se trata es de obtener un sistema que cumpla nuestras necesidades.
[[StarUML]]

## ¿Por qué son importantes los casos de uso?

La importancia de los casos de uso radica en que se diseña el sistema desde el propio  
punto de vista del usuario. La idea es involucrar a los usuarios en las etapas iniciales del análisis y diseño del sistema.

Centrarse en procesos, a menudo reproduce sistemas existentes, ya que nos centramos en el “como” y no en el  “porque” y en el “que”.

![[Pasted image 20240527174745.png]]
![[Pasted image 20240527174755.png]]

La meta del diagrama es proporcionar una explicación de la relación del sistema y el mundo
exterior. 

> [!Example]
> Por ejemplo en el caso de un cajero el diagrama del Caso de Uso puede corresponder a la pantalla principal y el menú disponible: retiro, consulta desaldo, etc. 
> 

Cada una de estas opciones puede representarse como un Caso de Uso separado. El cliente (fuera del sistema) está asociado con cada uno de los Casos de Uso (dentro del sistema) que planea usar.

![[Pasted image 20240527175120.png]]

## Elementos del diagrama

- Sistema: Establece el límite del sistema en relación con los actores que lo van a usar.  
- Actor: Es un rol que puede jugar una persona, otro sistema, ó un dispositivo.  
- Caso de Uso: Identifica una característica clave del sistema, expresa una meta que el sistema debe lograr.  
- Asociación: identifica la asociación entre actores y Casos de Uso. Cada asociación es un diálogo que debe explicarse con la narrativa del Caso de Uso.  
- Dependencia: Identifica una comunicación entre dos Casos de Uso.  
- Generalización: Define una relación entre dos actores ó entre dos Casos de Uso, cuando uno de los casos hereda las propiedades del otro.

## Sistema en el Caso de uso

  
- Que tanto incluiremos en el sistema?  
- Como se relaciona este sistema con otros?  
- Quien va a usar este sistema?  
- Un sistema es como un objeto con un propósito y con interfases, la implementación interna puede cambiarse sin afectar otras entidades, mientras el propósito y las interfases no cambien.  
- El propósito es la meta de la justificación del proyecto.  
- Las interfases son los canales de comunicación entre los actores fuera del sistema y las características del sistema en sí: los Casos de Uso.

•
Los estereotipos se usan en UML en los Casos de Uso, clases y paquetes.
[[Notación include]]: Cuando un Caso de Uso necesita ayuda de otro Caso de Uso, la dependencia se dibuja con una flecha punteada hacia el caso que será "usado". Es una subrutina o llamada a función.

[[Notación extend ]]: Indica que un Caso de Uso puede necesitar ayuda de otro Caso de Uso, contrario al include donde siempre la necesita.

![[Pasted image 20240527180552.png]]


## Generalización

La herencia indica que un objeto tiene desde el momento de su creación, acceso a todas las propiedades de otra clase.

Esto mismo se aplica a los actores y a los Casos de Uso, se conoce como [[generalización]] y a veces se especifica con una relación “es un”.

![[Pasted image 20240527180323.png]]


## Narrativa del Caso de Uso  

Es una descripción del Caso de Uso, que se refiere a la comunicación entre el Caso de Uso y el usuario, que puede ser un actor u otro Caso de Uso. Una narrativa debe incluir:  

- Suposiciones: Describen el estado del sistema que debe ser verdadero antes de que se pueda usar el  Caso de Uso. Estas condiciones no se prueban para el Caso de Uso. Por ejemplo, autenticación y  autorización en un sistema, un sistema típico soporta estas funciones. Cada Caso de Uso subsecuente supone que el usuario no puede acceder si no ha pasado por el chequeo de seguridad, por lo que no tendremos que incluir en cada Caso de Uso la verificación de la seguridad.

- Precondiciones: A diferencia de las suposiciones, estas condiciones si son probadas por el Caso de Uso, si no son verdaderas, no se puede continuar. Estas reglas deben conocerse, por ejemplo si se le pide a un cliente proporcionar un password, debe decirle exactamente como debe estar formado.  

- Iniciación del Caso de Uso: Hay que definir que va a iniciar el caso, sobre todo cuando éste se va a reutilizar y/o ser utilizado por varios actores.  

- Diálogo: Es una descripción paso a paso de la conversación entre el Caso de Uso (el sistema) y el usuario (un actor ú otro Caso de Uso). A menudo es útil modelar esta secuencia de eventos con un diagrama de Actividades. Por ejemplo si quieres sacar dinero de un cajero: Una vez que se pasó el Caso de Uso de seguridad y se tiene el menú de opciones, seleccionar “Retiro efectivo”. El sistema preguntará cuanto quieres sacar. Hay que escribir la cantidad en pesos, si se rebasa el permitido, el sistema dará un mensaje de error o bien si se pide una cantidad que no sea múltiplo de los billetes que maneja el cajero. Si se cumplen las restricciones del cajero, se obtendrá el dinero.

- Terminación del Caso de uso: Puede haber varias formas de terminar un caso de uso, por ejemplo si todo va por buen camino el caso de uso llegará a su fin normalmente, si no es así tendrá un fin diferente, un mensaje de error, una cancelación, etc.  

- Post-condiciones: Describen un estado del sistema que debe ser verdadero cuando el Caso de Uso termina. A veces se usa el término “garantizar”, por ejemplo al final de una transacción, exitosa o fallida, debemos notificar al usuario el estado de la transacción.