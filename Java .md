
[[1.3 Programación 1]]

---

Características principales de Java
Es un lenguaje de alto nivel.
Está orientadoa objetos.
Sigue el paradigma imperative.
Soporta multithreading.
Gestión automática de memoria (Garbage
Collection).
Independencia de la plataforma (Architecture
Neutral).
Write Once, Runs Everywhere (WORA).
Ejecución multiplataforma.
Portable.

```embed
title: "Ejercicios sobre operadores lógicos Java"
image: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgjIl3TqF3wVdGcKg9dOBELtZEINV1-KVyuNlsWkwVOGYZGBC6WWJZyKR_Ny7NaPj3HmwZZ_daOdyj4-4ilLMS4rqavc32_8QZbI9-Ko99i7uEIcW7oMfRVHjwpvy2_62_d8Siw3M18k64Dq70h2RHWLi4hpiWCrkYdU-NCXO4154L0dJJkOnRQ_CLzD2Qt/w1200-h630-p-k-no-nu/portada%20kindle.jpg"
description: "Tutorial Java. Ejercicios Básicos y avanzados de programación Java"
url: "https://puntocomnoesunlenguaje.blogspot.com/2018/09/ejercicios-sobre-operadores-logicos.html"
```

![[Pasted image 20240118102116.png]]
![[Pasted image 20240118103234.png]]

## Metodos 
Un método es un bloque de código que sólo se ejecuta cuando se llama.
• Un método se representa como un proceso predefinido (subrutina) en diagramas de flujo o pseudocódigo

![[Pasted image 20240205101957.png]]
Programación modular. se origino en los 60.
 Separar la funcionalidad de un programa en independiente, modulos intercambiables de modo que contenga todo lo necesario para ejecutar solo un aspecto de la funcionalidad deseada.

La modularidad se trata de hacer bloques, y cada bloque se hace con la ayuda de otros bloques..
![[Pasted image 20240205102359.png]]
### Interger y String 

Integer.parselnt(String s)
 - este método estático se usa para poder obtener el valor primitivo int (entero) a partir de una cadena (s)
 - Este metodo puede servirte para convertir los parametros del juego de la vida
String split(String regex)
- Este metodo de clase permite dividir una cadena en cadenas múltiples dado un delimitador (para separarlas). el metodo retorna un array de strings.
- String[ ] population = "001#110#01".split("#");
- var population = "001#110#0'1".split("#");
- population = {"001","110","01"}
Este metodo puede servirte para procesar la poblacion inicial del juego de la vida y convertirla en una matriz

### Paso de parámetros
- El método ser invocado  para ejecutar su codigo
- El codigo que invoca al metodo se llama llamador del metodo.
- Los metodos en java permiten reutilizar el codigo sin tener que volver a escribirlo.

![[Pasted image 20240205105043.png]]

Un metodo es un bloque de codigo que se ejecuta cuando es llamado
![[Pasted image 20240205105102.png]]

- Paso de parametros generales
	- Los dos mecanismos mas comunes en los lenguajes de programación modernos para el paso de parametros son Pass-by-Value y Pass-by-Reference
	- Pasar por valor, el metodo del llamador y el destinatario de la llamada operan en dos variables diferentes que son copias entre si. Cualquier cambio en una variable no modifica la otra. Esto significa que al llamar a un metodo, los parametros pasados al metodo del destinatario de la llamada seran clones de los parametros originales 
 ![[Pasted image 20240205105455.png]]

- Paso de parametros en Java
	En JAVA todos los parametros se pasan por valor
	- Java admite dos tipos de datos: Tipos de [[Datos primitivos]] y Tipo de datos de referencia.

![[Pasted image 20240205105647.png]]

Parameter Passing in Java 
- En Java, todos los parametros se pasan por valor.
- Con tipos de [[Datos primitivos]], Java puede pasar los valores a los metodos por valor y valor constante
- ![[Pasted image 20240205105945.png]]
![[Pasted image 20240205110031.png]]

### Constantes 

- Inmutabilidad; En Java, las variables son mutables por defecto, lo que significa que podemos cambiar el valor que tienen. 
![[Pasted image 20240205110133.png]]

- Una constante es algo que es inmutable. Mediante el uso de la palabra clave final al declarar una variable, el compilador de Java no nos deja cambiar el valor de esa variable (Por lo tanto, podemos declarar constantes de esta manera).
![[Pasted image 20240205110248.png]]

Valor asignado una vez
• Una vez que una constante ha sido asignada con un valor, no se puede modificar durante la ejecución del programa.
• Cualquier intento de cambiar el valor de una constante resultará en un error de compilación.
• Esto asegura que los valores fundamentales en el programa permanezcan inalterables y evita errores accidentales.

Uso en tiempo de compilación  
- Las constantes son reemplazadas por sus valores  en tiempo de compilación, es decir, el compilador sustituirá todas las referencias a la constante con su valor literal antes de generar el byte code.  
- Esto puede conducir a una mejora en el rendimiento en comparación con las variables, ya que no hay acceso en tiempo de ejecución para recuperar el valor
![[Pasted image 20240205111846.png]]

Beneficios en legibilidad y mantenibilidad  
- El uso de constantes mejora la legibilidad del código, ya que los  nombres descriptivos permiten a los desarrolladores entender rápidamente el propósito y significado de los valores.  
- Además, si hay algún cambio en el valor constante, solo se requiere modificar la declaración en un lugar, lo que hace que el mantenimiento del código sea más sencillo y menos propenso a errores.
![[Pasted image 20240205112137.png]]

Convención de nomenclatura  
- Aunque Java permite cualquier nombre válido para una constante, se sigue una convención para diferenciar las constantes de otras variables.
- Los nombres de constantes se escriben completamente en mayúsculas y se separan las palabras con guiones bajos. 
- Por ejemplo, MAXIMO_VALOR, NUMERO_PI, etc.  
- Esta convención ayuda a distinguir fácilmente las constantes de las variables y métodos en el código.
### Heap y Stack

