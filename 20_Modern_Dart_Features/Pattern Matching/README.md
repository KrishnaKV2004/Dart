# Pattern Matching

## Learning Goal

In this lesson, you will learn how pattern matching lets Dart inspect and destructure values in a concise way.

## What Is Pattern Matching

Pattern matching checks the shape of a value and lets you respond based on that shape.

It is especially useful when working with records, collections, enums, and class structures.

## Basic Example

```dart
void main() {
  final value = (name: 'Asha', age: 21);

  switch (value) {
    case (name: String name, age: int age):
      print('$name is $age');
      break;
  }
}
```

Expected output:

```text
Asha is 21
```

The pattern pulls the values out directly.

## Why This Is Useful

Pattern matching helps you:

- avoid manual field extraction
- write more expressive branching
- handle data shapes cleanly
- reduce boilerplate

## Real-World Example

```dart
void main() {
  final user = (role: 'admin', active: true);

  switch (user) {
    case (role: 'admin', active: true):
      print('Admin is active');
      break;
    default:
      print('Other user');
  }
}
```

Expected output:

```text
Admin is active
```

This is a neat way to branch based on structured data.

## Senior Trick: Match The Shape You Actually Care About

Pattern matching is most useful when the structure itself matters.

Do not overcomplicate simple logic that is clearer with a basic `if`.

## Senior Trick: Let Patterns Replace Repetitive Condition Checks

If you are checking the same fields one by one, a pattern may express the idea better.

That can make the code shorter and more readable.

## Summary

- pattern matching checks the shape of data
- it works well with records and structured values
- it can reduce repetitive extraction code
- use it when the shape matters

## Flutter Connection

Pattern matching is useful in Flutter for state handling, route results, API model decisions, and UI branching.
