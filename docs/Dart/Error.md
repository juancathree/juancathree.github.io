---
layout: default
title: Error handling
nav_order: 5
has_children: false
parent: Dart
---

# Error handling

## Throw
```dart
void distanceTo(Point other) => throw UnimplementedError();
```

## Catch
```dart
try {
  breedMoreLlamas();
} on OutOfLlamasException {
  // A specific exception
  buyMoreLlamas();
} on Exception catch (e) {
  // Anything else that is an exception
  print('Unknown exception: $e');
} catch (e) {
  // No specified type, handles all
  print('Something really unknown: $e');
}

// To partially handle an exception, while allowing it to propagate, use the rethrow keyword.
void misbehave() {
  try {
    dynamic foo = true;
    print(foo++); // Runtime error
  } catch (e) {
    print('misbehave() partially handled ${e.runtimeType}.');
    rethrow; // Allow callers to see the exception.
  }
}

void main() {
  try {
    misbehave();
  } catch (e) {
    print('main() finished handling ${e.runtimeType}.');
  }
}
```

## Finally
To ensure that some code runs whether or not an exception is thrown, use a finally clause
```dart
try {
  breedMoreLlamas();
} catch (e) {
  print('Error: $e'); // Handle the exception first.
} finally {
  cleanLlamaStalls(); // Then clean up.
}
```

## Assert
```dart
// Make sure the variable has a non-null value.
assert(text != null);
```
