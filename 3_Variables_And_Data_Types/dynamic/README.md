# dynamic

## Learning Goal

In this lesson, you will learn what `dynamic` is, when it can be useful, and why experienced developers use it carefully.

## What Is `dynamic`

`dynamic` means Dart will allow a variable to hold values of different types without strong compile-time checking.

## Basic Example

```dart
void main() {
  dynamic value = 'Hello';
  print(value);

  value = 42;
  print(value);

  value = true;
  print(value);
}
```

## Why `dynamic` Exists

Sometimes you do not know the exact type ahead of time.

Examples:

- loosely structured API data
- generic external data
- quick experiments

## The Risk Of `dynamic`

`dynamic` removes safety.

Example:

```dart
void main() {
  dynamic value = 'Hello';
  print(value.length);
}
```

This works.

But if the value changes:

```dart
void main() {
  dynamic value = 10;
  print(value.length);
}
```

This can fail at runtime because integers do not have `length`.

## Senior Trick: Avoid `dynamic` Unless You Truly Need It

Strong developers usually prefer:

- specific types first
- `Object` or structured models where appropriate
- `dynamic` only at the edges of uncertain data

## Better Alternative Example

Instead of:

```dart
dynamic userName = 'Anaya';
```

Prefer:

```dart
String userName = 'Anaya';
```

This gives you type safety and better tooling support.

## Real-World Example Where `dynamic` Appears

```dart
Map<String, dynamic> apiResponse = {
  'name': 'Laptop',
  'price': 55000,
  'inStock': true,
};
```

Here, `dynamic` is common because different keys may hold different value types.

But even then, strong apps often convert that raw data into typed model classes later.

## Why This Matters For Flutter

In Flutter apps, raw API responses may begin as `Map<String, dynamic>`, but good architecture usually moves quickly toward:

- typed models
- safe parsing
- predictable fields

That reduces bugs across the app.

## Summary

- `dynamic` allows flexible typing
- it is useful when data is uncertain
- it reduces compile-time safety
- use it carefully and prefer specific types when possible

## Flutter Connection

You may encounter `dynamic` in JSON parsing and external data handling, but long-term Flutter code is usually much healthier when converted into well-typed classes and fields.
