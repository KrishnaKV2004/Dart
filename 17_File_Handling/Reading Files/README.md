# Reading Files

## Learning Goal

In this lesson, you will learn how to read text from a file in Dart.

## What Does Reading A File Mean

Reading a file means loading the content that is already stored on disk and bringing it into your program.

## Basic Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/sample_read.txt');
  file.writeAsStringSync('Dart\nFile reading\nIs useful');

  final content = file.readAsStringSync();
  print(content);
}
```

Expected output:

```text
Dart
File reading
Is useful
```

This example writes a sample file first so the read operation has something to load.

## Why This Is Useful

Reading files is essential for:

- config values
- saved notes
- logs
- reports
- cached data

## Real-World Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/user_profile.txt');
  file.writeAsStringSync('name=Asha\nrole=developer');

  final lines = file.readAsLinesSync();
  for (final line in lines) {
    print(line);
  }
}
```

Expected output:

```text
name=Asha
role=developer
```

This shows how reading files often gives you structured text that you can process line by line.

## Senior Trick: Read Only What You Need

If you only need a few lines or a small section of data, think about whether a full file read is the best approach.

Larger files can take more time and memory.

## Senior Trick: Handle Missing Files Gracefully

A file may not exist when you try to read it.

That is normal in real apps, so reading code should be ready for failure.

## Summary

- reading loads file content into memory
- text files can be read as a full string or as lines
- file reads often power settings, logs, and cached data
- missing files should be handled safely

## Flutter Connection

In Flutter, file reading is common for settings, local storage, cached responses, and exported data.
