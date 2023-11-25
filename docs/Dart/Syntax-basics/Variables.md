---
layout: default
title: Variables
parent: Syntax basics
grand_parent: Dart
---

# Variables
```dart
var name = 'Bob';
String name = 'Bob';
```

## Null Safety
Null safety prevents an error that results from unintentional access of variables set to null. The error is called a null dereference error.
```dart
String? name  // Nullable type. Can be `null` or string.
String name   // Non-nullable type. Cannot be `null` but can be string.
```

## Late
The late modifier has two use cases:
  - Declaring a non-nullable variable that’s initialized after its declaration.
  - Lazily initializing a variable.

When you mark a variable as late but initialize it at its declaration, then the initializer runs the first time the variable is used.
```dart
late String description;
late String temperature = readThermometer(); // Lazily initialized.
```

## Final and const
If you never intend to change a variable, use final or const, either instead of var or in addition to a type. A final variable can be set only once.
```dart
final name = 'Bob'; // Without a type annotation
final String nickname = 'Bobby';

const bar = 1000000; // Unit of pressure (dynes/cm2)
const double atm = 1.01325 * bar; // Standard atmosphere
```
