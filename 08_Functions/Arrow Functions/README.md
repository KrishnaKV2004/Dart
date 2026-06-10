# Arrow Functions

## Learning Goal

In this lesson, you will learn how arrow functions provide a short syntax for simple functions.

## What Is An Arrow Function

An arrow function uses `=>` to return a single expression.

## Basic Example

```dart
int square(int number) => number * number;

void main() {
  print(square(4));
}
```

## Why Arrow Functions Are Useful

They are great when the function:

- is short
- returns one expression
- stays easy to read

## Compare With Normal Function Syntax

```dart
int square(int number) {
  return number * number;
}
```

Both are valid.

## Real-World Example

```dart
String formatUserName(String name) => 'User: $name';
```

This is clean and readable because the logic is small.

## Senior Trick: Use Arrow Functions For Simple Intent Only

If logic becomes bigger than one clean expression, switch back to normal block syntax.

Arrow functions should improve readability, not compress complexity.

## Summary

- arrow functions use `=>`
- they are best for short single-expression logic
- use block functions when logic grows

## Flutter Connection

Arrow functions are common in Flutter for:

- small helpers
- callbacks
- compact transformations

You will see them often, so it is good to be comfortable with them early.
