---
layout: default
title: Built-in Types
parent: Types
nav_order: 1
grand_parent: Dart
---

# Built-in Types

## Numbers
```dart
var x = 1; // int
var y = 1.1; // double
```
Here’s how you turn a string into a number, or vice versa:
```dart
// String -> int
var one = int.parse('1');
assert(one == 1);

// String -> double
var onePointOne = double.parse('1.1');
assert(onePointOne == 1.1);

// int -> String
String oneAsString = 1.toString();
assert(oneAsString == '1');

// double -> String
String piAsString = 3.14159.toStringAsFixed(2);
assert(piAsString == '3.14');
```

## Strings
```dart
var s1 = 'Single quotes work well for string literals.';
```

## Booleans
```dart
var isTrue = true;

// Check for an empty string.
var fullName = '';
assert(fullName.isEmpty);

// Check for zero.
var hitPoints = 0;
assert(hitPoints <= 0);

// Check for null.
var unicorn = null;
assert(unicorn == null);

// Check for NaN.
var iMeantToDoThis = 0 / 0;
assert(iMeantToDoThis.isNaN);
```
