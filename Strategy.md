## Problema

En el diseño de software, a menudo nos enfrentamos a la necesidad de cambiar el comportamiento de una clase en función de ciertas condiciones o contextos. Hacer esto mediante la creación de múltiples clases derivadas o utilizando múltiples condicionales puede llevar a código complicado y difícil de mantener.

![[Pasted image 20240826185108.png]]

![[Pasted image 20240826185129.png]]

![[Pasted image 20240826185139.png]]



## Solución 

- El patrón Strategy define una familia de algoritmos o estrategias encapsulados en clases separadas. 
- Cada estrategia implementa una versión específica del algoritmo.
- Luego, una clase "Contexto" tiene una referencia a una de estas estrategias y utiliza la estrategia actual para realizar la operación deseada

![[Pasted image 20240826185241.png]]

![[Pasted image 20240826185254.png]]


## Consecuencias 
- Intercambiabilidad: permite cambiar el comportamiento de un objeto en tiempo de ejecución al cambiar la estrategia que utiliza.
- Desacoplamiento: El patrón desacopla las clases que implementan las estrategias de la clase Contexto, lo que facilita cambios en las estrategias sin afectar al cliente.
- Reusabilidad: Diferentes estrategias pueden ser reutilizadas en diferentes contextos, lo que promueve la reutilización de código.
- Mayor flexibilidad: La capacidad de cambiar estrategias fácilmente facilita la adaptación a cambios en los requisitos o condiciones.