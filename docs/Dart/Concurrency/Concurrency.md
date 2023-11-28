---
layout: default
title: Concurrency
parent: Concurrency
nav_order: 2
grand_parent: Dart
---

# Concurrency
A promise to eventually provide an int value is typed as Future<int>. A promise to provide a series of int values has the type Stream<int>.

## Async-await syntax
```dart
const String filename = 'with_keys.json';

void main() async {
  // Read some data.
  final fileData = await _readFileAsync();
  final jsonData = jsonDecode(fileData);

  // Use that data.
  print('Number of JSON keys: ${jsonData.length}');
}

Future<String> _readFileAsync() async {
  final file = File(filename);
  final contents = await file.readAsString();
  return contents.trim();
}
```

## Isolate
```dart
const String filename = 'with_keys.json';

void main() async {
  // Read some data.
  final jsonData = await Isolate.run(_readAndParseJson);

  // Use that data.
  print('Number of JSON keys: ${jsonData.length}');
}
```
