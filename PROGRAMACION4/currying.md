---
tags: currying, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: funciones de orden superior, aplicación parcial, composición de funciones
---

# Currying

El currying es una técnica que transforma una función que toma varios argumentos en una secuencia de funciones que toman un solo argumento. Esto permite crear funciones más reutilizables y facilita la composición de funciones en programación funcional.

Por ejemplo, la función suma curried:

```js
const add = a => b => a + b;
console.log(add(2)(3)); // 5
```

El currying permite la aplicación parcial de argumentos, es decir, fijar algunos valores y obtener nuevas funciones:

```js
const add10 = add(10);
console.log(add10(5)); // 15
```

Esta técnica es útil para crear funciones especializadas a partir de funciones generales y es esencial para la composición de funciones.

---
#### Referencias
- Material de clase Semana 3, Programación 4, Universidad Jala 