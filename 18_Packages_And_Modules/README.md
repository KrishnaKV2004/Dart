# Lesson 18: Packages And Modules

This section teaches how Dart code is organized, shared, and reused through packages, libraries, imports, exports, and versioned dependencies.

Understanding packages and modules is essential once your code base grows beyond a single file or a single app.

## Topics In This Lesson

1. [Packages](./Packages/README.md)
2. [pubspec.yaml](./pubspec.yaml/README.md)
3. [Importing Libraries](./Importing%20Libraries/README.md)
4. [Exporting Libraries](./Exporting%20Libraries/README.md)
5. [Creating Packages](./Creating%20Packages/README.md)
6. [Versioning](./Versioning/README.md)

## Why This Lesson Matters

Real Dart projects are not just one file with a `main()` function.

They are built from:

- reusable libraries
- external packages
- internal modules
- shared utilities
- versioned dependencies

If you understand this layer well, you can build cleaner apps and use other people’s code safely.

## Senior Developer Mindset For Packages And Modules

Strong developers think about code boundaries.

A good rule is:

- keep responsibilities separated
- import only what you need
- export a clean public API
- pin versions carefully
- avoid making dependency structure messy

Good package design makes code easier to reuse and easier to maintain.

## What You Should Learn Here

By the end of this section, you should be able to:

- understand what a package is
- read and edit `pubspec.yaml`
- import libraries correctly
- export internal libraries through a public API
- create a basic reusable package
- think about versioning and dependency safety

## Real-World Example

```dart
import 'dart:math';

void main() {
  final random = Random();
  final value = random.nextInt(100);

  print('Random value: $value');
}
```

Expected output:

```text
Random value: 42
```

The exact number will vary, but the example shows how a library becomes a reusable tool you can import and use.

## Senior Trick: Treat Imports Like Dependencies, Not Decorations

An import is not just a line at the top of the file.

It is a dependency decision.

Ask:

- do I actually need this library?
- is there a cleaner internal module I should use?
- am I exposing too much through exports?

That habit keeps projects tidy.

## Summary

- packages group reusable Dart code
- `pubspec.yaml` describes dependencies and metadata
- imports bring libraries into scope
- exports define what a package exposes
- versioning helps keep dependencies stable

## Flutter Connection

Packages and modules are everywhere in Flutter:

- app dependencies
- plugin packages
- shared utilities
- feature modules
- internal architecture layers

If you understand this lesson well, managing Flutter projects becomes much easier.
