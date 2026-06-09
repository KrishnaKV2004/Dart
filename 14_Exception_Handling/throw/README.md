# throw

## Learning Goal

In this lesson, you will learn how to intentionally throw exceptions in Dart.

## What Does `throw` Do

The `throw` keyword creates an exception and stops the current flow of execution.

It is useful when your code detects an invalid or unsupported condition.

## Basic Example

```dart
void validateAge(int age) {
  if (age < 0) {
    throw Exception('Age cannot be negative');
  }
}

void main() {
  validateAge(-1);
}
```

## Why This Is Useful

`throw` tells the caller that something is wrong and the current operation cannot continue safely.

This is better than letting invalid data move deeper into the program.

## Real-World Example

```dart
double withdraw(double balance, double amount) {
  if (amount > balance) {
    throw Exception('Insufficient balance');
  }

  return balance - amount;
}
```

This protects the business rule directly.

## Senior Trick: Throw For Invalid State, Not For Normal Decisions

Do not use `throw` as a replacement for ordinary `if`/`else` logic.

Use it when the condition means the operation should fail, not when you simply want to choose one branch.

## Senior Trick: Make Exception Messages Useful

A weak exception message is hard to debug.

A useful message explains:

- what failed
- why it failed
- sometimes what the caller should do next

## Summary

- `throw` creates an exception manually
- it stops the current operation
- it is best for invalid or unsupported conditions
- clear messages make debugging easier

## Flutter Connection

In Flutter, `throw` is useful inside validation, repositories, services, and parsing code when an operation should not continue with invalid data.
