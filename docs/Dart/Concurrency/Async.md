---
layout: default
title: Asynchrony
parent: Concurrency
nav_order: 1
grand_parent: Dart
---

# Asynchrony
These functions are asynchronous: they return after setting up a possibly time-consuming operation (such as I/O), without waiting for that operation to complete.

## Handling futures
```dart
Future<void> checkVersion() async {
  var version = await lookUpVersion();
  // Do something with version
}
```

## Declaring async functions
```dart
Future<String> lookUpVersion() async => '1.0.0';
```
