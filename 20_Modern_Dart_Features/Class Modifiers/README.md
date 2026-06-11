# Class Modifiers

## Learning Goal

In this lesson, you will learn how Dart class modifiers help control how classes can be used and extended.

## What Are Class Modifiers

Class modifiers are keywords that shape how a class behaves in an inheritance hierarchy or API boundary.

They help Dart express intent more clearly.

## Basic Example

```dart
base class Vehicle {
  void start() {
    print('Vehicle started');
  }
}

class Car extends Vehicle {}

void main() {
  final car = Car();
  car.start();
}
```

Expected output:

```text
Vehicle started
```

The base class is designed for controlled inheritance.

## Why This Is Useful

Class modifiers help you communicate:

- whether a class may be extended
- whether it is meant for implementation
- whether it is sealed to a known set
- whether it should stay final

That makes APIs safer and more intentional.

## Real-World Example

```dart
sealed class AuthState {}

final class LoggedOut extends AuthState {}
final class LoggedIn extends AuthState {}

void main() {
  final state = LoggedIn();
  print(state.runtimeType);
}
```

Expected output:

```text
LoggedIn
```

This shows a controlled hierarchy of states.

## Senior Trick: Use Modifiers To Protect Design Intent

If a class is not meant for arbitrary extension, say so explicitly.

That avoids accidental misuse and makes the code easier to reason about.

## Senior Trick: Prefer Clear Boundaries Over Flexible Chaos

Class modifiers are most valuable when they prevent confusion.

They should make the design more obvious, not more magical.

## Summary

- class modifiers control how classes may be used
- they help design safer APIs
- they make hierarchy intent explicit
- they are useful for controlled inheritance and state modeling

## Flutter Connection

Class modifiers are useful in Flutter and Dart architecture for state classes, internal APIs, and controlled inheritance patterns.
