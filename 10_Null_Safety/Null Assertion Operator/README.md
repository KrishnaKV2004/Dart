# Null Assertion Operator

## Learning Goal

In this lesson, you will learn what the null assertion operator `!` does and why it should be used carefully.

## What Is The Null Assertion Operator

The null assertion operator is `!`.

It tells Dart:

- "Trust me, this value is not null."

## Basic Example

```dart
void main() {
  String? name = 'Rohan';
  print(name!.length);
}
```

This works because `name` really contains a value.

## The Risk

If the value is actually `null`, the program will crash at runtime.

```dart
void main() {
  String? name;
  print(name!.length);
}
```

This is dangerous.

## Senior Trick: `!` Is A Promise, Not A Fix

Many beginners use `!` just to silence errors.
That is a bad habit.

`!` should only be used when you truly know the value cannot be null at that point.

## Safer Alternative

Instead of:

```dart
print(name!.length);
```

Prefer checking first when possible:

```dart
if (name != null) {
  print(name.length);
}
```

## Real-World Example

```dart
void main() {
  String? selectedCity = 'Pune';

  if (selectedCity != null) {
    print('Selected city: ${selectedCity.length}');
  }
}
```

This is safer and more explicit than forcing `!`.

## When `!` Might Be Reasonable

Sometimes you truly know the value is available because:

- validation already happened
- initialization definitely completed
- logic guarantees the value exists

Even then, use it carefully and sparingly.

## Summary

- `!` asserts that a nullable value is not null
- it can be useful in controlled situations
- it is risky if used carelessly
- never use it just to silence compiler warnings

## Flutter Connection

In Flutter, careless `!` usage is a common source of crashes, especially with:

- async data
- form values
- route arguments
- controller initialization

Use it only when the logic genuinely guarantees safety.
