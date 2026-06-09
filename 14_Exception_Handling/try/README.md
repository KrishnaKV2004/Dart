# try

## Learning Goal

In this lesson, you will learn how to use `try` blocks to run code that may fail.

## What Does `try` Do

A `try` block wraps risky code so you can handle exceptions instead of letting them crash the app immediately.

## Basic Example

```dart
void main() {
  try {
    int number = int.parse('abc');
    print(number);
  } catch (e) {
    print('Something went wrong');
  }
}
```

The code inside `try` is the part that may fail.

## Why This Is Useful

`try` gives you a place to isolate dangerous operations such as:

- parsing
- file access
- network calls
- data conversion

This lets you recover or show a helpful message.

## Real-World Example

```dart
void main() {
  try {
    List<int> numbers = [1, 2, 3];
    print(numbers[10]);
  } catch (e) {
    print('Index was invalid');
  }
}
```

The risky code is isolated so the failure is controlled.

## Senior Trick: Keep `try` Blocks Small

Do not wrap huge sections of code in one `try` block.

Smaller `try` blocks make it much easier to see exactly what may fail.

## Senior Trick: Only Put Risky Code Inside `try`

If safe code is inside the same block, debugging becomes harder.

Keep the block focused so the failure point is obvious.

## Summary

- `try` wraps code that may fail
- it is used with `catch`, `on`, or `finally`
- small `try` blocks are easier to maintain
- isolate only the risky logic

## Flutter Connection

In Flutter, `try` is commonly used around parsing, async work, storage access, and API handling.
