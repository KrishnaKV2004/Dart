# Setters

## Learning Goal

In this lesson, you will learn how setters let you control how values are updated in a class.

## What Is A Setter

A setter is a special method used when assigning a value like a property.

It allows logic to run during assignment.

## Basic Example

```dart
class Temperature {
  double _celsius = 0;

  set celsius(double value) {
    if (value >= -273.15) {
      _celsius = value;
    }
  }

  double get celsius => _celsius;
}
```

## Why Setters Matter

Setters are useful when assignments should be validated or controlled.

## Real-World Example

```dart
class UserProfile {
  String _email = '';

  set email(String value) {
    if (value.contains('@')) {
      _email = value;
    }
  }

  String get email => _email;
}
```

## Senior Trick: Use Setters For Guardrails, Not Hidden Surprises

Setters should usually protect or validate data.
They should not perform unexpected heavy behavior.

## Summary

- setters control how values are assigned
- they are useful for validation and rules
- they help protect class state

## Flutter Connection

Setters can be useful in stateful logic and model classes where data updates should be validated before being accepted.
