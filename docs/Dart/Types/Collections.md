---
layout: default
title: Built-in Types
parent: Types
nav_order: 1
grand_parent: Dart
---

# Collections

## Lists
```dart
var list = [1, 2, 3]
assert(list.length == 3);
```

## Sets
```dart
var halogens = {'fluorine', 'chlorine', 'bromine', 'iodine', 'astatine'};


var elements = <String>{};
// Set<String> elements = {}; // This works, too.
// var elements = {}; // Creates a map, not a set.
elements.add('fluorine');
elements.addAll(halogens);
assert(elements.length == 5);
```

## Maps
```dart
var gifts = {
  // Key:    Value
  'first': 'partridge',
  'second': 'turtledoves',
  'fifth': 'golden rings'
};

var gifts = Map<String, String>();
gifts['first'] = 'partridge';
gifts['second'] = 'turtledoves';
gifts['fifth'] = 'golden rings';
```

# Operators

## Spread
Dart supports the spread operator (...) and the null-aware spread operator (...?) in list, map, and set literals. Spread operators provide a concise way to insert multiple values into a collection.
```dart
var list = [1, 2, 3];
var list2 = [0, ...list];
assert(list2.length == 4);
```

If the expression to the right of the spread operator might be null, you can avoid exceptions by using a null-aware spread operator (...?):
```dart
var list2 = [0, ...?list];
```

## Control-flow
Dart offers collection if and collection for for use in list, map, and set literals. You can use these operators to build collections using conditionals (if) and repetition (for).

```dart
var nav = ['Home', 'Furniture', 'Plants', if (promoActive) 'Outlet'];
var nav = ['Home', 'Furniture', 'Plants', if (login case 'Manager') 'Inventory'];

var listOfInts = [1, 2, 3];
var listOfStrings = ['#0', for (var i in listOfInts) '#$i'];
assert(listOfStrings[1] == '#1');
```
