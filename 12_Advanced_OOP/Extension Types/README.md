# Extension Types

## Learning Goal

In this lesson, you will get a beginner-friendly introduction to extension types and why they exist in modern Dart.

## What Is An Extension Type

An extension type lets you wrap another representation type in a more domain-specific API.

This gives you stronger modeling without always needing a full traditional class design.

## Basic Idea

You may have a raw value like a `String`, but semantically it represents something more meaningful, such as:

- email address
- user ID
- product code

An extension type helps you model that meaning more clearly.

## Basic Example

```dart
extension type UserId(String value) {
  String get display => 'User ID: $value';
}

void main() {
  UserId id = UserId('USR-1001');
  print(id.display);
}
```

## Why This Matters

It helps communicate domain meaning better than raw primitive values alone.

## Senior Trick: Stronger Domain Modeling Often Prevents Mistakes

Using a specific semantic type can make code more expressive than passing plain strings everywhere.

## Summary

- extension types wrap another representation with clearer meaning
- they help model domain concepts more explicitly
- they are useful for modern, expressive API design

## Flutter Connection

Extension types are more advanced and not required for most beginner Flutter apps, but they are helpful to understand as Dart evolves toward stronger domain modeling patterns.
