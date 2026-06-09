# Abstract Classes

## Learning Goal

In this lesson, you will learn what abstract classes are and why they are useful for defining shared contracts and behavior.

## What Is An Abstract Class

An abstract class is a class that cannot be instantiated directly.

It is used as a base design for other classes.

## Basic Example

```dart
abstract class PaymentMethod {
  void pay(double amount);
}

class CardPayment extends PaymentMethod {
  @override
  void pay(double amount) {
    print('Paid $amount by card');
  }
}
```

## Why Abstract Classes Matter

They are useful when you want to define:

- a common contract
- optional shared behavior
- a parent design that should not exist on its own

## Real-World Example

```dart
abstract class NotificationService {
  void send(String message);
}

class EmailNotificationService extends NotificationService {
  @override
  void send(String message) {
    print('Email: $message');
  }
}

class SmsNotificationService extends NotificationService {
  @override
  void send(String message) {
    print('SMS: $message');
  }
}
```

## Senior Trick: Use Abstract Classes When The Base Type Has Meaning But Should Not Exist Alone

For example:

- `PaymentMethod`
- `NotificationService`
- `AuthProvider`

These are real concepts, but usually the app needs a concrete implementation, not a bare generic instance.

## Summary

- abstract classes cannot be created directly
- they define shared contracts and optional shared behavior
- they are useful for strong architecture design

## Flutter Connection

Abstract classes are very useful in Flutter architecture for repositories, services, and shared state capabilities.
