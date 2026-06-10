# Type Inference

## Learning Goal

In this lesson, you will learn what type inference is, how Dart uses it, and how to balance convenience with clarity like an experienced developer.

## What Is Type Inference

Type inference means Dart can figure out a variable's type from the value assigned to it.

Example:

```dart
void main() {
  var name = 'Ritika';
  var price = 499.99;
  var isAvailable = true;

  print(name);
  print(price);
  print(isAvailable);
}
```

Dart infers:

- `name` as `String`
- `price` as `double`
- `isAvailable` as `bool`

## Why Type Inference Is Useful

It helps reduce repetition while keeping type safety.

That means you can write less code without losing structure.

## Example With `final`

```dart
void main() {
  final userId = 'USR909';
  final total = 850.50;

  print(userId);
  print(total);
}
```

Here, Dart infers:

- `userId` as `String`
- `total` as `double`

## Senior Trick: Inference Is Great When The Right Side Is Obvious

Good:

```dart
final productName = 'Tablet';
final quantity = 2;
final isPremium = false;
```

These are easy to read.

Less clear:

```dart
final data = loadSomething();
```

Without context, the reader may not know what `data` really is.

In those cases, explicit typing may be better:

```dart
final Map<String, dynamic> data = loadSomething();
```

## Type Inference Is Not Weak Typing

Some beginners think inference means Dart becomes loose about types.
That is not true.

Example:

```dart
void main() {
  var score = 100;
  score = 120;
}
```

This is fine because both are integers.

But:

```dart
void main() {
  var score = 100;
  score = 'high';
}
```

This is invalid because `score` was inferred as `int`.

## Real-World Example

```dart
void main() {
  final customerName = 'Rohit';
  final cartItems = 3;
  final totalAmount = 1499.99;
  final hasCoupon = true;

  print('Customer: $customerName');
  print('Items: $cartItems');
  print('Total: $totalAmount');
  print('Coupon applied: $hasCoupon');
}
```

This is concise but still very readable.

## When To Use Explicit Types Instead

Use explicit types when:

- the returned value is not obvious
- the variable is part of public API design
- clarity matters more than brevity
- the type itself communicates important meaning

## Summary

- type inference lets Dart detect types automatically
- it reduces repetition while keeping safety
- use inference when the value type is obvious
- use explicit types when they improve understanding

## Flutter Connection

In Flutter, type inference is common and useful, but the best code still stays readable.
That balance between short code and clear code is a strong professional habit.
