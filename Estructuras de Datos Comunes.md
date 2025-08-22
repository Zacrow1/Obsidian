[[Conceptos de OOP]]

Las DS proporcionan métodos y operaciones
para acceder, Insertar, eliminar y manipular los
datos de manera efectiva.

> [!help] ¿Que son las estructuras de datos?
> Las estructuras de datos (DS) son formas de
organizar y almacenar datos en la memoria de una
computadora de manera eficiente.

![[Pasted image 20240722181116.png]]

DS Primitivas: DS simples que almacenan un valor, como enteros, boolean, etc.
DS No Primitivas: DS que organizan la información de
manera no primitivas, como arrays, listas, queues, etc.

Organización de datos: Las DS permiten organizar datos de manera lógica y coherente.

> [!help] ¿Para que sirven?
> La utilidad de las DS radica en su capacidad para
resolver problemas específicos de manera
eficiente.

Eficiencia en operaciones: Cada DS tiene sus propias
características y propiedades que hacen que ciertas
Cual es mas lógico y coherente cuando queremos tener un problema con una serie de valores?

Al elegir la DS adecuada, puedes optimizar el rendimiento del programa.

![[Pasted image 20240722181528.png]]
![[Pasted image 20240722181745.png]]
![[Pasted image 20240722181919.png]]

Los arboles son mejores para representar jerarquías.

Las DS proporcionan abstracciones que simplifican la
resolución deproblemas.

## ¿Que es CRUD?
aplicaciones modernas.

La gestión de datos  es una necesidad común en las principales operaciones sobre datos se pueden resumir como CRUD:

CREATE: Creación de datos
READ: Lectura de Datos
UPDATE: Actualización de Datos
DELETE: Eliminación de Datos

## Collections Framework

EI Collections Framework de Java (CF) es una biblioteca Integrada que proporciona un conjunto de interfaces, clases y algoritmos para gestionar y manipular colecciones de objetos (DS específicas).

Encontramos el CF dentro del package base de Java java.util. La manipulación Incluye el CRUD de datos,
y algunas aplicaciones adicionales

![[Pasted image 20240722182334.png]]


```java
import java.util.collections
```

EI CF ofrece una amplia gama de DS y utilitarios para almacenar, organizar y acceder a datos de manera eficiente.
Incluye componentes listos para ser extendidos y utilizados

![[Pasted image 20240722182907.png]]

EI CF proporciona ofrece algoritmos y métodos de utilidad para búsqueda, ordenación y manipulación de
colecciones.

## List

EI CF está diseñado con genéricos, 10 que permite que las colecciones sean seguras en cuanto a tipos, asegurando la comprobación de tipos en tiempo de compilación y reduciendo el riesgo de errores en tiempo de ejecución.
![[Pasted image 20240722183422.png]]
![[Pasted image 20240722183508.png]]

EI CF admite iteradores, que proporcionan una forma de recorrer los elementos de una colección de forma secuencial, 10 que facilita el acceso y la manipulación de datos en las colecciones.

![[Pasted image 20240722184345.png]]

## Abstract Data Type (ADT) & Generics

> [!help] ¿Que es ADT?
> Un tipo de dato se puede definir como es una
colección (universo/dominio) de valores. Un tipo de dato abstracto (ADT) es una especificación de un tipo de dato, independiente de su implementación.
>
>La interfaz de un ADT se define en términos del tipo, y el conjunto de operaciones de ese tipo.
>Un ADT utiliza encapsulación para abstraer las implementaciones.
>Una DS es una implementación de un ADT

![[Pasted image 20240722184807.png]]

• Una ADT es una abstracción que describe un conjunto de datos y las operaciones que se pueden realizar con ellos, sin especificar los detalles de implementación.
• En otras palabras, un ADT define la interfaz y el comportamiento de una estructura de datos (DS), pero no revela cómo se implementa internamente.
• Frecuentemente, las ADT utilizan Generics para definir interfaces genéricas.

## Generics

> [!help]¿Que son los Generics?
Los Generics permiten definir interfaces genéricas en un ADT.
Los generics parametrizar el tipo de datos de una clase, método, o interface.
Los generics promueven la reutilización de código y la flexibilidad del ADT.
Con los generics NO necesita una se implementación específica para cada tipo de datos.
![[Pasted image 20240722190434.png]]

Generics
> [!help] ¿Para que sirven los Generics?
La combinación de ADT y Generics permite crear DS flexibles y seguras en cuanto a tipos.
Los ADT proporcionan la abstracción y la especificación de la DS.
Los generics brindan la seguridad de tipos y la reutilización de código necesarias para trabajar con diferentes tipos de datos de manera eficiente.
Juntos, ADT y Generics promueven un diseño modular y flexible en el desarrollo de software.

## Iterable 
La raíz de CF es la interface Iterable (varias clases e
interfaces la implementan!) 
Esta interfaz representa un iterador que permite recorrer todos los elementos de la colección como si fuesen una secuencia de valores.

## ArrayList
La clase ArrayList implementa la interfaz List y utiliza generics. Es una lista que proporciona un acceso rápido a través de índices ya que internamente utiliza arrays.

![[Pasted image 20240722191951.png]]![[Pasted image 20240722192136.png]]
• Buscando Objetos

• La búsqueda de elementos es muy importante
dentro de programación, ya que es una
funcionalidad común en muchas aplicaciones.
• En el contexto de listas, una de las formas mas
simples de búsqueda, es la búsqueda lineal
• La búsqueda lineal es un algoritmo de búsqueda
secuencial donde se comienza en un extremo de la

![[Pasted image 20240722192615.png]]
![[Pasted image 20240722192630.png]]
![[Pasted image 20240722192812.png]]
![[Pasted image 20240722193205.png]]
![[Pasted image 20240722193216.png]]
![[Pasted image 20240722193417.png]]