---
tags: [Estructuras de Control, Condicionales, Bucles, JavaScript]
Creado: 
Relacionado: funciones.md, entrada_y_salida_en_node.md
---

# Estructuras de Control en JavaScript

## Condicionales
### if, else if, else
```js
let edad = 20;
if (edad < 18) {
  console.log('Menor de edad');
} else {
  console.log('Mayor de edad');
}
```

### switch
```js
let dia = 'lunes';
switch (dia) {
  case 'lunes':
    console.log('Comienza la semana');
    break;
  case 'viernes':
    console.log('Fin de semana');
    break;
  default:
    console.log('Día normal');
}
```

## Bucles
### for
```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
### while
```js
let n = 0;
while (n < 3) {
  console.log(n);
  n++;
}
```
### do...while
```js
let x = 0;
do {
  console.log(x);
  x++;
} while (x < 2);
```

## break y continue
```js
for (let i = 0; i < 5; i++) {
  if (i === 3) break;
  if (i === 1) continue;
  console.log(i);
}
```

---
#### Referencias
a 