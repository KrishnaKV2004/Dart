# Classes

## Learning Goal

In this lesson, you will learn what a class is and why classes are the foundation of object-oriented programming in Dart.

## What Is A Class

A class is a blueprint for creating objects.

It defines:

- what data something has
- what behavior something can perform

## Basic Example

```dart
class User {
  String name = 'Asha';
  int age = 24;

  void showProfile() {
    print('Name: $name');
    print('Age: $age');
  }
}

void main() {
  User user = User();
  user.showProfile();
}
```

## Why Classes Matter

Classes help you group related data and behavior together.

Instead of scattering values and functions everywhere, you can model one concept in one place.

## Real-World Example

```dart
class Product {
  String name = 'Laptop';
  double price = 55000;

  void showDetails() {
    print('Product: $name');
    print('Price: $price');
  }
}
```

This is much closer to how app data is really organized.

## Senior Trick: Design Classes Around Real Concepts

Good classes often map to real domain concepts:

- `User`
- `Order`
- `Cart`
- `Message`

That makes the code easier to understand and discuss.

## Summary

- a class is a blueprint
- it groups data and behavior
- classes are the core building block of OOP

## Flutter Connection

In Flutter, classes are everywhere:

- model classes
- service classes
- widget classes

Learning classes well is one of the biggest steps toward professional app development.
