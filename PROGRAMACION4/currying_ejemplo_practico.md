---
tags: currying, ejemplo práctico, JavaScript, programación funcional
Creado: 2025-06-10
Relacionado: funciones de orden superior, closures
---

# Ejemplo práctico de currying

Un ejemplo clásico de currying es transformar una función de multiplicación para que acepte los argumentos uno a uno:

```js
const multiply = a => b => a * b;
const double = multiply(2);
console.log(double(5)); // 10
```

Esto permite crear funciones especializadas fácilmente, como una función para duplicar cualquier número. El currying aprovecha los closures para recordar el valor del primer argumento.

---
#### Referencias
- Video: Javascript. Qué es la técnica currying #javascript 