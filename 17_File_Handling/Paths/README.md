# Paths

## Learning Goal

In this lesson, you will learn how Dart uses file paths to locate files and directories.

## What Is A Path

A path is the address of a file or folder on disk.

Paths can be:

- absolute, such as a full system location
- relative, such as a path based on the current directory

## Basic Example

```dart
import 'dart:io';

void main() {
  final tempDir = Directory.systemTemp.path;
  final filePath = '$tempDir${Platform.pathSeparator}notes.txt';

  print('Temp directory: $tempDir');
  print('File path: $filePath');
}
```

Expected output:

```text
Temp directory: /var/folders/.../T
File path: /var/folders/.../T/notes.txt
```

The exact path will differ by machine, but the structure is the same.

## Why Paths Matter

If the path is wrong, file code fails even if the file logic itself is correct.

Paths are the foundation of file access.

## Real-World Example

```dart
import 'dart:io';

void main() {
  final folder = Directory.systemTemp.path;
  final path = '$folder${Platform.pathSeparator}reports${Platform.pathSeparator}daily.txt';

  print(path);
}
```

Expected output:

```text
/tmp/reports/daily.txt
```

The separator is important because path syntax can differ across platforms.

## Senior Trick: Do Not Hardcode Path Formats

If you build paths by manually guessing separators, your code may break on another platform.

Use `Platform.pathSeparator` when you need to compose paths safely.

## Senior Trick: Know The Difference Between File Path And Directory Path

A file path points to a file.

A directory path points to a folder.

That sounds simple, but confusing the two is a common source of bugs.

## Summary

- a path tells Dart where a file or folder lives
- paths may be absolute or relative
- separators can differ by platform
- correct path building is essential for file work

## Flutter Connection

Paths matter in Flutter when you work with cache files, app documents, exports, or any file stored on the device.
