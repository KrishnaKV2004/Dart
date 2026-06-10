# Stream Controllers

## Learning Goal

In this lesson, you will learn how to create and control streams manually with a stream controller.

## What Is A Stream Controller

A stream controller lets you add data, errors, or completion events to a stream yourself.

It gives you more direct control over the stream source.

## Basic Example

```dart
import 'dart:async';

void main() {
  final controller = StreamController<int>();

  controller.stream.listen((value) {
    print(value);
  });

  controller.add(1);
  controller.add(2);
  controller.close();
}
```

The controller pushes values into the stream.

## Why This Is Useful

Stream controllers are helpful when:

- you need custom stream sources
- values come from callbacks or events
- you want manual control over stream emission

## Real-World Example

```dart
import 'dart:async';

void main() {
  final controller = StreamController<String>();

  controller.stream.listen((message) {
    print(message);
  });

  controller.add('New notification');
  controller.close();
}
```

This is a simple event-publishing pattern.

## Senior Trick: Always Close Controllers

Stream controllers hold resources.

If you create one, make sure you close it when you are done.

## Senior Trick: Use Controllers For Event Sources, Not Random State

Controllers are best when you are managing a stream of events.

If you just need a simple value, a controller may be unnecessary.

## Summary

- stream controllers manually emit stream events
- they are useful for custom event sources
- they should be closed when finished
- they are best for event-driven designs

## Flutter Connection

Stream controllers are often used in Flutter for custom reactive flows, input events, and state broadcasting.
