# Writing Files

## Learning Goal

In this lesson, you will learn how to write and append text to a file in Dart.

## What Does Writing A File Mean

Writing a file means saving content to disk so it can be read later.

You can either replace the file content or add to it.

## Basic Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/lesson_note.txt');
  file.writeAsStringSync('Lesson 17 started');

  print('Saved: ${file.path}');
  print('Content: ${file.readAsStringSync()}');
}
```

Expected output:

```text
Saved: /var/folders/.../T/lesson_note.txt
Content: Lesson 17 started
```

This shows the simplest write flow: create the file, write content, then read it back to verify.

## Why This Is Useful

Writing files is essential for:

- saving user preferences
- storing logs
- exporting reports
- caching results
- creating backup data

## Real-World Example

```dart
import 'dart:io';

void main() {
  final file = File('${Directory.systemTemp.path}/activity_log.txt');

  file.writeAsStringSync('App opened\n');
  file.writeAsStringSync('User clicked save\n', mode: FileMode.append);
  file.writeAsStringSync('App closed\n', mode: FileMode.append);

  print(file.readAsStringSync());
}
```

Expected output:

```text
App opened
User clicked save
App closed
```

This demonstrates overwrite and append behavior in one place.

## Senior Trick: Decide Between Overwrite And Append

Writing a file is not one single behavior.

Ask whether you want to:

- replace the whole file
- append new data
- preserve the existing content

That choice matters a lot in real applications.

## Senior Trick: Confirm The Write Worked

In important workflows, do not assume the save succeeded.

Read the file back, check for errors, or log the result when needed.

## Summary

- writing saves data to disk
- you can overwrite or append
- writes are used for logs, settings, and exports
- verifying the write is often a good idea

## Flutter Connection

In Flutter, writing files is useful for cache data, user-generated content, exports, and app state that should survive restarts.
