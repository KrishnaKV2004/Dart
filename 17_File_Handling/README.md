# Lesson 17: File Handling

This section teaches how to work with files and directories in Dart so your programs can save, load, inspect, and manage data on disk.

File handling is important because real apps often need to persist data outside memory, whether that is a config file, a report, or cached content.

## Topics In This Lesson

1. [Paths](./Paths/README.md)
2. [Reading Files](./Reading%20Files/README.md)
3. [Writing Files](./Writing%20Files/README.md)
4. [File Operations](./File%20Operations/README.md)
5. [Directories](./Directories/README.md)

## Why This Lesson Matters

If your app only keeps data in memory, everything disappears when the program ends.

File handling lets you:

- read existing data
- save user data
- build logs
- cache results
- manage folders and files safely

That is a big step toward building real-world tools and applications.

## Senior Developer Mindset For File Handling

Strong developers treat file work as something that needs careful boundaries.

A good rule is:

- know where files live
- check whether they exist
- handle read and write failures
- create directories intentionally
- clean up temporary files when possible

File code should be predictable and safe, not fragile.

## What You Should Learn Here

By the end of this section, you should be able to:

- understand file paths and separators
- read text from files
- write and append data to files
- check existence and file metadata
- copy, rename, and delete files
- create and inspect directories

## Real-World Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/lesson17_demo.txt');
  file.writeAsStringSync('Hello from Lesson 17');

  final content = file.readAsStringSync();
  print(content);
}
```

Expected output:

```text
Hello from Lesson 17
```

This shows the core idea of file handling: save data first, then read it back later.

## Senior Trick: Treat File Paths As Part Of The Design

File handling bugs often come from path mistakes, not just file logic.

Think carefully about:

- absolute vs relative paths
- platform separators
- where temporary data should live
- whether the app should create the folder first

Small path mistakes can cause big headaches later.

## Summary

- file handling lets Dart work with persistent data
- paths tell you where files and folders live
- reading and writing are the core operations
- file operations help manage existing files
- directories organize data on disk

## Flutter Connection

File handling is useful in Flutter for:

- local cache files
- settings
- logs
- downloaded data
- export and import features

If you understand file handling well, you can build apps that remember things properly.
