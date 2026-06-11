# `dart:async`

## Learning Goal

In this lesson, you will learn what `dart:async` provides for futures, streams, timers, and asynchronous control.

## What Is `dart:async`

`dart:async` contains the tools that Dart uses for asynchronous programming.

It includes:

- `Future`
- `Stream`
- `Timer`
- `Completer`
- async utilities

## Basic Example

```dart
import 'dart:async';

void main() async {
  final value = await Future.delayed(const Duration(seconds: 1), () => 'Done');
  print(value);
}
```

Expected output:

```text
Done
```

The delay represents work that finishes later.

## Why This Is Useful

This library powers:

- network requests
- delays
- stream listening
- async coordination

It is one of the most important Dart libraries for real apps.

## Real-World Example

```dart
import 'dart:async';

void main() {
  final timer = Timer(const Duration(seconds: 1), () {
    print('Timer finished');
  });

  print('Waiting...');
}
```

Expected output:

```text
Waiting...
Timer finished
```

This shows how async work can continue after the first line finishes.

## Senior Trick: Use Async Tools For Timing, Not Just Syntax

The real value of `dart:async` is controlling how work happens over time.

Think in terms of event flow, not just future syntax.

## Senior Trick: Keep Async APIs Predictable

When you expose async behavior, make it clear whether the caller should await a result, listen to a stream, or handle a timer/event.

That clarity prevents confusion.

## Summary

- `dart:async` supports asynchronous programming
- it includes futures, streams, and timers
- it is essential for waiting and event-based code
- it helps manage time-based behavior cleanly

## Flutter Connection

Flutter depends heavily on `dart:async` for loading data, timers, stream updates, and event-driven behavior.
