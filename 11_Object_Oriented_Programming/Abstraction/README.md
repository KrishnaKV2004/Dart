# Abstraction

## Learning Goal

In this lesson, you will learn what abstraction means and why it helps keep systems simpler and cleaner.

## What Is Abstraction

Abstraction means focusing on what something does instead of exposing every detail of how it works.

It helps reduce complexity.

## Basic Example

```dart
abstract class PaymentService {
  void pay(double amount);
}
```

This tells other parts of the program:

- a payment service must support `pay`

without forcing them to care about the internal payment logic.

## Why It Matters

Abstraction helps:

- define clear contracts
- hide details
- keep code flexible

## Real-World Example

```dart
abstract class AuthService {
  void login(String email, String password);
}
```

Different implementations might log in through:

- local mock logic
- Firebase
- a REST API

but the rest of the app can depend on the shared idea of an auth service.

## Senior Trick: Abstract Important Capabilities, Not Everything

Good abstraction simplifies a system.
Too much abstraction too early can make code harder to follow.

## Summary

- abstraction focuses on capability, not internal detail
- it helps define clean contracts
- it is useful for building flexible systems

## Flutter Connection

Abstraction is very valuable in Flutter architecture for services, repositories, and other reusable app capabilities.
