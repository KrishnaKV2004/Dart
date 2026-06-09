# final

## Learning Goal

In this lesson, you will learn what `final` means, when to use it, and why experienced Dart and Flutter developers prefer it often.

## What Is `final`

`final` means a variable can be assigned only once.

After a value is set, it cannot be changed.

## Basic Example

```dart
void main() {
  final String appName = 'Budget Buddy';

  print(appName);
}
```

This is valid.

But this is not:

```dart
void main() {
  final String appName = 'Budget Buddy';
  appName = 'Expense Pro';
}
```

## Why Use `final`

Use `final` when a value is known once during execution and should not change after that.

Examples:

- logged-in user ID
- API base URL loaded for the session
- created object references
- function results that should stay fixed

## Real-World Example

```dart
void main() {
  final String userId = 'USR1024';
  final double accountBalance = 4500.75;

  print('User ID: $userId');
  print('Balance: $accountBalance');
}
```

These values are read, but not meant to be reassigned.

## Senior Trick: Prefer `final` By Default

Many good Dart developers follow this mindset:

- if a variable does not need to change, make it `final`

Why:

- it prevents accidental reassignment
- it communicates intent clearly
- it makes code safer and easier to reason about

## Example: Safer Local Code

```dart
void main() {
  final double price = 999.0;
  final double discount = 100.0;
  final double finalPrice = price - discount;

  print(finalPrice);
}
```

This tells the reader that these values are fixed within this logic.

## `final` With Objects

This is important:

`final` protects reassignment of the variable, not necessarily mutation inside the object.

```dart
void main() {
  final List<String> items = ['Book', 'Pen'];
  items.add('Notebook');

  print(items);
}
```

This is allowed because the variable `items` still points to the same list.

But this is not allowed:

```dart
void main() {
  final List<String> items = ['Book', 'Pen'];
  items = ['Bag'];
}
```

## Why This Matters

This distinction becomes important later in Flutter when dealing with:

- model objects
- widget fields
- collections in state

## `final` In Functions

```dart
double calculateTotal(double price, double tax) {
  final double total = price + tax;
  return total;
}
```

This is often cleaner than using a mutable variable unless mutation is truly needed.

## Common Beginner Mistake

Some learners use plain variables everywhere even when values never change.

That makes code less expressive.

Compare:

```dart
double taxRate = 0.18;
```

Better:

```dart
final double taxRate = 0.18;
```

The second version communicates stability.

## Senior Trick: `final` Makes Refactoring Safer

When code grows, accidental reassignment can introduce subtle bugs.

Using `final` early helps catch those mistakes faster.

## Summary

- `final` means assign once
- use it when a variable should not be reassigned
- it improves safety, clarity, and maintainability
- it is one of the best default choices in Dart

## Flutter Connection

You will see `final` constantly in Flutter for:

- widget constructor fields
- model properties
- local computed values
- service references

Getting comfortable with `final` now is a very strong long-term habit.
