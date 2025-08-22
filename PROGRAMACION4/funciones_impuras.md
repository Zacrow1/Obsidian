# Funciones impuras en JavaScript

Una **función impura** es aquella que puede producir efectos secundarios o modificar el estado fuera de su propio ámbito. Esto significa que puede alterar variables externas, modificar los argumentos recibidos (si son objetos o arreglos), interactuar con el entorno (como la consola, archivos, bases de datos, etc.), o depender de datos externos que pueden cambiar.

## Características de una función impura

1. **No determinismo**: Puede devolver resultados diferentes aunque se le pasen los mismos argumentos, si depende de factores externos.
2. **Efectos secundarios**: Modifica variables globales, argumentos por referencia, o interactúa con el entorno externo.

## Ejemplo de función impura (modificando un arreglo)

```javascript
function agregarElementoImpuro(arr, elemento) {
    arr.push(elemento); // Modifica el arreglo original
    return arr;
}

const original = [1, 2, 3];
agregarElementoImpuro(original, 4);
// original ahora es [1, 2, 3, 4] (¡fue modificado!)
```

## Ejemplo de función impura (efecto externo)

```javascript
let contador = 0;
function incrementarContador() {
    contador++;
    return contador;
}

// El valor de retorno depende del estado externo (contador)
```

## Ejemplo de función impura (dependencia de datos externos)

```javascript
function obtenerHoraActual() {
    return new Date().getHours();
}

// El resultado cambia cada vez que se llama, aunque no reciba argumentos
```

## Riesgos de las funciones impuras

- **Difíciles de testear**: Su resultado puede variar y dependen del contexto externo.
- **Menos predecibles**: Pueden causar errores difíciles de rastrear.
- **Pueden generar bugs**: Si modifican datos compartidos, pueden provocar efectos no deseados en otras partes del programa.

## ¿Cuándo pueden ser necesarias?

Las funciones impuras son inevitables cuando necesitamos interactuar con el mundo exterior: mostrar mensajes en pantalla, leer archivos, acceder a bases de datos, modificar el DOM, etc. La clave es aislarlas y minimizar su uso, manteniendo la mayor parte del código lo más puro posible.

---

**Resumen:**
- Una función impura puede modificar el estado externo o depender de él.
- Es recomendable limitar su uso y preferir funciones puras siempre que sea posible. 