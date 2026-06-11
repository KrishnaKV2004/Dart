# Records

## Learning Goal

In this lesson, you will learn how records let you bundle multiple values together without creating a dedicated class.

## What Is A Record

A record is a lightweight data structure that groups values together.

Records can be positional, named, or both.

## Basic Example

```dart
void main() {
  final record = ('Asha', 21);

  print(record.$1);
  print(record.$2);
}
```

Expected output:

```text
Asha
21
```

This is a compact way to group related values.

## Named Record Example

```dart
void main() {
  final user = (name: 'Asha', age: 21);

  print(user.name);
  print(user.age);
}
```

Expected output:

```text
Asha
21
```

Named fields make the record easier to read.

## Why Records Matter

Records are useful when you want to:

- return multiple values from a function
- pass structured temporary data
- avoid creating a small throwaway class

## Real-World Example

```dart
({String name, int age}) loadProfile() {
  return (name: 'Ravi', age: 25);
}

void main() {
  final profile = loadProfile();
  print('Name: ${profile.name}');
  print('Age: ${profile.age}');
}
```

Expected output:

```text
Name: Ravi
Age: 25
```

This is a clean way to return a pair of related values.

## Senior Trick: Use Records For Shape, Not Behavior

Records are best when you only need to carry data around.

If the data needs methods, validation, or business behavior, a class is usually the better choice.

## Senior Trick: Name Fields When The Meaning Matters

Named fields make records much easier to understand than relying on position alone.

That is especially important when there are three or more values.

## Summary

- records group multiple values together
- they can be positional or named
- they are useful for small structured data
- classes are better when behavior belongs with the data

## Flutter Connection

Records can help in Flutter when returning temporary grouped values from helpers, parsing steps, or UI decisions.
