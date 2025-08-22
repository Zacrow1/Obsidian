---
tags: funciones de alto orden, aplicaciones, JavaScript, programación funcional
Creado: 2025-06-10
Relacionado: map, filter, React
---

# Aplicaciones comunes de funciones de alto orden en JavaScript

Las funciones de alto orden se utilizan ampliamente en JavaScript para procesar y transformar datos. Ejemplos comunes incluyen map y filter, que permiten aplicar funciones a cada elemento de un array o filtrar elementos según una condición.

Por ejemplo, usando map:

```js
const numbers = [1, 2, 3];
const doubled = numbers.map(x => x * 2);
console.log(doubled); // [2, 4, 6]
```

Y usando filter:

```js
const even = numbers.filter(x => x % 2 === 0);
console.log(even); // [2]
```

En frameworks como React, estas funciones son esenciales para manipular listas y renderizar componentes de manera declarativa.

---
#### Referencias
- Video: ¿Qué son las High Order Functions en Javascript? 