# Polymorphism

## Learning Goal

In this lesson, you will learn what polymorphism means and why it makes OOP code more flexible.

## What Is Polymorphism

Polymorphism means different classes can be used through a shared type, while each provides its own behavior.

## Basic Example

```dart
class PaymentMethod {
  void pay() {
    print('Generic payment');
  }
}

class CardPayment extends PaymentMethod {
  @override
  void pay() {
    print('Paid by card');
  }
}

class CashPayment extends PaymentMethod {
  @override
  void pay() {
    print('Paid by cash');
  }
}

void main() {
  List<PaymentMethod> methods = [CardPayment(), CashPayment()];

  for (PaymentMethod method in methods) {
    method.pay();
  }
}
```

## Why It Matters

Polymorphism lets code work with general types while still getting specific behavior.

This improves flexibility and extensibility.

## Senior Trick: Program To Shared Contracts

When possible, write code that depends on a shared type or capability instead of a single concrete class.

That makes future changes easier.

## Summary

- polymorphism lets one interface support many implementations
- shared types plus specialized behavior make code flexible
- it is one of the most powerful ideas in OOP

## Flutter Connection

Polymorphism is useful in Flutter for services, state abstractions, data handlers, and any place where multiple implementations should fit one API.
