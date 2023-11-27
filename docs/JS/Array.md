---
layout: default
title: Array
nav_order: 7
has_children: false
parent: JS
---

# Array
```js
const letters = ["a", "b", "c"];  // Array con 3 elementos
const letters = [];               // Array vacío (0 elementos)
const letters = ["a", 5, true];   // Array mixto (String, Number, Boolean)
```

## Acceso
```js
const letters = ["a", "b", "c"];

letters.length;   // 3
letters[0];       // 'a'
letters.at(0);    // se puede hacer exactamente lo mismo que con [pos], sólo que además permite valores negativos
```

## Añadir o eliminar
```js
const elements = ["a", "b", "c"]; // Array inicial

elements.push("d");    // Devuelve 4.   Ahora elements = ['a', 'b', 'c', 'd']
elements.pop();        // Devuelve 'd'. Ahora elements = ['a', 'b', 'c']

elements.unshift("Z"); // Devuelve 4.   Ahora elements = ['Z', 'a', 'b', 'c']
elements.shift();      // Devuelve 'Z'. Ahora elements = ['a', 'b', 'c']
```

## Alternativas para crear arrays
```js
const text = "12345";

const letters = Array.from(text);               // ["1", "2", "3", "4", "5"]
const letters = [...text];                      // ["1", "2", "3", "4", "5"]

const firstPart = [1, 2, 3];
firstPart.concat(firstPart);              // Devuelve [1, 2, 3, 1, 2, 3]

letters.join("->");       // Devuelve '1->2->3->4->5'
"5-4-3-2-1".split("-");   // Devuelve ['5', '4', '3', '2', '1']
```

## Buscar elementos
```js
const numbers = [5, 10, 15, 20, 25];

numbers.includes(3);    // false
numbers.includes(15);   // true
numbers.indexOf(5);   // 0
numbers.lastIndexOf(5);   // 4
```

## Ordenacion
```js
const elements = ["A", "B", "C", "D", "E", "F"];
const reversedElements = elements.reverse(); // ["F", "E", "D", "C", "B", "A"]
const reversedElements = elements.toReversed(); // no modifica el original

const names = ["Alberto", "Zoe", "Ana", "Mauricio", "Bernardo"];
const sortedNames = names.sort(); // ["Alberto", "Ana", "Bernardo", "Mauricio", "Zoe"]
const sortedNames = names.toSorted();

const numbers = [1, 8, 2, 32, 9, 7, 4];
const naturalNumbers = numbers.toSorted((a,b) => a-b);     // [1, 2, 4, 7, 8, 9, 32]
```

## Array functions
```js
const letters = ["a", "b", "c", "d"];

letters.forEach(e => console.log(e));
letters.every(e => e.length == 1);
letters.some(e => e.length == 2);
letters.map(e => e.length); // [1,1,1,1]
letters.filter(e => e.startsWith("a")); // ["a"]
letters.find(e => e.lenght == 1); // ["a", "b", "c", "d"]
letters.findIndex(e => e.startsWith("a")); // 0
letters.findLast(e => e.startsWith("a"));
letters.findLastIndex(e => e.startsWith("a"));

const numbers = [95, 5, 25, 10, 25];
numbers.reduce((first, second) =>  first + second);
numbers.reduce((accumulator, nextElement) => accumulator + nextElement, 0);
```

## Destructuracion
```js
const elements = [5, 2];
const [first, last] = elements;    // first = 5, last = 2

// intercambio de variables
let a = 10;
let b = 5;
[a, b] = [b, a];

// spread
const debug = (param) => console.log(...param);

// rest
const elements = [5, 4, 3, 2];
const [first, ...rest] = elements;  // first = 5, rest = [4, 3, 2]
```
