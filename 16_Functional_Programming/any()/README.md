# `any()`

## Learning Goal

In this lesson, you will learn how `any()` checks whether at least one item matches a condition.

## What Does `any()` Do

`any()` returns `true` if at least one item in the collection satisfies the condition.

Otherwise, it returns `false`.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 3, 5, 8];
  bool hasEven = numbers.any((n) => n % 2 == 0);

  print(hasEven);
}
```

The result is `true` because one item matches.

## Why This Is Useful

`any()` is useful when you only need to know whether a match exists.

You do not need to scan the collection manually.

## Real-World Example

```dart
void main() {
  List<String> names = ['Asha', 'Ravi', 'Nina'];
  bool hasLongName = names.any((name) => name.length > 4);

  print(hasLongName);
}
```

This gives a simple yes/no answer.

## Senior Trick: Use `any()` For Existence Checks

If you only care whether at least one match exists, `any()` is cleaner than writing a loop.

It says exactly what you mean.

## Senior Trick: Prefer Intent Over Loop Mechanics

The strength of `any()` is clarity.

It communicates the question directly instead of exposing iteration details.

## Summary

- `any()` checks whether at least one item matches
- it returns a boolean
- it is ideal for existence checks
- it makes intent obvious

## Flutter Connection

`any()` is useful in Flutter for validation, selection logic, and checking whether a condition appears in a list of data.
