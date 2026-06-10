# Creating Packages

## Learning Goal

In this lesson, you will learn the basic shape of a reusable Dart package.

## What Does It Mean To Create A Package

Creating a package means organizing Dart code so it can be reused by other projects.

Usually that includes:

- a `pubspec.yaml`
- library files
- source files
- tests
- documentation

## Basic Example

```dart
class Calculator {
  int add(int a, int b) => a + b;
}

void main() {
  final calculator = Calculator();
  print(calculator.add(3, 4));
}
```

Expected output:

```text
7
```

This is the kind of simple reusable logic that can live inside a package.

## Why This Is Useful

Packages help you share code across:

- projects
- teams
- features
- apps

That reduces duplication and improves consistency.

## Real-World Example

```dart
class StringTools {
  String capitalize(String value) {
    if (value.isEmpty) return value;
    return value[0].toUpperCase() + value.substring(1);
  }
}

void main() {
  final tools = StringTools();
  print(tools.capitalize('dart'));
}
```

Expected output:

```text
Dart
```

This is the kind of reusable utility that is often extracted into a package or shared module.

## Senior Trick: Design A Package Around A Clear Problem

The best packages solve one repeatable problem well.

That makes them easier to test, document, and reuse.

## Senior Trick: Think About The Public API First

Before adding code, ask:

- what should users import?
- what should stay internal?
- what should the package promise?

That keeps the package cleaner from the beginning.

## Summary

- packages are reusable code units
- they usually include config, source, tests, and docs
- package design should be focused
- the public API should stay simple

## Flutter Connection

Creating packages is especially useful in Flutter when building shared widgets, utilities, and reusable feature modules.
