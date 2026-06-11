# Lesson 19: Dart Libraries

This section teaches the built-in Dart libraries that power everyday programming tasks such as time handling, JSON, files, math, collections, and debugging.

Dart ships with a strong standard library, and learning it well gives you a big advantage because you can solve many problems without adding extra dependencies.

## Topics In This Lesson

1. [`dart:core`](./dart:core/README.md)
2. [`dart:async`](./dart:async/README.md)
3. [`dart:collection`](./dart:collection/README.md)
4. [`dart:convert`](./dart:convert/README.md)
5. [`dart:developer`](./dart:developer/README.md)
6. [`dart:io`](./dart:io/README.md)
7. [`dart:math`](./dart:math/README.md)

## Why This Lesson Matters

The Dart SDK already gives you a lot of useful tools.

These libraries help with:

- basic data types and utilities
- asynchronous programming
- collection helpers
- JSON and text conversion
- debugging
- file and console work
- math and random values

Knowing the standard libraries well keeps your code simpler and more reliable.

## Senior Developer Mindset For Dart Libraries

Strong developers do not reach for external packages first.

They ask:

- does Dart already provide this?
- is the built-in API enough?
- is there a smaller and safer solution in the standard library?

That habit often leads to cleaner and more stable code.

## What You Should Learn Here

By the end of this section, you should be able to:

- use core Dart types and helpers
- work with async primitives
- use collection utilities
- encode and decode JSON
- use basic debugging tools
- work with files and console I/O
- use math and random helpers

## Real-World Example

```dart
import 'dart:convert';
import 'dart:math';

void main() {
  final data = {'score': Random().nextInt(100)};
  final json = jsonEncode(data);

  print(json);
}
```

Expected output:

```text
{"score":42}
```

The exact number will vary, but the example shows how Dart libraries can work together in one small flow.

## Senior Trick: Use The Smallest Library That Solves The Problem

If `dart:core` already covers the need, do not add complexity.

If `dart:convert` can handle your JSON, do not manually build strings.

Good library choices make code easier to trust.

## Summary

- Dart includes many useful built-in libraries
- standard libraries solve common programming tasks
- using them well reduces extra dependencies
- each library has a clear area of responsibility

## Flutter Connection

These libraries are used constantly in Flutter for:

- model parsing
- networking
- local files
- async work
- debugging
- app logic and utilities

If you know the Dart libraries well, a lot of Flutter code becomes much easier to understand.
