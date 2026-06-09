# String Interpolation

## Learning Goal

In this lesson, you will learn how to combine text and values cleanly using string interpolation.

## What Is String Interpolation

String interpolation means inserting variables or expressions directly inside a string.

This makes output cleaner and easier to read.

## Basic Example

```dart
void main() {
  String name = 'Kunal';
  print('Hello, $name');
}
```

## Expressions Inside Strings

Use `${}` when inserting expressions:

```dart
void main() {
  int quantity = 3;
  double price = 499.0;

  print('Total: ${quantity * price}');
}
```

## Why Interpolation Is Better Than Manual Joining

Less clean:

```dart
print('Hello, ' + name);
```

Better:

```dart
print('Hello, $name');
```

Interpolation is usually more readable and more idiomatic in Dart.

## Real-World Example

```dart
void main() {
  String userName = 'Neeraj';
  int pendingTasks = 5;

  print('User: $userName');
  print('Pending tasks: $pendingTasks');
}
```

## Senior Trick: Use Interpolation To Improve Clarity, Not To Cram Logic

Good:

```dart
double total = 1200 + 300;
print('Total amount: $total');
```

Less good:

```dart
print('Total amount after processing all invoice data and extra logic: ${1200 + 300}');
```

If the expression gets meaningful, compute it first and name it.

## Example With Conditional Thinking

```dart
void main() {
  bool isLoggedIn = true;
  String status = isLoggedIn ? 'Online' : 'Offline';

  print('User status: $status');
}
```

## Common Mistakes

### Forgetting `${}` for expressions

Wrong:

```dart
print('Total: $quantity * $price');
```

This prints text pieces, not the multiplication result.

Correct:

```dart
print('Total: ${quantity * price}');
```

### Making strings too crowded

If a string contains too much logic, move the logic out first.

## Summary

- string interpolation inserts values directly into text
- use `$variable` for simple variables
- use `${expression}` for expressions
- interpolation is cleaner than manual string joining

## Flutter Connection

In Flutter, interpolation is used constantly for:

- labels
- status messages
- counts
- summaries
- dynamic UI text

Clean string building makes apps feel much more polished.
