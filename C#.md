---
aliases:
  - Csharp
---
### Venís de [[2.3 Programación 3]]

# C#'

> [!question] ¿Que es C#?
> C# es un lenguaje de programación moderno. Se introdujo en 2002. C# es un lenguaje de programación multiplataforma.  Las aplicaciones C# se pueden ejecutar en cualquier sistema operativo que tenga la plataforma .NET instalada. Es mas utilizado junto al paradigma Orientado a objetos. Se utiliza para crear una amplia gama de aplicaciones, desde aplicaciones web y móviles hasta aplicaciones empresariales.

### Organización de una aplicación en C#
Una aplicación de C# se organiza de la siguiente manera: • Una solución contiene uno o varios proyectos. • Cada proyecto contiene uno o varios namespaces. • El código fuente de una aplicación se coloca en los namespaces de los proyectos.

![[Pasted image 20250106162134.png]]
### Archivo de proyecto

Un proyecto es un conjunto de archivos relacionados que se utilizan para crear una aplicación, una biblioteca o una herramienta. 
Un proyecto puede contener código fuente, archivos de configuración, archivos de recursos y otros archivos.

Los proyectos se pueden guardar en un archivo con la extensión .csproj.  Estos archivos son de tipo XML. Definen la estructura del proyecto, dependencias y configuraciones de compilación

### Archivo de solución

Una solución es un conjunto de proyectos que están relacionados entre sí. Una solución puede contener proyectos de diferentes tipos, como proyectos de aplicaciones, proyectos de bibliotecas, proyectos de pruebas, etc. 
Las soluciones se pueden guardar en un archivo con la extensión .sln.

Al igual que los proyectos (.csproj), las soluciones se pueden abrir y cerrar en Visual Studio. (Entorno de desarrollo integrado para lenguajes .NET)

![[Pasted image 20250106162544.png]]

### Namespaces

Un Namespaces es como la dirección específica para encontrar tipos de datos. Por ejemplo, "System.Console.WriteLine" le dice al compilador dónde encontrar el método "WriteLine" en el espacio de nombres "System". Importar un espacio de nombres simplifica el código al permitir el acceso a tipos sin usar un prefijo de espacio de nombres y mejora la experiencia del programador mostrando las opciones disponibles mientras escribes código.
Simplifica el código al permitir el acceso a tipos sin usar un prefijo de espacio de nombres y mejora la experiencia del programador mostrando las opciones disponibles mientras escribes código.
![[Pasted image 20250106162624.png]]

### Namespaces implícitos 
Tener estas declaraciones global using significa que solo se necesitan importar en un archivo .cs y pueden ser utilizados en el proyecto
![[Pasted image 20250106162701.png]]
![[Pasted image 20250106162709.png]]

### El método main
Es el punto de entrada de un programa ejecutable; es donde se inicia y finaliza el control del programa. Main se declara dentro de una clase o estructura. El valor de Main debe ser static y no public. Es bastante similar en comparación con Java.

![[Pasted image 20250106162737.png]]
![[Pasted image 20250106162751.png]]

### Declaración de variables
![[Pasted image 20250106162821.png]]
![[Pasted image 20250106162834.png]]
![[Pasted image 20250106162843.png]]
![[Pasted image 20250106162856.png]]
![[Pasted image 20250106162909.png]]

### Sistema de tipos
El Common Type System (CTS) es un conjunto de reglas y definiciones que describen los tipos de datos que se pueden utilizar en C#. El CTS define los tipos de datos primitivos, las estructuras, las clases, las enumeraciones, los tipos de referencia y los tipos de valor. A continuación exploraremos mas sobre la clasificación de tipos por valor y por referencia.

![[Pasted image 20250106162933.png]]

### Tipos por valor y por referencia 
Los tipos de valor derivan de System.ValueType, se almacenan los datos de forma directa en la pila (stack). Cuando se asigna una variable de tipo valor a otra variable, se copia el valor de la primera variable a la segunda. Al declarar una variable de un reference type, contiene el valor null hasta que se asigna un valor (p. ejem. usando el operador new). Cuando se asigna una variable de tipo referencia a otra variable, se copia la referencia de la primera variable a la segunda.

![[Pasted image 20250106163016.png]]

![[Pasted image 20250106163027.png]]

### Resumen de manejo de tipos de datos
Existen algunas pequeñas diferencias en cuanto a la sintaxis, por ejemplo en C# puedes usar string o String, la forma que se imprime en consola, el uso de namespaces, etc. En su gran mayoría se podría decir que tanto Java y C# son bastante similares en este aspecto

![[Pasted image 20250106163102.png]]

![[Pasted image 20250106163119.png]]
![[Pasted image 20250106163129.png]]
![[Pasted image 20250106163138.png]]
![[Pasted image 20250106163147.png]]
![[Pasted image 20250106163218.png]]
![[Pasted image 20250106163940.png]]
![[Pasted image 20250106164054.png]]
![[Pasted image 20250106164101.png]]

### Boxing y unboxing
La conversión boxing es una conversión implícita de un tipo por valor en el tipo object o en cualquier tipo de interfaz implementado por este tipo de valor. Al aplicarla se asigna una instancia de objeto en el heap y se copia el valor en el nuevo objeto. La conversión unboxing es una conversión explícita del tipo object en un tipo por valor. Primero comprueba si el tipo del valor de unboxing es del tipo guardado en el heap y después copia el valor de la instancia en la variable de tipo por valor.

![[Pasted image 20250106164144.png]]

![[Pasted image 20250106164200.png]]
![[Pasted image 20250106164209.png]]

![[Pasted image 20250106164234.png]]

