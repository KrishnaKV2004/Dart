# Packages

## Learning Goal

In this lesson, you will learn what a package is and why Dart uses packages to share reusable code.

## What Is A Package

A package is a reusable bundle of Dart code.

It may include:

- Dart source files
- configuration
- documentation
- assets
- tests

## Basic Example

```dart
import 'dart:math';

void main() {
  final random = Random();
  print(random.nextInt(10));
}
```

Expected output:

```text
7
```

The exact value changes, but the example shows how code from a package or library can be reused in your program.

## Why Packages Matter

Packages help you avoid reinventing the wheel.

They let you use:

- tested utilities
- third-party functionality
- shared internal tools
- reusable app features

## Real-World Example

```dart
class Logger {
  void info(String message) {
    print('[INFO] $message');
  }
}

void main() {
  final logger = Logger();
  logger.info('App started');
}
```

Expected output:

```text
[INFO] App started
```

This shows the kind of reusable logic that often lives inside a package.

## Senior Trick: Prefer Small, Focused Packages

A package should usually solve one clear problem well.

Smaller packages are easier to understand, test, and reuse.

## Senior Trick: Use Packages To Separate Responsibilities

If code is becoming hard to maintain inside one app layer, a package or module boundary may help make the design cleaner.

## Summary

- packages are reusable bundles of Dart code
- they can include source, docs, tests, and assets
- packages help with reuse and organization
- focused packages are easier to manage

## Flutter Connection

Flutter apps rely heavily on packages for UI widgets, networking, state management, and more.
