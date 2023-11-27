---
layout: default
title: Set
nav_order: 8
has_children: false
parent: JS
---

# Set
```js
const set = new Set();                    // Set({})               (Conjunto vacío)
const set = new Set([5, 6, 7, 8, 9]);     // Set({5, 6, 7, 8, 9})  (Conjunto con 5 elementos)

set.size;    // 0
set.add(5);
set.has(5);     // true
set.delete(3);    // false
set.clear();
const array = [...set]; // convertir en array
const clonedArray = [...structuredClone(set)];
const set = new Set(array);
```

## Operaciones de conjunto
```js
const firstSet = new Set([1, 2, 3, 4, 5]);
const secondSet = new Set([4, 5, 6, 7, 8]);

// union
const set = new Set([...firstSet, ...secondSet]);

// interseccion
const commonElements = [...firstSet].filter(element => secondSet.has(element));
const set = new Set(commonElements);

// diferencia
const diffElements = [...firstSet].filter(element => !secondSet.has(element));
const set = new Set(diffElements);

// exclusion
const firstOnlyElements = [...firstSet].filter(element => !secondSet.has(element));
const secondOnlyElements = [...secondSet].filter(element => !firstSet.has(element));
const set = new Set([...firstOnlyElements, ...secondOnlyElements]);
```
