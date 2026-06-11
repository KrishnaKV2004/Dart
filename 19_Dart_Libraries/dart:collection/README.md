# `dart:collection`

## Learning Goal

In this lesson, you will learn what `dart:collection` provides and when it is useful beyond the basic `List`, `Map`, and `Set` types.

## What Is `dart:collection`

`dart:collection` contains collection utilities and specialized collection classes.

It is useful when the default collection types are not enough for your design.

## Basic Example

```dart
import 'dart:collection';

void main() {
  final queue = Queue<int>();
  queue.addAll([1, 2, 3]);

  print(queue.first);
  print(queue.last);
}
```

Expected output:

```text
1
3
```

The queue gives you collection behavior with a specific ordering model.

## Why This Is Useful

This library helps when you need:

- queues
- specialized collection behavior
- controlled collection access
- collection wrappers

## Real-World Example

```dart
import 'dart:collection';

void main() {
  final queue = Queue<String>();
  queue.add('Task 1');
  queue.add('Task 2');
  queue.add('Task 3');

  while (queue.isNotEmpty) {
    print(queue.removeFirst());
  }
}
```

Expected output:

```text
Task 1
Task 2
Task 3
```

This shows a simple first-in, first-out workflow.

## Senior Trick: Use Specialized Collections Only When They Match The Problem

If a plain list is enough, use a plain list.

If the problem is actually a queue, a specialized collection can make the code clearer.

## Senior Trick: Match Collection Type To Behavior

Choosing the correct collection type is part of good design.

The collection should describe how the data is meant to behave.

## Summary

- `dart:collection` provides specialized collection tools
- it is useful when regular collections are not enough
- queues are a common example
- collection type should match the problem

## Flutter Connection

Specialized collections can help in Flutter for task queues, ordered workflows, and internal state management logic.
