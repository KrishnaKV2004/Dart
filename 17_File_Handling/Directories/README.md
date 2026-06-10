# Directories

## Learning Goal

In this lesson, you will learn how to create, inspect, and manage directories in Dart.

## What Is A Directory

A directory is a folder that can contain files and other directories.

Directories help organize data on disk.

## Basic Example

```dart
import 'dart:io';

void main() {
  final dir = Directory('${Directory.systemTemp.path}/lesson17_folder');
  dir.createSync(recursive: true);

  print('Directory created: ${dir.existsSync()}');
  print('Path: ${dir.path}');
}
```

Expected output:

```text
Directory created: true
Path: /var/folders/.../T/lesson17_folder
```

The folder is created if it does not already exist.

## Why This Is Useful

Directories are used to organize:

- app data
- downloads
- exports
- logs
- temporary working files

## Real-World Example

```dart
import 'dart:io';

void main() {
  final dir = Directory('${Directory.systemTemp.path}/lesson17_list_demo');
  dir.createSync(recursive: true);

  File('${dir.path}/a.txt').writeAsStringSync('A');
  File('${dir.path}/b.txt').writeAsStringSync('B');

  final entries = dir.listSync();
  for (final entry in entries) {
    print(entry.path);
  }
}
```

Expected output:

```text
/var/folders/.../T/lesson17_list_demo/a.txt
/var/folders/.../T/lesson17_list_demo/b.txt
```

This shows how a directory can hold multiple files.

## Senior Trick: Create Parent Folders Intentionally

If your code writes to a nested path, the parent directory may need to be created first.

Do not assume the folder structure already exists.

## Senior Trick: Use Directories To Keep File Systems Organized

Good directory structure makes file handling easier to debug and maintain.

If everything is dumped into one folder, things get messy quickly.

## Summary

- directories are folders on disk
- they can contain files and other directories
- they are important for organizing app data
- creating parent folders carefully avoids errors

## Flutter Connection

Directories matter in Flutter for local storage, caches, logs, downloads, and exported files.
