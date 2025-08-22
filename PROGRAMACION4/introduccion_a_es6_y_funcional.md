---
tags: [ES6, Programación Funcional, JavaScript]
Creado: 
Relacionado: funciones_orden_superior_y_paradigmas_declarativos.md, principios_solidos_monadas.md
---

# Introducción a ES6 y Principios de Programación Funcional

## ¿Qué es ES6?
ES6 (ECMAScript 2015) es una versión importante de JavaScript que introdujo nuevas características y mejoras al lenguaje, facilitando la escritura de código más limpio, seguro y expresivo.

### Características principales de ES6
- **let y const**: Nuevas formas de declarar variables con alcance de bloque.
- **Arrow functions**: Sintaxis concisa para funciones.
- **Clases**: Sintaxis para programación orientada a objetos.
- **Template literals**: Cadenas de texto con interpolación.
- **Destructuring**: Extraer valores de arrays y objetos fácilmente.
- **Módulos**: import/export para modularizar código.
- **Promesas**: Manejo de asincronía más sencillo.
- **Parámetros por defecto y rest/spread**: Mayor flexibilidad en funciones.

#### Ejemplo de arrow function y destructuring
```js
const persona = { nombre: 'Ana', edad: 28 };
const saludar = ({ nombre }) => `Hola, ${nombre}`;
console.log(saludar(persona));
```

## Principios de Programación Funcional
- **Funciones puras**: No dependen ni modifican el estado externo.
- **Inmutabilidad**: No modificar datos originales.
- **Transparencia referencial**: Una función siempre devuelve el mismo resultado para los mismos argumentos.
- **Composición**: Combinar funciones simples para crear otras más complejas.
- **Declaratividad**: Describir el "qué" más que el "cómo".

### Ejemplo de función pura e inmutabilidad
```js
const sumar = (a, b) => a + b;
const arr = [1, 2, 3];
const nuevoArr = [...arr, 4]; // arr no se modifica
```

---

**Sigue con los siguientes archivos para profundizar en funciones de orden superior, pruebas y técnicas avanzadas.**

---
#### Referencias
a 