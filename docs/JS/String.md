---
layout: default
title: String
nav_order: 5
has_children: false
parent: JS
---

# String
```js
const text = "¡Hola a todos!";
"Hola".length;    // 4
text[1];      // "H"
```

## Posiciones
```js
const name = "Manz";
name.charAt(0);     // 'M'
name.indexOf("n");  // 2
name..lastIndexOf("n");  // 2
```

## Substring
```js
const text = "Submarino";

text.substring(3);    // 'marino' (desde el 3 en adelante)
text.substring(3, 5); // 'ma'     (desde el 3, hasta el 5)
text.substr(3);       // 'marino' (desde el 3 en adelante)
text.substr(3, 5);    // 'marin'  (desde el 3, hasta el 3+5)
text.substr(-3);      // 'ino'    (desde la posición 3 desde el final, en adelante)
text.substr(-3, 2);   // 'in'     (desde la posición 3 desde el final, hasta 2 posiciones más)
```

## Dividir texto
```js
"88.12.44.123".split(".");    // ["88", "12", "44", "123"] (4 elementos)
"1.2.3.4.5".split(".");       // ["1", "2", "3", "4", "5"] (5 elementos)
"Hola a todos".split(" ");    // ["Hola", "a", "todos"] (3 elementos)
"A,B,C,D,E".split(",", 3);    // ["A", "B", "C"] (limitado a los 3 primeros elementos)
"Código".split("");           // ["C", "ó", "d", "i", "g", "o"] (6 elementos)
// Separa tanto por punto como por coma
"88.12,44.123".split(/[.,]/);    // ["88", "12", "44", "123"] (4 elementos)
```

## Comprobacion
```js
onst text = "Manz";

text.startsWith("M");     // true  ('Manz' empieza por 'M')
text.startsWith("a", 1);  // true  ('anz' empieza por 'a')
text.endsWith("o");       // false ('Manz' no acaba en 'o')
text.endsWith("n", 3);    // true  ('Man' acaba en 'n')
text.includes("an");      // true  ('Manz' incluye 'an')
text.includes("M", 1);    // false ('anz' no incluye 'M')
```

## Busqueda
```js
const text = "El gato, el perro y el pato.";
const regexp = /.a.o/g;

text.search(regexp);   // 3, porque la primera coincidencia ocurre en la posición 3 (gato)
text.match(regexp);    // ["gato", "pato"], las dos coincidencias encontradas

// el método .matchAll() es un poco más avanzado
const iterator = text.matchAll(regexp);
for (let ocurrence of iterator) {
  console.log(ocurrence);
}

// ['gato', index: 3, input: 'El gato, el perro y el pato.', groups: undefined]
// ['pato', index: 23, input: 'El gato, el perro y el pato.', groups: undefined]

// También es posible utilizar .matchAll() desestructurando su resultado, lo que nos permitirá acceder a la información de una forma más directa
const results = [...text.matchAll(regexp)];    // ["gato", "pato"]

results.length     // 2
results[0].index   // 3
results[1].index   // 23
```

## Reemplazar
```js
const text = "Hola gato, ¿eres un perro o eres un pato?";

// Reemplazar la primera ocurrencia
text.replace("g", "p");                     // "Hola pato, ¿eres un perro o eres un pato?"
text.replace("g", "p").replace("o", "a");   // "Hala pato, ¿eres un perro o eres un pato?"

// Reemplazar todas las ocurrencias
text.replaceAll("e", "i");                  // "Hola gato, ¿iris un pirro o iris un pato?"
text.replace(/e/g, "i");                    // "Hola gato, ¿iris un pirro o iris un pato?"
```

## Modificar
```js
const text = "Los gatos dominarán el mundo.";

text.toLowerCase();   // "los gatos dominarán el mundo."
text.toUpperCase();   // "LOS GATOS DOMINARÁN EL MUNDO."
text.trim(); // elimina espacios de alante y atras

```
