# Importing Libraries

## Learning Goal

In this lesson, you will learn how to bring Dart libraries into scope with `import`.

## What Does `import` Do

`import` makes code from another library available in your file.

Without imports, your file can only use what it already defines.

## Basic Example

```dart
import 'dart:math';

void main() {
  final random = Random();
  print(random.nextInt(100));
}
```

Expected output:

```text
58
```

The exact number changes, but the import gives you access to `Random`.

## Why This Is Useful

Imports let you use:

- core Dart libraries
- local project files
- third-party packages

## Real-World Example

```dart
import 'dart:convert';

void main() {
  final json = '{"name":"Asha"}';
  final decoded = jsonDecode(json);

  print(decoded);
}
```

Expected output:

```text
{name: Asha}
```

This shows how imports unlock useful library functions.

## Senior Trick: Import Only What You Need

Too many imports make files harder to scan.

Keep your dependencies focused and intentional.

## Senior Trick: Know The Difference Between Library Imports And File Imports

Importing a core library is not the same as importing another file in your project.

Both are useful, but they solve different problems.

## Summary

- `import` brings library code into a file
- imports can target core libraries, packages, or local files
- keep imports focused
- imports are part of design, not just syntax

## Flutter Connection

Imports are everywhere in Flutter, especially for widgets, utilities, models, and package APIs.
