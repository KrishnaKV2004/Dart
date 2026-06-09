# on

## Learning Goal

In this lesson, you will learn how to catch only specific exception types using `on`.

## What Does `on` Do

The `on` keyword is used with `try` to handle a particular exception type.

It is useful when different errors need different responses.

## Basic Example

```dart
void main() {
  try {
    int value = int.parse('abc');
    print(value);
  } on FormatException {
    print('The input was not a valid number');
  }
}
```

This only handles `FormatException`.

## Why This Is Useful

`on` makes exception handling more precise.

It is better than catching every error the same way when you know the type matters.

## Real-World Example

```dart
void main() {
  try {
    List<int> numbers = [1, 2, 3];
    print(numbers[10]);
  } on RangeError {
    print('Index out of range');
  }
}
```

The response is tailored to the specific problem.

## Senior Trick: Use `on` For Known Failure Types

If your program can recover differently depending on the exception class, `on` is the cleanest tool.

It keeps the logic readable and intentional.

## Senior Trick: Combine `on` With `catch` When Needed

You can also write:

```dart
on FormatException catch (e) {
  print(e);
}
```

That gives you both the type-specific handling and access to the exception value.

## Summary

- `on` catches a specific exception type
- it makes handling more precise
- it is useful when different exceptions need different responses
- it can be combined with `catch`

## Flutter Connection

In Flutter, `on` is helpful when you want separate handling for parsing errors, network errors, or range-related failures.
