# Mixins

## Learning Goal

In this lesson, you will learn how mixins let classes reuse behavior without using inheritance in the usual way.

## What Is A Mixin

A mixin is a way to share methods and behavior across multiple classes.

It is useful when different classes need the same capability.

## Basic Example

```dart
mixin LoggerMixin {
  void log(String message) {
    print('Log: $message');
  }
}

class PaymentService with LoggerMixin {}

void main() {
  PaymentService service = PaymentService();
  service.log('Payment started');
}
```

## Why Mixins Matter

Mixins help reuse behavior without forcing an "is a" inheritance relationship.

## Real-World Example

```dart
mixin TimestampMixin {
  void showTimestamp() {
    print(DateTime.now());
  }
}

class OrderService with TimestampMixin {}
class UserService with TimestampMixin {}
```

Both classes reuse the same behavior.

## Senior Trick: Use Mixins For Shared Capability, Not Identity

If multiple classes need the same helper behavior, a mixin may fit better than inheritance.

## Summary

- mixins share reusable behavior
- they are useful when many classes need the same capability
- they are a flexible alternative to inheritance for behavior reuse

## Flutter Connection

Mixins are common in Flutter and Dart for shared behavior, lifecycle helpers, and reusable logic across classes.
