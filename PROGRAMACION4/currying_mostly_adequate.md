---
tags: currying, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: funciones de orden superior, closures, composición de funciones
---

# Currying (Según Mostly Adequate Guide)

El currying es una técnica que transforma una función que acepta varios argumentos en una secuencia de funciones que aceptan un solo argumento. Esto permite crear funciones más reutilizables y facilita la composición en programación funcional. En JavaScript, el currying se apoya en los closures para recordar los argumentos ya proporcionados.

Ejemplo básico:

```js
const add = a => b => a + b;
console.log(add(2)(3)); // 5
```

El currying permite crear funciones especializadas a partir de funciones generales, y es fundamental para la programación point-free y la composición de funciones.

Más detalles y ejemplos en el capítulo 4 de Mostly Adequate Guide: [https://mostly-adequate.gitbook.io/mostly-adequate-guide/ch04](https://mostly-adequate.gitbook.io/mostly-adequate-guide/ch04)

---
#### Referencias
- Mostly Adequate Guide, Capítulo 4: Currying 