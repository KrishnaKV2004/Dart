# Default Parameters

## Learning Goal

In this lesson, you will learn how default parameter values make functions easier to use.

## What Are Default Parameters

Default parameters provide a value automatically when the caller does not pass one.

## Basic Example

```dart
void greetUser(String name, {String greeting = 'Hello'}) {
  print('$greeting, $name');
}

void main() {
  greetUser('Maya');
  greetUser('Maya', greeting: 'Welcome');
}
```

## Why They Matter

Default values help functions stay convenient without forcing callers to provide the same common values every time.

## Real-World Example

```dart
void showToast({
  required String message,
  String type = 'info',
}) {
  print('[$type] $message');
}

void main() {
  showToast(message: 'Profile updated');
  showToast(message: 'Payment failed', type: 'error');
}
```

## Senior Trick: Use Defaults For Common Cases, Not Hidden Surprises

Default values should feel natural and predictable.

Good defaults:

- common
- safe
- easy to understand

Bad defaults are values that cause surprising behavior when the caller forgets to specify them.

## Summary

- default parameters provide automatic fallback values
- they reduce repetitive calling code
- choose defaults that are predictable and sensible

## Flutter Connection

Default parameters are very useful in Flutter helpers and reusable widgets where some configuration is common but still customizable.
