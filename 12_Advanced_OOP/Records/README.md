# Records

## Learning Goal

In this lesson, you will learn what records are and when they are useful for lightweight grouped data.

## What Is A Record

A record is a lightweight way to group multiple values together without creating a full class.

## Basic Example

```dart
void main() {
  var userInfo = ('Asha', 24);

  print(userInfo.$1);
  print(userInfo.$2);
}
```

## Named Record Fields

```dart
void main() {
  var order = (product: 'Laptop', price: 55000.0);

  print(order.product);
  print(order.price);
}
```

## Why Records Matter

Records are useful when you want to return or pass a few related values together, but a full class would be unnecessary.

## Real-World Example

```dart
(String, double) getProductSummary() {
  return ('Keyboard', 1499.0);
}

void main() {
  var summary = getProductSummary();
  print(summary.$1);
  print(summary.$2);
}
```

## Senior Trick: Use Records For Small Structured Data, Not Long-Term Domain Models

Records are great for:

- temporary grouped results
- helper return values
- small structured state

If the concept becomes important in the domain, a real class is often better.

## Summary

- records group values together without a full class
- they are useful for lightweight structured data
- they are best for small, focused use cases

## Flutter Connection

Records are useful in Flutter-related Dart code for helper returns, structured temporary values, and modern pattern-matching-friendly state handling.
