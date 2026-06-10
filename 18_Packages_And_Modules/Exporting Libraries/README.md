# Exporting Libraries

## Learning Goal

In this lesson, you will learn how `export` helps you expose a clean public API from your package or module.

## What Does `export` Do

`export` makes code from one library available through another library.

This lets you hide internal structure and present a simpler interface.

## Basic Example

```dart
// library.dart
export 'src/helper.dart';
```

```dart
// src/helper.dart
String greet() => 'Hello from helper';
```

If a user imports `library.dart`, they can access `greet()` without knowing where it lives internally.

## Why This Is Useful

Exports help you:

- hide internal folders
- present a cleaner API
- reduce import complexity
- organize large packages

## Real-World Example

```dart
// package.dart
export 'src/logger.dart';
export 'src/parser.dart';
```

This file becomes the public entry point for the package.

## Senior Trick: Export A Clean Surface, Not Your Whole Folder Tree

Good package design often means exposing only the parts users should touch.

That keeps the package easier to understand and less fragile.

## Senior Trick: Use Source Folders Internally

A common pattern is to keep implementation details in `src/` and export only the public pieces.

That gives you more freedom to change internals later.

## Summary

- `export` exposes code through another library
- it helps create clean public APIs
- it hides internal structure
- it is useful for package design

## Flutter Connection

Exports are useful in Flutter packages and internal libraries when you want to present a simple public API to app code.
