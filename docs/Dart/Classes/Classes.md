---
layout: default
title: Classes
parent: Classes & objects
nav_order: 1
grand_parent: Dart
---

# Classes
```dart
class Point {
  double? x; // Declare instance variable x, initially null.
  double? y; // Declare y, initially null.
  double z = 0; // Declare z, initially 0.
}

void main() {
  var point = Point();
  point.x = 4; // Use the setter method for x.
  assert(point.x == 4); // Use the getter method for x.
  assert(point.y == null); // Values default to null.
}
```

## Constructors
```dart
class Point {
  final double x;
  final double y;

  Point(this.x, this.y);
  // Sets the x and y instance variables
  // before the constructor body runs.

  // Named constructor
  Point.origin()
      : x = xOrigin,
        y = yOrigin;
}
```
