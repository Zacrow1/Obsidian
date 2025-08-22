El Desarrollo de software es Complejo y Complicado

Los problemas pequeños toleran la complacencia, la falta de penalización
inmediata lleva a la inacción. La retroalimentación negativa se acumula sutilmente y cuando se vuelve dolorosa, el problema es demasiado grande para abordarlo.
La analogía dela rana en agua gradualmente calentada: 
- El problema con las cosas pequeñas es que ninguna de ellas es lo suficientemente grande como para asustarte para actuar, pero siguen aumentando poco a poco y cuando te alarmas, el problema es demasiado difícil de manejar.
- En consecuencia, los "malos olores de diseño" se acumulan, la "deuda técnica" crece y el resultado es la "putrefacción del software".

![[Pasted image 20240429184101.png]]

Divide y vencerás: 
- Identifica partes lógicas del sistema que resuelvan cada parte del problema.
- Es más fácil con la ayuda de un experto en el dominio que ya conoce los pasos del proceso ("cómo se hace actualmente").
Resultado:
- Un Modelo del Dominio del Problema (o "modelo de dominio").


## Planos de Ingeniería de Software

Especificar problemas y soluciones de software es como escribir una tira cómica.
Desafortunadamente, la mayoría de nosotros no somos artistas, así que utilizaremos algo menos emocionante: los símbolos UML.

- El software debe ser escrito para las personas en primer lugar (Las computadoras ejecutan el software, pero el hardware se vuelve obsoleto rápidamente)
- Un software útil y bueno perdura en el tiempo 
- Para cuidar el software, las personas deben ser capaces de entenderlo.

## Métodos de desarrollo de software

**Método = estrategia de trabajo**
- El algoritmo de resolución de problemas de Feynman:
	1. Escribe el problema
	2. Piensa intensamente
	3. Escribe la respuesta.
- Waterfall (Cascada)
	- Unidireccional, completar esta etapa antes de pasar a la siguiente.
- Iterativo + Incremental
	- Desarrollar incrementos de funcionalidad, repetir en un bucle de retroalimentación.
- Agile (Ágil)
	- La retroalimentación continua del usuario es esencial; bucles de retroalimentación en varios niveles de granularidad.

![[Pasted image 20240429190216.png]]

  
- Utiliza diagramas informales, ad-hoc y dibujados a mano en las etapas iniciales y  
dentro del equipo de desarrollo.  
	 El dibujo a mano obliga a economizar y lleva a una baja inversión emocional.  

- Economizar se enfoca en las consideraciones esenciales y más importantes.  
	Prioriza el contenido sobre la forma.  	

- No estar demasiado involucrado facilita la crítica y las modificaciones sugeridas.  
	Siempre toma una captura de pantalla para conservar registros para el futuro.  

- Utiliza diagramas estandarizados, ordenados y generados por computadora cuando se haya alcanzado un consenso y los diseños hayan "estabilizado".  
	 Los estándares como UML facilitan la comunicación con una amplia gama de partes interesadas.  
	 Pero invierte esfuerzo en hacer diagramas ordenados y pulidos solo cuando haya acuerdo sobre el diseño, de modo que este esfuerzo valga la pena.  
		• Invierte en la forma solo cuando el contenido valga tal inversión.


## Sistema a desarrollar  
- Actores  
	- Agentes externos al sistema que interactúan con él  
- Conceptos/Objetos  
	- Agentes que trabajan dentro del sistema para hacerlo funcionar  
- Casos de Uso  
	- Escenarios para usar el sistema

Evaluar la factibilidad o calidad de un diseño requiere un gran conocimiento del dominio (¡y conocimiento común también!).

## Medición de Software

Qué medir?  
- Proyecto (trabajo de los desarrolladores)
	para la presupuestación y planificación.
- Producto
	para la evaluación de calidad.