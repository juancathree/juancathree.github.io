---
layout: default
title: Map
nav_order: 9
has_children: false
parent: JS
---

# Map
```js
const map = new Map();                                        // Map({}) (Mapa vacío)
const map = new Map([[1, "uno"]]);                            // Map({ 1=>"uno" })

map.size;    // 1
map.set(5, "cinco");
map.has(2);     // false
map.delete(3);    // false
map.clear();
const entries = [...structuredClone(map)]; // convertir a array
```
