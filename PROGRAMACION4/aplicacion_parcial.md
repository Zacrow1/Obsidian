---
tags: aplicación parcial, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, funciones de orden superior
---

# Aplicación parcial

La aplicación parcial consiste en fijar algunos argumentos de una función, obteniendo una nueva función que espera el resto de los argumentos. Es útil para crear funciones especializadas a partir de funciones generales.

Ejemplo tradicional:

```js
function calculateSphereVolume(pi, radius, height) {
  return pi * radius * radius * height;
}
function partialCalculateSphereVolume(pi) {
  return function (radius, height) {
    return calculateSphereVolume(pi, radius, height);
  };
}
const partialWithPi = partialCalculateSphereVolume(3.14159);
console.log(partialWithPi(5, 10)); // 785.3975
```

Ejemplo con funciones flecha:

```js
const calculateSphereVolume = (pi, radius, height) => pi * radius * radius * height;
const partialCalculateSphereVolume = pi => (radius, height) => calculateSphereVolume(pi, radius, height);
const partialWithPi = partialCalculateSphereVolume(3.14159);
console.log(partialWithPi(5, 10)); // 785.3975
```

La diferencia con currying es que la aplicación parcial puede fijar varios argumentos a la vez, mientras que el currying transforma la función en una secuencia de funciones unarias.

---
#### Referencias
- Material de clase Semana 3, Programación 4, Universidad Jala 