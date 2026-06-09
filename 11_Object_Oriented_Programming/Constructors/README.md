# Constructors

## Learning Goal

In this lesson, you will learn what constructors are and how they help initialize objects cleanly.

## What Is A Constructor

A constructor is a special method used when an object is created.

It helps set up the initial state of the object.

## Basic Example

```dart
class User {
  String name;
  int age;

  User(this.name, this.age);
}

void main() {
  User user = User('Aditi', 25);
  print(user.name);
  print(user.age);
}
```

## Why Constructors Matter

Without constructors, you often create incomplete objects first and fill them later.

Constructors make object creation cleaner and safer.

## Real-World Example

```dart
class Product {
  String name;
  double price;

  Product(this.name, this.price);
}

void main() {
  Product product = Product('Keyboard', 1499.0);
  print(product.name);
  print(product.price);
}
```

## Senior Trick: Prefer Fully Initialized Objects

It is often better for an object to be valid immediately after creation.

That usually leads to fewer bugs and clearer code.

## Summary

- constructors run when objects are created
- they initialize object state
- they help make objects valid from the beginning

## Flutter Connection

Constructors are everywhere in Flutter, especially in widgets and model classes.
Getting comfortable with them now is extremely valuable.
