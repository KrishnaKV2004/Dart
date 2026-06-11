# Destructuring

## Learning Goal

In this lesson, you will learn how destructuring lets you pull values out of records and other structures directly.

## What Is Destructuring

Destructuring is the act of unpacking values from a structured object into separate variables.

It saves you from repeatedly accessing nested fields.

## Basic Example

```dart
void main() {
  final user = (name: 'Asha', age: 21);

  final (:name, :age) = user;

  print(name);
  print(age);
}
```

Expected output:

```text
Asha
21
```

The record values are unpacked into local variables.

## Why This Is Useful

Destructuring makes code:

- shorter
- easier to scan
- less repetitive
- more expressive

## Real-World Example

```dart
void main() {
  final point = (10, 20);

  final (x, y) = point;

  print('x: $x');
  print('y: $y');
}
```

Expected output:

```text
x: 10
y: 20
```

This is a clean way to unpack positional data.

## Senior Trick: Destructure When It Improves Readability

If extracting values makes the code easier to follow, destructuring is a good choice.

If it feels confusing, keep the explicit access instead.

## Senior Trick: Keep Names Meaningful

Destructured variables should still tell the reader what they mean.

Good variable names still matter, even when the syntax is shorter.

## Summary

- destructuring unpacks structured values into variables
- it works well with records
- it can reduce repeated field access
- readability should guide the choice

## Flutter Connection

Destructuring is useful in Flutter when working with helper results, records, and compact state data.
