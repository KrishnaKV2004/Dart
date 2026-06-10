# File Operations

## Learning Goal

In this lesson, you will learn the common operations you can perform on files after they already exist.

## What Are File Operations

File operations include tasks like:

- checking whether a file exists
- reading metadata
- copying a file
- renaming a file
- deleting a file

## Basic Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/ops_demo.txt');
  file.writeAsStringSync('File operations demo');

  print('Exists: ${file.existsSync()}');
  print('Length: ${file.lengthSync()} bytes');
}
```

Expected output:

```text
Exists: true
Length: 20 bytes
```

The file exists, and Dart can inspect its size.

## Why This Is Useful

File operations are important when your code needs to manage files, not just read or write them.

That includes:

- cleanup tools
- backup systems
- import/export features
- logging systems

## Real-World Example

```dart
import 'dart:io';

void main() {
  final tempDir = Directory.systemTemp.createTempSync('lesson17_');
  final source = File('${tempDir.path}/source.txt');
  source.writeAsStringSync('Original data');

  final copy = source.copySync('${tempDir.path}/copy.txt');
  final renamed = copy.renameSync('${tempDir.path}/renamed.txt');

  print('Source exists: ${source.existsSync()}');
  print('Copied file: ${copy.path}');
  print('Renamed file: ${renamed.path}');
}
```

Expected output:

```text
Source exists: true
Copied file: /var/folders/.../T/lesson17_xxx/copy.txt
Renamed file: /var/folders/.../T/lesson17_xxx/renamed.txt
```

This shows the lifecycle of a file beyond simple reading and writing.

## Senior Trick: Check Before You Delete

Deleting files is powerful and permanent.

Before deletion, make sure:

- you are targeting the correct file
- the file is no longer needed
- the operation is safe for the user

## Senior Trick: Use Temporary Data For Practice

When experimenting with file operations, use temporary directories first.

That keeps your real workspace safe while you test behavior.

## Summary

- file operations manage existing files
- common actions include exist, copy, rename, and delete
- metadata like file size can be inspected
- deletion should always be deliberate

## Flutter Connection

File operations are useful in Flutter when cleaning up cache, moving exports, managing downloads, or maintaining local storage.
