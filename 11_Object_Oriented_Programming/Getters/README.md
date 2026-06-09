# Getters

## Learning Goal

In this lesson, you will learn how getters provide computed or controlled read access to class data.

## What Is A Getter

A getter is a special way to read a value like a property, while still running logic behind the scenes.

## Basic Example

```dart
class Rectangle {
  double width;
  double height;

  Rectangle(this.width, this.height);

  double get area => width * height;
}

void main() {
  Rectangle rectangle = Rectangle(10, 5);
  print(rectangle.area);
}
```

## Why Getters Matter

Getters are useful when a value:

- should be calculated
- should be exposed read-only
- should feel like a natural property

## Real-World Example

```dart
class CartItem {
  double price;
  int quantity;

  CartItem(this.price, this.quantity);

  double get total => price * quantity;
}
```

## Senior Trick: Use Getters For Derived Values

If a value depends on other fields and should always stay up to date, a getter is often a great choice.

## Summary

- getters provide read access with optional logic
- they are useful for computed values
- they make class APIs cleaner

## Flutter Connection

Getters are very useful in Flutter models and state objects for values like totals, labels, derived status, and validation state.
