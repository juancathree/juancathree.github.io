---
layout: default
title: Tipos de datos
nav_order: 1
has_children: false
parent: JS
---

# Tipos de datos
```js
var number = 42
var bigInt = 123445323412124 
var string = "Hola"
var isFalse = true
var notDefined // undefined
var function = function(){}
var simbolo = Symbol(1) // valir unico
```

## ¿Qué tipo de dato tiene?
Podemos utilizar la función typeof, que nos devuelve el tipo de dato de la variable que le pasemos por parámetro. Más adelante, nos encontraremos que en muchos casos, typeof() resulta insuficiente porque en tipos de datos más avanzados simplemente nos indica que son objetos. Con constructor.name podemos obtener el tipo de constructor que se utiliza.
```js
console.log(typeof(number))
console.log(string.constructor.name)
```
