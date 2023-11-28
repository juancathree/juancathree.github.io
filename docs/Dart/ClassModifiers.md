---
layout: default
title: Class modifiers
nav_order: 7
has_children: false
parent: Dart
---

# Class modifiers

## Abstract
To define a class that doesn’t require a full, concrete implementation of its entire interface, use the abstract modifier.
```dart
abstract class Vehicle {
  void moveForward(int meters);
}

class MockVehicle implements Vehicle {
  @override
  void moveForward(int meters) {
    // ...
  }
}
```

## Interface
To define an interface, use the interface modifier. Libraries outside of the interface’s own defining library can implement the interface, but not extend it.
```dart
interface class Vehicle {
  void moveForward(int meters) {
    // ...
  }
}

class MockVehicle implements Vehicle {
  @override
  void moveForward(int meters) {
    // ...
  }
}
```

## Final
To close the type hierarchy, use the final modifier. This prevents subtyping from a class outside of the current library. Disallowing both inheritance and implementation prevents subtyping entirely
```dart
final class Vehicle {
  void moveForward(int meters) {
    // ...
  }
}
```

## Sealed
The sealed modifier prevents a class from being extended or implemented outside its own library. Sealed classes are implicitly abstract.
```dart
sealed class Vehicle {}

class Car extends Vehicle {}

class Truck implements Vehicle {}

class Bicycle extends Vehicle {}

// ERROR: Cannot be instantiated
Vehicle myVehicle = Vehicle();

// Subclasses can be instantiated
Vehicle myCar = Car();
```
