# Non Nullable Types

## Learning Goal

In this lesson, you will learn what non-nullable types are and why they should often be your default choice.

## What Is A Non-Nullable Type

A non-nullable type cannot hold `null`.

In Dart, types are non-nullable by default.

## Basic Example

```dart
void main() {
  String name = 'Anika';
  print(name);
}
```

This means `name` must always contain a real `String`.

## What Is Not Allowed

```dart
void main() {
  String name = null;
}
```

This is invalid because `String` is non-nullable here.

## Why Non-Nullable By Default Is Great

It forces you to be explicit.

That means the code is clearer about which values:

- must always exist
- may be missing

## Real-World Example

```dart
void main() {
  String appName = 'Smart Notes';
  int maxLoginAttempts = 5;
  bool isLoggedIn = false;

  print(appName);
  print(maxLoginAttempts);
  print(isLoggedIn);
}
```

These are values the program expects to exist.

## Senior Trick: Prefer Non-Nullable Until Reality Demands Otherwise

This is a very healthy default rule:

- start with non-nullable
- make it nullable only if the business case is genuinely optional

That keeps your code safer and easier to reason about.

## Summary

- non-nullable types cannot store `null`
- types in Dart are non-nullable by default
- this helps make code safer and clearer
- non-nullable should often be your first choice

## Flutter Connection

In Flutter, non-nullable fields and variables often lead to more stable widget code because the UI can rely on those values being present.
