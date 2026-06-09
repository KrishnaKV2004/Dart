# Bitwise Operators

## Learning Goal

In this lesson, you will get an introduction to bitwise operators in Dart and understand when they matter.

## What Are Bitwise Operators

Bitwise operators work at the binary level on integers.

Common bitwise operators:

- `&` bitwise AND
- `|` bitwise OR
- `^` bitwise XOR
- `~` bitwise NOT
- `<<` left shift
- `>>` right shift

## Important Note

For most beginner Dart and Flutter development, bitwise operators are not used daily.

They become more relevant in:

- low-level optimization
- flags and masks
- system-style logic
- some performance-sensitive tasks

## Basic Example

```dart
void main() {
  int a = 5; // 0101
  int b = 3; // 0011

  print(a & b);
  print(a | b);
  print(a ^ b);
}
```

## Why This Is Advanced

These operators act on bits, not on the human meaning of the numbers.

So they are less common in beginner business logic than arithmetic or relational operators.

## Practical Advice

If you are new to Dart:

- know that bitwise operators exist
- understand that they work on integers
- do not force them into normal app code

## Senior Trick: Do Not Use Bitwise Logic When Readable Business Logic Is Better

In ordinary app development, readability usually matters more than low-level cleverness.

## Summary

- bitwise operators work on binary representations of integers
- they are useful in specialized cases
- they are not a core daily tool for most app code
- it is enough for now to recognize them and know their purpose

## Flutter Connection

Most Flutter developers rarely use bitwise operators in regular UI work, but knowing they exist helps you read broader Dart code with more confidence.
