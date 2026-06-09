# Type Constraints

## Learning Goal

In this lesson, you will learn how to limit generic types so they only accept types with the capabilities you need.

## What Is A Type Constraint

A type constraint tells Dart that a generic type must extend or implement a specific type.

This is usually written as:

```dart
T extends SomeType
```

## Basic Example

```dart
T larger<T extends Comparable<T>>(T a, T b) {
  return a.compareTo(b) > 0 ? a : b;
}

void main() {
  print(larger<int>(5, 9));
  print(larger<String>('cat', 'dog'));
}
```

The function only works with types that can be compared.

## Why This Matters

Constraints make your generic code safer.

They help Dart know which methods or properties are available on the type.

Without a constraint, you may not be allowed to call the operations your code needs.

## Real-World Example

```dart
class Repository<T extends Object> {
  final List<T> items = [];

  void add(T item) {
    items.add(item);
  }
}

void main() {
  Repository<String> repository = Repository();
  repository.add('Dart');

  print(repository.items);
}
```

This keeps the repository generic, but still prevents unsupported null-like values by design.

## Senior Trick: Constrain The Type, Not The Problem

If your code needs comparison, use a comparable constraint.

If it needs a specific base class, constrain it that way.

Do not write unconstrained generic code and then patch it with runtime checks later.

## Senior Trick: Use Constraints To Make APIs Honest

A good constraint tells the reader exactly what the function or class expects.

That means fewer surprises and fewer hidden assumptions.

## Summary

- type constraints restrict what a generic type can be
- they make generic code safer and more predictable
- they allow access to needed methods or properties
- they improve API clarity

## Flutter Connection

Constraints are useful in Flutter for:

- generic repositories
- state helpers
- utility classes
- reusable model logic

They help keep your app architecture strongly typed and easier to maintain.
