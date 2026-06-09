# Objects

## Learning Goal

In this lesson, you will learn what an object is and how objects are created from classes.

## What Is An Object

An object is an instance of a class.

If a class is the blueprint, the object is the actual thing created from it.

## Basic Example

```dart
class User {
  String name = 'Ravi';
}

void main() {
  User user = User();
  print(user.name);
}
```

Here:

- `User` is the class
- `user` is the object

## Why Objects Matter

Objects let you create real usable pieces of data and behavior from a class design.

## Real-World Example

```dart
class Order {
  String productName = 'Headphones';
  int quantity = 2;
}

void main() {
  Order order = Order();

  print(order.productName);
  print(order.quantity);
}
```

## Senior Trick: Objects Represent Real Instances

Try to think in terms of actual app entities:

- one user
- one product
- one order
- one cart

That thinking makes object design more natural.

## Summary

- an object is an instance of a class
- objects hold the actual data and behavior you use
- classes define, objects realize

## Flutter Connection

In Flutter, you constantly create objects:

- model instances from API data
- configuration objects
- service objects

Understanding objects is essential for real app architecture.
