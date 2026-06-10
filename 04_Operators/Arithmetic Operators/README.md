# Arithmetic Operators

## Learning Goal

In this lesson, you will learn how Dart performs basic mathematical operations and how those operations appear in real app logic.

## What Are Arithmetic Operators

Arithmetic operators are used for calculations.

Main arithmetic operators in Dart:

- `+` addition
- `-` subtraction
- `*` multiplication
- `/` division
- `%` remainder
- `~/` integer division

## Basic Example

```dart
void main() {
  int a = 10;
  int b = 3;

  print(a + b);
  print(a - b);
  print(a * b);
  print(a / b);
  print(a % b);
  print(a ~/ b);
}
```

## Output

```text
13
7
30
3.3333333333333335
1
3
```

## Operator Meanings

### `+`

Adds values.

```dart
int total = 5 + 2;
```

### `-`

Subtracts values.

```dart
int remaining = 10 - 4;
```

### `*`

Multiplies values.

```dart
int totalCost = 3 * 500;
```

### `/`

Divides and returns a `double`.

```dart
double result = 10 / 4;
```

### `%`

Returns the remainder.

```dart
int remainder = 10 % 3;
```

### `~/`

Integer division, discarding the decimal part.

```dart
int pages = 10 ~/ 3;
```

## Real-World Example

```dart
void main() {
  double productPrice = 1500;
  int quantity = 2;
  double discount = 200;

  double subtotal = productPrice * quantity;
  double finalAmount = subtotal - discount;

  print('Subtotal: $subtotal');
  print('Final amount: $finalAmount');
}
```

This is the kind of calculation logic that appears constantly in shopping and billing apps.

## Senior Trick: Name Intermediate Calculations

Less clear:

```dart
print((1500 * 2) - 200);
```

Better:

```dart
double subtotal = 1500 * 2;
double finalAmount = subtotal - 200;

print(finalAmount);
```

This is easier to debug, review, and change later.

## Using `%` In Real Logic

The remainder operator is often used for patterns.

Example:

```dart
void main() {
  int number = 8;

  if (number % 2 == 0) {
    print('Even number');
  } else {
    print('Odd number');
  }
}
```

## Common Mistake: Forgetting `/` Returns `double`

```dart
void main() {
  var result = 10 / 2;
  print(result);
}
```

This prints `5.0`, not `5`.

If you specifically want an integer result, consider `~/` when appropriate.

## Summary

- arithmetic operators perform calculations
- `/` returns a `double`
- `%` gives remainder
- `~/` performs integer division
- named intermediate values improve readability

## Flutter Connection

In Flutter, arithmetic operators are used for:

- totals and discounts
- counters
- percentages
- ratings
- layout and sizing calculations

Clean math logic now helps prevent UI bugs later.
