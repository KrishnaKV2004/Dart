# do while

## Learning Goal

In this lesson, you will learn how `do while` works and when it is useful.

## What Is `do while`

A `do while` loop runs the loop body first, then checks the condition.

That means it always runs at least once.

## Basic Example

```dart
void main() {
  int count = 1;

  do {
    print(count);
    count++;
  } while (count <= 3);
}
```

## Why It Is Different From `while`

With a `while` loop, the condition is checked first.
With `do while`, the code runs first.

## Example

```dart
void main() {
  int count = 5;

  do {
    print('This runs once');
  } while (count < 3);
}
```

Even though `count < 3` is false, the block still runs once.

## Real-World Example

```dart
void main() {
  String? menuChoice;

  do {
    print('Show menu');
    menuChoice = 'exit';
  } while (menuChoice != 'exit');
}
```

This pattern can make sense when a menu or prompt must appear at least once.

## Senior Trick: Use `do while` Only When "At Least Once" Is Meaningful

If the loop should not run unless a condition is already true, use `while` instead.

Choose `do while` only when the first run is intentional.

## Summary

- `do while` runs the body before checking the condition
- it always runs at least once
- it is useful for menus, prompts, or guaranteed-first-pass flows
- do not use it unless that first run is truly desired

## Flutter Connection

You may not use `do while` as often in Flutter UI code, but understanding it helps when writing plain Dart logic that must perform one initial pass before checking continuation conditions.
