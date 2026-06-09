# Method Overriding

## Learning Goal

In this lesson, you will learn how a child class can replace inherited behavior with its own version.

## What Is Method Overriding

Method overriding happens when a child class defines a method with the same name as a parent class method.

The child version is used instead.

## Basic Example

```dart
class User {
  void showRole() {
    print('User');
  }
}

class AdminUser extends User {
  @override
  void showRole() {
    print('Admin');
  }
}
```

## Why It Matters

Overriding lets subclasses keep the same interface but provide specialized behavior.

## Real-World Example

```dart
class NotificationService {
  void send() {
    print('Sending generic notification');
  }
}

class EmailNotificationService extends NotificationService {
  @override
  void send() {
    print('Sending email notification');
  }
}
```

## Senior Trick: Use `@override` Always When Overriding

This makes intent explicit and helps the analyzer catch mistakes.

## Summary

- overriding replaces inherited behavior
- it allows specialization in child classes
- `@override` should be used for clarity and safety

## Flutter Connection

Method overriding is common in Flutter framework classes and custom Dart hierarchies where child behavior differs from base behavior.
