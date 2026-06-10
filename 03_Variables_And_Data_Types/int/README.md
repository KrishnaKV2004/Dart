# int

## Learning Goal

In this lesson, you will learn what `int` is, when to use it, and how it shows up in practical app logic.

## What Is `int`

`int` is the data type for whole numbers.

Examples:

- `0`
- `7`
- `42`
- `-15`

## Basic Example

```dart
void main() {
  int age = 25;
  int cartItems = 3;

  print(age);
  print(cartItems);
}
```

## When To Use `int`

Use `int` for values that should not contain decimals.

Common examples:

- age
- quantity
- score
- item count
- index position

## Real-World Example

```dart
void main() {
  int unreadMessages = 12;
  int rewardPoints = 250;

  print('Unread messages: $unreadMessages');
  print('Reward points: $rewardPoints');
}
```

## `int` Supports Arithmetic

```dart
void main() {
  int apples = 5;
  int oranges = 3;
  int totalFruits = apples + oranges;

  print(totalFruits);
}
```

## Output

```text
8
```

## Why `int` Matters In Apps

Many app features depend on whole-number logic:

- cart quantity
- notification count
- page number
- number of likes
- selected tab index

## Common Mistake: Using `int` For Decimal Values

```dart
void main() {
  int price = 99.99;
}
```

This is wrong because `99.99` is not a whole number.
Use `double` instead.

## Senior Trick: Choose Types By Business Meaning

Ask:

- Is this a count?
- Is this a position?
- Is this a quantity with no fractions?

If yes, `int` is probably right.

Example:

```dart
int totalOrders = 18;
int selectedIndex = 2;
```

These model meaning clearly.

## Example With Conditional Logic

```dart
void main() {
  int stock = 7;

  if (stock > 0) {
    print('Item available');
  } else {
    print('Out of stock');
  }
}
```

## Summary

- `int` stores whole numbers
- use it for counts, indexes, and discrete values
- do not use it for decimal values
- choosing `int` correctly improves clarity and safety

## Flutter Connection

In Flutter, `int` is commonly used for:

- item counts
- selected indexes
- badge numbers
- pagination
- loop counters

It may seem simple, but it is everywhere in real UI logic.
