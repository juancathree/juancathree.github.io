---
layout: default
title: Operadores
nav_order: 3
has_children: false
parent: JS
---

# Operadores

## AND
```js
0 && undefined      // 0 (se evalua como false && false, devuelve el primero)
undefined && 0      // undefined (se evalua como false && false, devuelve el primero)
55 && null          // null (se evalua como true && false, devuelve el segundo)
null && 55          // null (se evalua como false && true, devuelve el primero)
44 && 20            // 20 (se evalua como true && true, devuelve el segundo)
```

Teniendo todo esto en cuenta, este operador es una oportunidad fantástica para utilizarlo a modo de if compactos y muy legibles.

```js
45 && "OK"            // "OK"
false && "OK"         // false

const doTask = () => "OK!";   // Creamos función que devuelve "OK!"
isCorrect && doTask()         // Si isCorrect es true, ejecuta doTask()
```

## Operador ternario
```js
/ Sin operador ternario
let role;
if (name === "Manz") {
  role = "streamer";
} else {
  role = "user";
}

// Con operador ternario
const role = name === "Manz" ? "streamer" : "user";
```

## OR
```js
0 || null          // null (se evalua como false || false, devuelve el segundo)
44 || undefined    // 44 (se evalua como true || false, devuelve el primero)
0 || 17            // 17 (se evalua como false || true, devuelve el segundo)
4 || 10            // 4 (se evalua como true || true, devuelve el primero)
```

Teniendo todo esto en cuenta, el operador || nos podría venir bastante bien para situaciones donde, por ejemplo, tenemos una variable name que no sabemos a ciencia cierta si está definida y queremos crear una nueva variable userName con el valor de name, o sino, un valor por defecto "Unknown name"
```js
const userName = name || "Unknown name";

"Manz" || "Unknown name"      // "Manz"
null || "Unknown name"        // "Unknown name"
false || "Unknown name"       // "Unknown name"
undefined || "Unknown name"   // "Unknown name"
0 || "Unknown name"           // "Unknown name"
```

## Nullish coalescing
Es un operador lógico muy similar al operador OR, pero con ciertos matices y cambios. A grandes rasgos, se puede decir que el operador a ?? b devuelve b sólo cuando a es undefined o null.
```js
42 || 50          // 42
42 ?? 50          // 42 (ambos se comportan igual)
false || 50       // 50 (false es un valor falsy, devuelve el segundo)
false ?? 50       // false (la parte izquierda no es null ni undefined, devuelve el primero)
0 || 50           // 50 (0 es un valor falsy, devuelve el segundo)
0 ?? 50           // 0 (la parte izquierda no es null ni undefined, devuelve el primero)
null || 50        // 50 (null es un valor falsy, devuelve el segundo)
null ?? 50        // 50 (devuelve el segundo)
undefined || 50   // 50 (undefined es un valor falsy, devuelve el segundo)
undefined ?? 50   // 50 (devuelve el segundo)
```

## Asignacion logica nula
Existen ciertos casos donde, si una variable tiene valores null o undefined (valores nullish) y sólo en esos casos, queremos cambiar su valor.
```js
// Sin asignación lógica nula
if (x === null || x === undefined) {
  x = 50;
}

// Con asignación lógica nula
x ??= 50;


const resetConfig = (data) => {
  data.life ??= 100;
  data.level ??= 1;
  return data;
}

resetConfig({ life: 25, level: 4 });      // { life: 25, level: 4 }
resetConfig({ life: null, level: 2 });    // { life: 100, level: 2 }
resetConfig({});                          // { life: 100, level: 1 }
```

## Encadenamiento opcional
Vamos a imaginar que la propiedad attrs (y todo su contenido) no existe aún, sino que tenemos un objeto user que solo tiene las propiedades name y role, pero que en algún momento de nuestro código esta propiedad attrs se añadirá en nuestro objeto. Si intentamos acceder a una de sus propiedades sin que la propiedad attrs exista, nos lanzara un error.
```js
const user = {
  name: "Manz",
  role: "streamer",
  attrs: {
    life: 100,
    power: 25
  }
}

user.attrs?.power    // undefined
user.attrs?.life     // undefined
```
Con optional chaining podemos acceder de manera segura aunque no este definido.
