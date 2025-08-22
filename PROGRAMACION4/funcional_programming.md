---
tags: [Programación Funcional, JavaScript, Inmutabilidad, Funciones Puras]
Creado: 
Relacionado: funciones.md, funciones_orden_superior_y_paradigmas_declarativos.md
---

# Programación Funcional en JavaScript

La programación funcional es un paradigma que trata la computación como la evaluación de funciones matemáticas y evita el estado y los datos mutables.

## Conceptos básicos
- **Funciones puras**: No tienen efectos secundarios y siempre devuelven el mismo resultado para los mismos argumentos.
- **Inmutabilidad**: No modificar los datos originales, sino crear nuevos.
- **Funciones de orden superior**: Reciben funciones como argumentos o devuelven funciones.
- **Composición de funciones**: Combinar funciones simples para crear otras más complejas.

### Ejemplo de función pura
```js
function suma(a, b) {
  return a + b;
}
```

### Ejemplo de inmutabilidad
```js
const arr = [1, 2, 3];
const nuevoArr = arr.concat(4); // arr no se modifica
```

### Funciones de orden superior
```js
const numeros = [1, 2, 3, 4];
const dobles = numeros.map(n => n * 2);
```

### Composición de funciones
```js
const agregarUno = x => x + 1;
const duplicar = x => x * 2;
const compuesto = x => duplicar(agregarUno(x));
console.log(compuesto(3)); // 8
```

## Avanzado: inmutabilidad profunda y librerías
- Uso de librerías como Immutable.js o Ramda para estructuras inmutables y composición avanzada.

---

La programación funcional ayuda a escribir código más predecible, fácil de probar y mantener.

---
#### Referencias
a 