# Printing Output

## Learning Goal

In this lesson, you will learn how to display output in Dart, why output is important for both users and developers, and how to keep printed messages useful and readable.

## What Is Output

Output is the information a program shows after doing some work.

In console-based Dart programs, output is usually displayed using `print()`.

## Basic Example

```dart
void main() {
  print('Hello, Dart!');
}
```

## Explanation

### `print()`

`print()` sends text or values to the console.

This is the most common way to:

- show messages
- display results
- debug simple programs

## Printing More Than One Line

```dart
void main() {
  print('Welcome to the app');
  print('Loading your dashboard...');
  print('Done');
}
```

## Printing Variables

```dart
void main() {
  String name = 'Aisha';
  int points = 120;

  print(name);
  print(points);
}
```

## Printing Labels With Values

```dart
void main() {
  String productName = 'Keyboard';
  double price = 1499.0;

  print('Product: $productName');
  print('Price: $price');
}
```

This is much more readable than printing raw values without context.

## Senior Trick: Print For Humans, Not Just For The Machine

Weak:

```dart
print(price);
```

Better:

```dart
print('Current price: $price');
```

If output is meant for a person, give it context.

## Real-World Example

```dart
void main() {
  String userName = 'Riya';
  bool isPremium = true;

  print('User: $userName');
  print('Premium member: $isPremium');
}
```

This is similar to the kind of information you might show in a profile or admin summary.

## Output For Debugging

Printing is also useful while learning and debugging.

```dart
void main() {
  double itemPrice = 500;
  int quantity = 3;
  double total = itemPrice * quantity;

  print('itemPrice = $itemPrice');
  print('quantity = $quantity');
  print('total = $total');
}
```

## Why This Helps

If something looks wrong, printing intermediate values can help you find the issue quickly.

This is one of the simplest and most reliable debugging habits.

## Senior Trick: Use Temporary Prints To Understand Logic, Then Clean Up

While learning or debugging, extra prints are helpful.
But in finished code, avoid leaving noisy output unless it serves a real purpose.

## Common Beginner Mistakes

### Printing without labels

```dart
print(1200);
print(true);
```

This works, but it is harder to understand than:

```dart
print('Balance: 1200');
print('Active: true');
```

### Trying to print undeclared variables

```dart
void main() {
  print(userName);
}
```

This fails because `userName` was never declared.

## Summary

- `print()` displays output in the console
- output should be readable and meaningful
- labels make output easier to understand
- printing is also a useful debugging tool

## Flutter Connection

In Flutter, user-facing output usually appears in widgets instead of the console, but the same principle stays true:

- show clear information
- give values context
- make the result easy to understand
