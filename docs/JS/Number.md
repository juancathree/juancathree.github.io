---
layout: default
title: Number
nav_order: 4
has_children: false
parent: JS
---

# Number

## Convertir texto a numero
```js
// Enteros
Number.parseInt("42");      // 42
Number.parseInt("42€");     // 42 (descarta todo desde un carácter no numérico)
Number.parseInt("Núm. 42"); // NaN (empieza a descartar en Núm, descarta también 42)
Number.parseInt("A");       // NaN (No se puede representar como un número)
Number.parseInt("");        // NaN (No se puede representar como un número)

// Decimales
Number.parseFloat("42.5");      // 42.5 (Conserva decimales)
Number.parseFloat("42");        // 42 (El número es entero, convierte a entero)
Number.parseFloat("88.99€");    // 88.99 (Conserva decimales)
Number.parseFloat("42€");       // 42 (El número es entero, convierte a entero)
Number.parseFloat("Núm. 33.5"); // NaN (empieza a descartar en Núm, descarta todo)

// Otra base
Number.parseInt("11101", 2);    // 11101 en binario, es 29 en decimal
Number.parseInt("31", 8);       // 31 en octal, es 25 en decimal
Number.parseInt("FF", 16);      // FF en hexadecimal, es 255 en decimal
```

## Math
```js
Math.abs(-5);             // 5
Math.sign(-5);            // -1
Math.max(1, 40, 5, 15);   // 40
Math.min(5, 10, -2, 0);   // -2
Math.pow(2, 10);          // 1024 (Equivale a 2**10)
Math.sqrt(2);             // 1.4142135623730951 (Equivale a Math.SQRT2)

// Número al azar entre 0 y 5 (no incluido)
const x = Math.floor(Math.random() * 5);

// Redondeo natural, el más cercano
Math.round(3.75);           // 4
Math.round(3.25);           // 3

// Redondeo superior (el más alto)
Math.ceil(3.75);            // 4
Math.ceil(3.25);            // 4

// Redondeo inferior (el más bajo)
Math.floor(3.75);           // 3
Math.floor(3.25);           // 3

// Redondeo con precisión
Math.round(3.123456789);    // 3
Math.fround(3.123456789);   // 3.1234567165374756

// Truncado (sólo parte entera)
Math.trunc(3.75);           // 3
Math.round(-3.75);          // -4
Math.trunc(-3.75);          // -3
```
