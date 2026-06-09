# Inheritance

## Learning Goal

In this lesson, you will learn how inheritance lets one class reuse and extend another class.

## What Is Inheritance

Inheritance means a class can build on another class.

The child class gets the parent class's fields and methods, and can add more of its own.

## Basic Example

```dart
class Animal {
  void eat() {
    print('Eating');
  }
}

class Dog extends Animal {
  void bark() {
    print('Barking');
  }
}

void main() {
  Dog dog = Dog();
  dog.eat();
  dog.bark();
}
```

## Why Inheritance Matters

It helps reuse shared behavior while allowing specialization.

## Real-World Example

```dart
class User {
  String name;

  User(this.name);

  void showRole() {
    print('Basic user');
  }
}

class AdminUser extends User {
  AdminUser(super.name);

  void deletePost() {
    print('Post deleted');
  }
}
```

## Senior Trick: Inheritance Is For "Is A" Relationships

Good examples:

- `AdminUser` is a `User`
- `Dog` is an `Animal`

If the relationship is not naturally "is a", inheritance may not be the best fit.

## Summary

- inheritance lets one class reuse another
- child classes can extend parent behavior
- use inheritance when the relationship is natural and meaningful

## Flutter Connection

Inheritance appears in Flutter and Dart in framework classes and custom abstractions, but it should be used thoughtfully rather than by default.
