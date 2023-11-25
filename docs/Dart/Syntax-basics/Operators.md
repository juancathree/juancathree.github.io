---
layout: default
title: Operators
parent: Syntax basics
nav_order: 2
grand_parent: Dart
---

# Operators

## Type test operators
Use the as operator to cast an object to a particular type if and only if you are sure that the object is of that type.
```dart
(employee as Person).firstName = 'Bob';
```

If you aren’t sure that the object is of type T, then use is T to check the type before using the object.
```dart
if (employee is Person) {
  // Type check
  employee.firstName = 'Bob';
}
```

## Assignment check
To assign only if the assigned-to variable is null, use the ??= operator.
```dart
// Assign value to b if b is null; otherwise, b stays the same
b ??= value;
```

## Conditional expressions
When you need to assign a value based on a boolean expression, consider using ? and :.
```dart
var visibility = isPublic ? 'public' : 'private';
```

If the boolean expression tests for null, consider using ??
```dart
String playerName(String? name) => name ?? 'Guest';
```

## Cascade notation
```dart
var paint = Paint()
  ..color = Colors.black
  ..strokeCap = StrokeCap.round
  ..strokeWidth = 5.0;
// ==
var paint = Paint();
paint.color = Colors.black;
paint.strokeCap = StrokeCap.round;
paint.strokeWidth = 5.0;\

// access without throw error if null
var paint = Paint()
paint?.color = Colors.black
```
