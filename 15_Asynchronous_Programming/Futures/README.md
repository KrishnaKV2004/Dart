# Futures

## Learning Goal

In this lesson, you will learn what a Future is and how it represents a value that will be available later.

## What Is A Future

A `Future` is an object that represents a result that is not ready yet.

It can eventually complete with:

- a value
- an error

## Basic Example

```dart
Future<String> loadData() {
  return Future.delayed(const Duration(seconds: 1), () => 'Loaded');
}

void main() {
  print(loadData());
}
```

The result is not available immediately.

## Why Futures Matter

Futures are the foundation of async programming in Dart.

They are used for:

- network requests
- file operations
- database calls
- delayed work

## Real-World Example

```dart
Future<int> getUserId() async {
  return 101;
}
```

Even simple-looking async APIs often use `Future` so they can fit into a consistent async model.

## Senior Trick: A Future Is A Promise Of Data, Not Data Yet

Do not treat a future like the actual value.

You must wait for it to complete before using the result.

## Senior Trick: Design Future APIs To Be Predictable

If a function returns a `Future`, make the caller understand:

- what it is waiting for
- what might fail
- when it should be awaited

Clear naming helps a lot here.

## Summary

- a future represents a result that arrives later
- it can complete with a value or an error
- it is the basis of async Dart
- future-based APIs are common in real apps

## Flutter Connection

Flutter uses futures constantly for loading data, saving data, and waiting on async operations.
