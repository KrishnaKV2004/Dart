# `dart:developer`

## Learning Goal

In this lesson, you will learn how `dart:developer` can help with logging, debugging, and performance observation.

## What Is `dart:developer`

`dart:developer` contains tools that are mostly useful when you are debugging or inspecting application behavior.

It is not usually for everyday business logic.

## Basic Example

```dart
import 'dart:developer';

void main() {
  log('Application started');
  print('Running...');
}
```

Expected output:

```text
Application started
Running...
```

The log message is useful during debugging and tracing.

## Why This Is Useful

This library helps with:

- logging
- debugging
- timeline events
- profiling and inspection

## Real-World Example

```dart
import 'dart:developer';

void main() {
  final userId = 101;
  log('Loading user', name: 'Profile', error: null, stackTrace: null);
  print('User ID: $userId');
}
```

Expected output:

```text
User ID: 101
```

The real value is in the developer tooling and tracing behavior.

## Senior Trick: Use Developer Tools For Debugging, Not App Logic

Logging is helpful, but it should not become the program’s business logic.

Keep debug tooling separate from the core domain.

## Senior Trick: Log What Helps You Diagnose Problems

Good logs explain:

- what is happening
- which part of the app is doing it
- what data matters

That makes future debugging much easier.

## Summary

- `dart:developer` supports debugging and tracing
- it is useful for logs and profiling
- it is not usually part of business logic
- good logs help diagnose issues faster

## Flutter Connection

This library is useful in Flutter when you need tracing, performance checks, or structured debug logging during development.
