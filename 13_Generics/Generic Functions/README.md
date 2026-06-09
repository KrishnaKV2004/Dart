# Generic Functions

## Learning Goal

In this lesson, you will learn how to write functions that can work with multiple data types.

## What Is A Generic Function

A generic function is a function that introduces a type parameter, usually written with angle brackets like `<T>`.

This lets the function adapt to the type passed in by the caller.

## Basic Example

```dart
T echo<T>(T value) {
  return value;
}

void main() {
  print(echo<String>('Hello'));
  print(echo<int>(42));
}
```

## Why This Is Useful

Generic functions are helpful when the logic is the same for different types.

You write the behavior once and reuse it safely.

## Real-World Example

```dart
T firstItem<T>(List<T> items) {
  return items[0];
}

void main() {
  List<String> names = ['Asha', 'Ravi'];
  List<int> scores = [10, 20];

  print(firstItem(names));
  print(firstItem(scores));
}
```

The function works for both lists without losing type information.

## Senior Trick: Let Dart Infer The Type When It Can

You do not always need to write `<T>` at the call site.

If the function signature is clear, Dart can often infer the type for you.

That makes the code shorter and easier to read.

## Senior Trick: Use Generic Functions For Shared Logic, Not Special Cases

A generic function is a good choice when the algorithm is the same for many types.

If each type needs different behavior, a generic function may be the wrong tool.

## Summary

- generic functions use type parameters
- they let the same logic work with many types
- they keep type safety intact
- type inference often makes calls cleaner

## Flutter Connection

Generic functions are useful in Flutter for:

- list helpers
- parsing helpers
- mapping data
- reusable utility functions

They help you write flexible helper code without falling back to `dynamic`.
