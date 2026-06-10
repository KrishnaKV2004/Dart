# Async Generators

## Learning Goal

In this lesson, you will learn how to generate stream values asynchronously using `async*` and `yield`.

## What Is An Async Generator

An async generator is a function that produces a stream of values over time.

It uses:

- `async*` to mark the generator
- `yield` to emit values

## Basic Example

```dart
Stream<int> count() async* {
  yield 1;
  yield 2;
  yield 3;
}
```

This produces one value after another.

## Why This Is Useful

Async generators are useful when you want to build a stream in a simple and readable way.

They are often cleaner than manually pushing values with a controller.

## Real-World Example

```dart
Stream<String> steps() async* {
  yield 'Start';
  await Future.delayed(const Duration(seconds: 1));
  yield 'Middle';
  await Future.delayed(const Duration(seconds: 1));
  yield 'End';
}
```

This models a timed sequence of async events.

## Senior Trick: Use Async Generators For Simple Stream Creation

If the stream comes from a clear sequence of steps, `async*` is elegant and easy to read.

It is often the simplest way to build a stream.

## Senior Trick: Keep Emission Logic Easy To Follow

Each `yield` should make sense in the flow.

If the function becomes too complex, consider splitting the logic.

## Summary

- async generators create streams
- they use `async*` and `yield`
- they are useful for readable stream creation
- they are often simpler than manual controllers

## Flutter Connection

Async generators can be helpful in Flutter when you want to create timed flows, progress streams, or simple reactive sequences.
