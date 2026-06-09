# Extension Methods

## Learning Goal

In this lesson, you will learn how extension methods add useful behavior to existing types without changing their original source code.

## What Is An Extension Method

An extension method lets you add new methods or getters to an existing type.

## Basic Example

```dart
extension StringFormatting on String {
  String toGreeting() {
    return 'Hello, $this';
  }
}

void main() {
  print('Asha'.toGreeting());
}
```

## Why Extension Methods Matter

They are useful when you want cleaner APIs for repeated helper logic.

Instead of:

```dart
String formatUserName(String value) {
  return 'User: $value';
}
```

you may prefer behavior that reads naturally on the type itself.

## Real-World Example

```dart
extension PriceFormatting on double {
  String toPriceLabel() {
    return 'Rs. $this';
  }
}

void main() {
  double price = 1499.0;
  print(price.toPriceLabel());
}
```

## Senior Trick: Use Extension Methods For Domain Helpers, Not Random Utility Dumping

Good extensions feel like natural capabilities of the type.

Examples:

- formatting
- validation helpers
- lightweight conversions

## Summary

- extension methods add behavior to existing types
- they can make repeated helper logic more readable
- they should feel natural and focused

## Flutter Connection

Extension methods are very useful in Flutter for formatting, validation, UI-friendly conversions, and small developer-quality improvements across the codebase.
