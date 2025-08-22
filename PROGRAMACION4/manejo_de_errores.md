---
tags: [Errores, Excepciones, JavaScript, Manejo de Errores]
Creado: 
Relacionado: estructuras_de_control.md, funciones.md
---

# Manejo de Errores en JavaScript

## try, catch, finally
```js
try {
  throw new Error('Ocurrió un error');
} catch (e) {
  console.log(e.message);
} finally {
  console.log('Esto siempre se ejecuta');
}
```

## throw
Permite lanzar errores personalizados.
```js
function dividir(a, b) {
  if (b === 0) {
    throw new Error('No se puede dividir por cero');
  }
  return a / b;
}
```

## Errores comunes
- ReferenceError, TypeError, SyntaxError, etc. 

---
#### Referencias
a 