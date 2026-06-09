# if

## Learning Goal

In this lesson, you will learn how to run code only when a condition is true.

## What Is `if`

The `if` statement checks a condition.
If the condition is `true`, the code inside the block runs.

## Basic Example

```dart
void main() {
  int age = 20;

  if (age >= 18) {
    print('You are eligible to vote.');
  }
}
```

## Explanation

### `if`

Starts the condition check.

### `(age >= 18)`

This is the condition.
It returns `true` or `false`.

### `{ }`

The block runs only if the condition is true.

## Real-World Example

```dart
void main() {
  bool isLoggedIn = true;

  if (isLoggedIn) {
    print('Welcome back!');
  }
}
```

If the user is logged in, the greeting appears.

## Why `if` Matters

Many programs need to do something only in certain situations:

- show a warning
- allow access
- calculate a discount
- send a notification

## Senior Trick: Let Conditions Read Like Plain Meaning

Good:

```dart
bool hasPermission = true;

if (hasPermission) {
  print('Access granted');
}
```

Less clear:

```dart
bool x = true;

if (x) {
  print('Access granted');
}
```

Strong variable names make conditions easier to understand.

## Example With Business Logic

```dart
void main() {
  double orderTotal = 2500;

  if (orderTotal >= 2000) {
    print('Free shipping unlocked');
  }
}
```

This kind of logic appears often in e-commerce apps.

## Common Beginner Mistakes

### Using assignment instead of comparison

Wrong idea:

```dart
// This is not the right way to compare values.
```

Remember:

- `=` assigns
- `==` compares

### Making conditions too long

If the condition gets crowded, break it up:

```dart
bool qualifiesForDiscount = orderTotal >= 2000;

if (qualifiesForDiscount) {
  print('Discount applied');
}
```

## Summary

- `if` runs code only when a condition is true
- it is used for one-way decisions
- readable condition names improve clarity
- simple `if` statements are a core tool in real apps

## Flutter Connection

In Flutter, `if` is often used to:

- show warnings
- display badges
- render content only when data exists
- trigger small conditional UI behavior

It may look basic, but it is everywhere.
