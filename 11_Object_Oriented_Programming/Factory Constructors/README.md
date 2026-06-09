# Factory Constructors

## Learning Goal

In this lesson, you will learn what factory constructors are and why they are useful for controlled object creation.

## What Is A Factory Constructor

A factory constructor does not have to create a brand-new instance every time.

It can:

- return an existing instance
- decide which subclass or object to return
- perform extra creation logic

## Basic Example

```dart
class User {
  String role;

  User._internal(this.role);

  factory User.guest() {
    return User._internal('guest');
  }
}

void main() {
  User user = User.guest();
  print(user.role);
}
```

## Why Factory Constructors Matter

They are useful when normal constructors are not flexible enough.

## Real-World Example

```dart
class StatusMessage {
  final String text;

  StatusMessage._(this.text);

  factory StatusMessage.fromCode(int code) {
    if (code == 200) {
      return StatusMessage._('Success');
    }

    return StatusMessage._('Unknown');
  }
}
```

## Senior Trick: Use Factory Constructors When Creation Needs Logic

Common examples:

- parsing input
- returning cached instances
- choosing a variant by state

## Summary

- factory constructors can control how objects are created
- they are useful when creation needs logic beyond simple field assignment
- they often improve clarity and flexibility

## Flutter Connection

Factory constructors are very common in Flutter and Dart model classes, especially for parsing, caching, and structured creation patterns.
