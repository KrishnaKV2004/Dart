# this Keyword

## Learning Goal

In this lesson, you will learn what `this` means and how it helps refer to the current object.

## What Is `this`

`this` refers to the current instance of the class.

It is often used when constructor parameters have the same names as class fields.

## Basic Example

```dart
class User {
  String name;
  int age;

  User(this.name, this.age);
}
```

This short syntax is a common and clean use of `this`.

## Longer Form

```dart
class User {
  String name;
  int age;

  User(String name, int age)
      : this.name = name,
        this.age = age;
}
```

## Why It Matters

`this` helps make it clear that you are assigning values to fields of the current object.

## Real-World Example

```dart
class Product {
  String name;
  double price;

  Product(this.name, this.price);
}
```

## Senior Trick: Prefer The Short Form When It Stays Clear

The shorthand constructor form with `this.field` is one of the cleanest Dart features for model classes.

## Summary

- `this` refers to the current object
- it is often used in constructors
- it helps connect parameters to class fields clearly

## Flutter Connection

You will see `this` all the time in Flutter and Dart model classes, widget constructors, and general OOP code.
