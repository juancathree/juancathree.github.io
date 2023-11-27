---
layout: default
title: Functions
nav_order: 3
has_children: false
parent: Dart
---

# Functions
```dart
bool isNoble(atomicNumber) {
  return _nobleGases[atomicNumber] != null;
}

bool isNoble(int atomicNumber) => _nobleGases[atomicNumber] != null;
```

## Parameters
```dart
// named parameter are optional unless  they're explicitly marked as required
void enableFlags({bool? bold, bool? hidden}) {...}
enableFlags(bold: true, hidden: false);
void enableFlags({bool bold = false, bool hidden = false}) {...} // dafults values
enableFlags(bold: true);
const Scrollbar({super.key, required Widget child}); // required parameter

// Wrapping a set of function parameters in [] marks them as optional positional parameters. If you don’t provide a default value, their types must be nullable as their default value will be null
String say(String from, String msg, [String? device]) {
  var result = '$from says $msg';
  if (device != null) {
    result = '$result with a $device';
  }
  return result;
}

assert(say('Bob', 'Howdy') == 'Bob says Howdy');
assert(say('Bob', 'Howdy', 'smoke signal') == 'Bob says Howdy with a smoke signal');

String say(String from, String msg, [String device = 'carrier pigeon']) {
  var result = '$from says $msg with a $device';
  return result;
}
```

## Return values
```dart
(String, int) foo() {
  return ('something', 42);
}
```

## Generators
```dart
// synchronous
Iterable<int> naturalsTo(int n) sync* {
  int k = 0;
  while (k < n) yield k++;
}

// asynchronous
Stream<int> asynchronousNaturalsTo(int n) async* {
  int k = 0;
  while (k < n) yield k++;
}
```
