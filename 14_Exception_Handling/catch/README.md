# catch

## Learning Goal

In this lesson, you will learn how to catch exceptions and respond to failures safely.

## What Does `catch` Do

`catch` receives an exception thrown inside a `try` block so you can handle it.

## Basic Example

```dart
void main() {
  try {
    int value = int.parse('abc');
    print(value);
  } catch (e) {
    print('Error: $e');
  }
}
```

The `catch` block runs when something inside `try` fails.

## Why This Is Useful

`catch` lets you:

- show a user-friendly message
- log the problem
- recover with fallback logic
- stop the app from crashing unexpectedly

## Real-World Example

```dart
double parsePrice(String value) {
  try {
    return double.parse(value);
  } catch (e) {
    return 0.0;
  }
}
```

This gives the caller a safe fallback value.

## Senior Trick: Catch Specific Failures When Possible

Do not catch everything blindly if you know the exact failure type.

Specific handling makes code clearer and safer.

## Senior Trick: Use The Stack Trace When Debugging

If you need to diagnose a real problem, capture the stack trace so you know where the exception came from.

That helps a lot in larger applications.

## Summary

- `catch` handles exceptions from `try`
- it is useful for logging, recovery, and user messages
- specific handling is better than blind handling
- stack traces help with debugging

## Flutter Connection

`catch` is very common in Flutter for API errors, parsing issues, storage failures, and async operations that can fail.
