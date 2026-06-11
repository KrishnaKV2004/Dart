# `dart:io`

## Learning Goal

In this lesson, you will learn how `dart:io` supports files, directories, stdin/stdout, and other system-level operations.

## What Is `dart:io`

`dart:io` provides input/output APIs for working with the operating system.

It is commonly used for:

- files
- directories
- console input and output
- network sockets
- process interaction

## Basic Example

```dart
import 'dart:io';

void main() {
  stdout.writeln('Enter a value:');
}
```

Expected output:

```text
Enter a value:
```

This is a simple console I/O example using the system output stream.

## Why This Is Useful

`dart:io` is essential for command-line apps and local file handling.

It is also useful in tools and backend-style Dart programs.

## Real-World Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/io_demo.txt');
  file.writeAsStringSync('Hello IO');

  print(file.readAsStringSync());
}
```

Expected output:

```text
Hello IO
```

This shows the file system side of `dart:io`.

## Senior Trick: Remember Platform Differences

File paths, permissions, and available features can vary by operating system.

Write with that in mind when your code needs to run in different environments.

## Senior Trick: Use `dart:io` Where The Platform Makes Sense

This library is great for local tools, server apps, and command-line workflows.

It is not always available in every runtime environment, so make sure it fits the target.

## Summary

- `dart:io` handles system-level I/O
- it is used for files, directories, and console work
- it is important in CLI and backend-style Dart code
- platform differences matter

## Flutter Connection

Flutter uses `dart:io` for local files, exports, downloads, and some platform-specific workflows.
