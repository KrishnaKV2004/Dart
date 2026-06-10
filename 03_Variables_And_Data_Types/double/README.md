# double

## Learning Goal

In this lesson, you will learn what `double` is, when to use it, and why it is important for money, measurements, and UI-related values.

## What Is `double`

`double` is the data type for decimal numbers.

Examples:

- `9.5`
- `1200.0`
- `3.14159`

## Basic Example

```dart
void main() {
  double price = 249.99;
  double rating = 4.8;

  print(price);
  print(rating);
}
```

## When To Use `double`

Use `double` when the value may include fractions or decimals.

Examples:

- price
- rating
- tax
- discount percentage
- height and width values

## Real-World Example

```dart
void main() {
  double productPrice = 799.50;
  double discount = 99.50;
  double finalPrice = productPrice - discount;

  print('Final price: $finalPrice');
}
```

## Why `double` Matters

Real apps often deal with values that are not whole numbers:

- e-commerce prices
- average ratings
- layout dimensions
- animation values

## Common Mistake: Using `double` When `int` Would Be Clearer

```dart
double itemCount = 4.0;
```

This technically works for a numeric value, but it is weaker than:

```dart
int itemCount = 4;
```

If something is a count, `int` usually expresses the business meaning better.

## Senior Trick: Use The Narrowest Honest Type

If a value can be represented more clearly as an `int`, use `int`.
If decimals are natural to the domain, use `double`.

That rule keeps code expressive.

## Example With User Input Thinking

```dart
void main() {
  double temperature = 36.7;

  if (temperature > 37.0) {
    print('Fever detected');
  } else {
    print('Temperature is normal');
  }
}
```

## Summary

- `double` stores decimal numbers
- use it for values like price, rating, percentage, and measurements
- do not use it when a whole-number type is more accurate
- strong type choice improves code meaning

## Flutter Connection

In Flutter, `double` appears very often for:

- dimensions
- padding
- font sizes
- animation values
- ratings and prices

So this type becomes extremely familiar in real app development.
