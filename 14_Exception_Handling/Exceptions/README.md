# Exceptions

## Learning Goal

In this lesson, you will learn what exceptions are and why they matter in Dart programs.

## What Is An Exception

An exception is a runtime problem that interrupts normal program flow.

It usually happens when something goes wrong that the code did not expect or could not safely continue from.

## Basic Example

```dart
void main() {
  int number = int.parse('abc');
  print(number);
}
```

This will fail because `'abc'` cannot be converted into an integer.

## Why Exceptions Matter

Exceptions are part of real software.

They can happen because of:

- bad input
- missing files
- invalid state
- network failure
- parsing problems

If you do not understand exceptions, your code will eventually surprise you.

## Real-World Example

```dart
void main() {
  List<int> scores = [10, 20, 30];
  print(scores[5]);
}
```

This fails because the index does not exist.

## Senior Trick: Expect Failure In External Input

Anything coming from outside your code can fail:

- user input
- API responses
- files
- databases

Do not assume these values are always correct.

## Senior Trick: Separate Expected Failures From Bugs

Some exceptions are part of normal application flow.

Others signal a real bug.

Good developers know which is which, so they do not hide serious issues behind generic error handling.

## Summary

- exceptions are runtime problems
- they interrupt normal flow
- they often come from invalid input or unexpected state
- good code expects and manages them

## Flutter Connection

Exceptions appear often in Flutter when reading input, fetching network data, parsing JSON, or accessing unavailable resources.
