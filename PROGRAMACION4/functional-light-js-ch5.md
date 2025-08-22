---
sticker: emoji//1f4a1
---

# Functional-Light JS: Capítulo 5 - Reduciendo efectos secundarios (Resumen y explicación)

Este capítulo trata sobre cómo minimizar los efectos secundarios en la programación, una de las bases de la programación funcional. Se explica por qué los efectos secundarios son problemáticos y cómo reducirlos.

## Puntos clave
- Los efectos secundarios son cualquier interacción con el mundo externo o modificación de estado fuera del alcance de la función.
- Reducir efectos secundarios mejora la previsibilidad y testabilidad del código.
- Se recomienda aislar los efectos secundarios en partes específicas del programa.
- El uso de funciones puras y la inmutabilidad son estrategias clave.

## Ejemplo de reducción de efectos secundarios
```js
// Función impura
let contador = 0;
function incrementar() {
  contador++;
}

// Función pura
function incrementarPuro(contador) {
  return contador + 1;
}
```

## Reflexión
Cuantos menos efectos secundarios tenga nuestro código, más fácil será de mantener, probar y razonar sobre él.

---
#### Referencias
- [Functional-Light JS - Capítulo 5](https://github.com/getify/Functional-Light-JS/blob/master/manuscript/ch5.md/#chapter-5-reducing-side-effects) 