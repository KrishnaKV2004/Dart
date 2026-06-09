# Static Members

## Learning Goal

In this lesson, you will learn what static members are and when they are useful.

## What Is A Static Member

A static member belongs to the class itself, not to individual objects.

That means you access it using the class name.

## Basic Example

```dart
class AppConfig {
  static String appName = 'TaskFlow';
}

void main() {
  print(AppConfig.appName);
}
```

## Static Methods

```dart
class MathHelper {
  static int square(int number) {
    return number * number;
  }
}

void main() {
  print(MathHelper.square(4));
}
```

## Why Static Members Matter

They are useful for:

- constants
- utility logic
- shared configuration

## Senior Trick: Use Static For Class-Level Meaning, Not Random Convenience

If behavior does not depend on object state, static may be a good fit.
But do not put unrelated global logic everywhere just because static exists.

## Summary

- static members belong to the class, not the instance
- they are useful for shared configuration and utilities
- use them intentionally and sparingly

## Flutter Connection

Static members are common in Flutter for helpers, constants, route names, and configuration-style values.
