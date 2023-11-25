---
layout: default
title: Imports
parent: Syntax basics
nav_order: 3
grand_parent: Dart
---

# Imports

## Using libraries
```dart
import 'dart:html';

// set a prefix
import 'package:lib2/lib2.dart' as lib2;

// Import only foo.
import 'package:lib1/lib1.dart' show foo;

// Import all names EXCEPT foo.
import 'package:lib2/lib2.dart' hide foo;
```
