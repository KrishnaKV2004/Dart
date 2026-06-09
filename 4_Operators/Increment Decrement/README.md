# Increment Decrement

## Learning Goal

In this lesson, you will learn how increment and decrement operators work and how to use them safely.

## What Are Increment And Decrement Operators

These operators change a numeric variable by one:

- `++` increment
- `--` decrement

## Basic Example

```dart
void main() {
  int count = 5;

  count++;
  print(count);

  count--;
  print(count);
}
```

## Output

```text
6
5
```

## Prefix And Postfix

There are two forms:

- prefix: `++count`
- postfix: `count++`

## Example

```dart
void main() {
  int a = 5;
  int b = a++;

  print(a);
  print(b);
}
```

Output:

```text
6
5
```

Why:

- `a++` returns the old value first
- then increments `a`

Now prefix:

```dart
void main() {
  int a = 5;
  int b = ++a;

  print(a);
  print(b);
}
```

Output:

```text
6
6
```

Why:

- `++a` increments first
- then returns the new value

## Senior Trick: Avoid Clever Prefix/Postfix Expressions

Although prefix and postfix are valid, many strong developers avoid burying them inside larger expressions because they are easy to misread.

Less clear:

```dart
int result = score++ + 5;
```

Clearer:

```dart
score++;
int result = score + 5;
```

The second version is easier to review and debug.

## Real-World Example

```dart
void main() {
  int cartItemCount = 1;

  cartItemCount++;
  print('Items in cart: $cartItemCount');

  cartItemCount--;
  print('Items in cart: $cartItemCount');
}
```

## Summary

- `++` adds one
- `--` subtracts one
- prefix and postfix behave differently
- simple standalone usage is usually clearer than clever expressions

## Flutter Connection

Increment and decrement are common in Flutter for:

- counters
- steppers
- quantity buttons
- index movement

Clarity matters a lot when UI state changes are involved.
