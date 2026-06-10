# First Class Functions

## Learning Goal

In this lesson, you will learn what it means for functions to be first-class values in Dart.

## What Are First Class Functions

Functions are first-class in Dart, which means you can:

- assign them to variables
- pass them as arguments
- return them from other functions

That makes functions as flexible as any other value.

## Basic Example

```dart
void greet() {
  print('Hello');
}

void main() {
  var action = greet;
  action();
}
```

The function is stored in a variable and called later.

## Why This Is Useful

First-class functions make your code more flexible.

They are a big part of:

- callbacks
- event handling
- reusable utilities
- higher-order functions

## Real-World Example

```dart
void logMessage(String message) {
  print(message);
}

void runTask(void Function(String) logger) {
  logger('Task started');
}

void main() {
  runTask(logMessage);
}
```

The function is passed into another function as behavior.

## Senior Trick: Think Of Functions As Tools

When you treat functions like values, you can compose behavior more cleanly.

That helps you separate:

- what should happen
- from when it should happen

## Senior Trick: Keep Function Values Easy To Read

If a function reference makes the code harder to understand, give it a clear name or keep the logic nearby.

Flexibility is useful, but readability still wins.

## Summary

- functions are first-class values in Dart
- they can be stored, passed, and returned
- they power callbacks and higher-order functions
- they make behavior reusable

## Flutter Connection

First-class functions are everywhere in Flutter for event handlers, builders, callbacks, and state updates.
