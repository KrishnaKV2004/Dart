# Return Values

## Learning Goal

In this lesson, you will learn how functions can send results back using return values.

## What Is A Return Value

A return value is the result a function gives back after doing its work.

## Basic Example

```dart
int add(int a, int b) {
  return a + b;
}

void main() {
  int result = add(5, 3);
  print(result);
}
```

## Why Returning Is Better Than Printing Everything

This works:

```dart
void showTotal(int a, int b) {
  print(a + b);
}
```

But it is less reusable than:

```dart
int calculateTotal(int a, int b) {
  return a + b;
}
```

The returned value can now be:

- printed
- stored
- compared
- passed into another function

## Real-World Example

```dart
double calculateDiscountedPrice(double price, double discount) {
  return price - discount;
}

void main() {
  double finalPrice = calculateDiscountedPrice(1500, 200);
  print('Final price: $finalPrice');
}
```

## Senior Trick: Prefer Returning Data Over Printing Inside Logic Functions

Functions that return data are usually easier to:

- test
- reuse
- compose

For example, this is flexible:

```dart
bool isEligibleForFreeShipping(double orderTotal) {
  return orderTotal >= 2000;
}
```

Then the caller decides what to do with the result.

## Summary

- `return` sends a value back from a function
- returned values are more reusable than direct printing
- many of the best functions compute and return results

## Flutter Connection

In Flutter, returning values is very common for:

- validation helpers
- calculated UI text
- business rule checks
- transformed data

This is a key skill for clean app architecture.
