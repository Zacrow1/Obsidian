---
tags: currying, ventajas, JavaScript, programación funcional
Creado: 2025-06-10
Relacionado: funciones de orden superior, closures
---

# Currying: concepto, razones y ventajas

El currying es una técnica que transforma una función que recibe varios argumentos en una secuencia de funciones que reciben un solo argumento. En JavaScript, esto es posible porque las funciones son ciudadanos de primera clase y gracias a los closures.

Razones para usar currying incluyen la reutilización de código y la creación de funciones especializadas a partir de funciones generales. Por ejemplo, se puede crear una función de registro personalizada:

```js
const log = type => msg => `[${type}] ${msg}`;
const info = log('INFO');
console.log(info('El sistema inició.'));
// [INFO] El sistema inició.
```

El currying facilita la composición y la reutilización, permitiendo construir funciones más expresivas y adaptables.

---
#### Referencias
- Video: Javascript. Qué es la técnica currying #javascript 