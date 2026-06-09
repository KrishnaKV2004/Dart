# Named Constructors

## Learning Goal

In this lesson, you will learn how named constructors provide multiple clear ways to create an object.

## What Is A Named Constructor

A named constructor is a constructor with a custom name after the class name.

It lets a class offer different initialization paths.

## Basic Example

```dart
class User {
  String name;
  int age;

  User(this.name, this.age);

  User.guest()
      : name = 'Guest',
        age = 0;
}

void main() {
  User guestUser = User.guest();
  print(guestUser.name);
}
```

## Why Named Constructors Matter

Sometimes one class can be created in multiple meaningful ways.

Examples:

- normal user
- guest user
- product from cache
- product from API

## Real-World Example

```dart
class Order {
  String status;

  Order(this.status);

  Order.pending() : status = 'pending';
  Order.completed() : status = 'completed';
}
```

## Senior Trick: Use Named Constructors To Express Intent

Names like:

- `guest`
- `empty`
- `fromJson`
- `pending`

make creation clearer than overloaded or confusing setup code.

## Summary

- named constructors give multiple ways to create an object
- they improve clarity and express intent
- they are especially useful when initialization paths differ

## Flutter Connection

Named constructors are common in Dart and Flutter models, especially for creating objects from different sources or states.
