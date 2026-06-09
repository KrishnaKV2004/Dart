# Formatting Output

## Learning Goal

In this lesson, you will learn how to make output easier to read and more professional.

## Why Formatting Matters

Correct output is not always enough.
Good output should also be:

- readable
- structured
- friendly
- easy to scan

This matters for:

- users
- debugging
- reports
- command-line tools

## Basic Example

```dart
void main() {
  String name = 'Tina';
  double balance = 3200.50;

  print('User: $name');
  print('Balance: $balance');
}
```

This is already better than printing raw values separately.

## Using Separators

```dart
void main() {
  print('=== Account Summary ===');
  print('Name: Tina');
  print('Balance: 3200.50');
  print('=======================');
}
```

Separators help organize console output.

## Multi-Line Output

```dart
void main() {
  String summary = '''
Order Summary
-------------
Product: Headphones
Quantity: 2
Status: Confirmed
''';

  print(summary);
}
```

## Senior Trick: Format Output As If Someone Else Will Read It

Even if you wrote the program yourself, assume future-you or a teammate may read the output later.

That leads to better choices:

- clear labels
- grouped sections
- useful spacing

## Real-World Example

```dart
void main() {
  String customerName = 'Mina';
  int items = 3;
  double total = 2450.75;

  print('=== Invoice ===');
  print('Customer: $customerName');
  print('Items: $items');
  print('Total: $total');
}
```

## Common Mistake: Output Without Structure

Harder to read:

```dart
print('Mina');
print(3);
print(2450.75);
```

Better:

```dart
print('Customer: Mina');
print('Items: 3');
print('Total: 2450.75');
```

## Senior Trick: Keep Display Format Separate From Core Logic

If a value needs calculation, do that first.
Then format it for output.

```dart
void main() {
  double price = 1200;
  double tax = 216;
  double finalAmount = price + tax;

  print('Final amount: $finalAmount');
}
```

This separation keeps code easier to maintain.

## Summary

- formatted output is easier to read and trust
- labels, spacing, and grouping improve clarity
- calculate first, then display cleanly
- readable output is part of professional code quality

## Flutter Connection

In Flutter, formatting output becomes:

- clean UI text
- readable summaries
- friendly labels
- well-presented data on screen

Good display habits start here, even in console programs.
