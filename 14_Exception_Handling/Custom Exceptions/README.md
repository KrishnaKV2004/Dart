# Custom Exceptions

## Learning Goal

In this lesson, you will learn how to create your own exception types for clearer and more maintainable error handling.

## What Is A Custom Exception

A custom exception is a user-defined exception type that describes a specific failure in your app or domain.

## Basic Example

```dart
class InsufficientBalanceException implements Exception {
  final String message;

  InsufficientBalanceException(this.message);

  @override
  String toString() => message;
}

void withdraw(double balance, double amount) {
  if (amount > balance) {
    throw InsufficientBalanceException('Not enough balance to withdraw');
  }
}
```

This makes the failure type more meaningful than a generic exception.

## Why This Is Useful

Custom exceptions help you:

- describe domain-specific failures
- handle different problems differently
- make error handling easier to understand

## Real-World Example

```dart
class InvalidEmailException implements Exception {
  final String message;

  InvalidEmailException(this.message);

  @override
  String toString() => message;
}

void validateEmail(String email) {
  if (!email.contains('@')) {
    throw InvalidEmailException('Email is invalid');
  }
}
```

This makes it clear what kind of problem occurred.

## Senior Trick: Use Custom Exceptions For Meaning, Not Vanity

Do not create custom exceptions just because you can.

Create them when callers need to understand or handle a specific failure type.

## Senior Trick: Keep Exception Types Small And Clear

A good custom exception should be easy to recognize and easy to search for.

That helps during debugging and makes service boundaries cleaner.

## Summary

- custom exceptions describe specific failures
- they make code easier to read and handle
- they are useful for domain rules and app-specific errors
- they should be created with purpose, not for everything

## Flutter Connection

Custom exceptions are useful in Flutter for validation, repositories, services, and business rules where a generic error is too vague.
