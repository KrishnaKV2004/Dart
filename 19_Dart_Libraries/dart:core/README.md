# `dart:core`

## Learning Goal

In this lesson, you will learn what `dart:core` provides and why it is the foundation of almost every Dart program.

## What Is `dart:core`

`dart:core` is the default core library that gives you the basic building blocks of Dart.

It includes common types and utilities such as:

- `String`
- `int`
- `double`
- `bool`
- `List`
- `Map`
- `Set`
- `Object`
- `DateTime`
- `print()`

## Basic Example

```dart
void main() {
  final name = 'Asha';
  final age = 21;
  final isStudent = true;

  print('Name: $name');
  print('Age: $age');
  print('Student: $isStudent');
}
```

Expected output:

```text
Name: Asha
Age: 21
Student: true
```

This is all powered by the core language and core library.

## Why This Is Useful

Almost every Dart program uses `dart:core`, even if you never import it explicitly.

It is the library that makes common types and operations available.

## Real-World Example

```dart
void main() {
  final values = [10, 20, 30];
  final total = values.length;
  final hasTwoDigits = values.any((value) => value >= 10);

  print('Count: $total');
  print('Has two digits: $hasTwoDigits');
}
```

Expected output:

```text
Count: 3
Has two digits: true
```

This shows how core types and collection methods work together.

## Senior Trick: Know The Core API Before Reaching For Extra Tools

A lot of basic work is already covered by core types and methods.

That means fewer dependencies and less complexity.

## Senior Trick: Learn Core Types Deeply

Understanding how `String`, `List`, `Map`, and `DateTime` behave gives you a strong base for everything else in Dart.

## Summary

- `dart:core` is the foundation library of Dart
- it provides built-in types and common utilities
- it is used in almost every program
- it is the first library to understand well

## Flutter Connection

Flutter code uses `dart:core` constantly for values, collections, dates, strings, and basic logic.
