# Encapsulation

## Learning Goal

In this lesson, you will learn what encapsulation means and why it is important for safe class design.

## What Is Encapsulation

Encapsulation means keeping an object's internal details controlled and exposing only what should be used from outside.

In simple terms:

- protect the inside
- expose a clean outside

## Basic Example

```dart
class BankAccount {
  double _balance = 0;

  void deposit(double amount) {
    if (amount > 0) {
      _balance += amount;
    }
  }

  double get balance => _balance;
}
```

## Why This Is Better

Instead of letting outside code set the balance in any way, the class protects the rule:

- only valid deposits change the balance

## Why Encapsulation Matters

It helps:

- protect data
- reduce accidental misuse
- keep rules in one place

## Senior Trick: Put Business Rules Close To The Data They Protect

If a class owns a concept, it should often own the rules around that concept too.

## Summary

- encapsulation protects internal state
- it exposes only safe or intended access
- it keeps rules centralized inside the class

## Flutter Connection

Encapsulation helps keep Flutter models, services, and state logic safer by preventing messy outside access to internal data.
