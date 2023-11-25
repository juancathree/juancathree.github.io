---
layout: default
title: Typedefs
parent: Types
nav_order: 3
grand_parent: Dart
---

# Typedefs
```dart
typedef IntList = List<int>;
IntList il = [1, 2, 3];

typedef ListMapper<X> = Map<X, List<X>>;
Map<String, List<String>> m1 = {}; // Verbose.
ListMapper<String> m2 = {}; // Same thing but shorter and clearer.
```
