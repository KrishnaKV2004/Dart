# Assignment Operators

## Learning Goal

In this lesson, you will learn how assignment operators store and update values in variables.

## What Are Assignment Operators

Assignment operators put values into variables or update them based on their current value.

Common ones:

- `=`
- `+=`
- `-=`
- `*=`
- `/=`
- `%=`
- `~/=`

## Basic Example

```dart
void main() {
  int score = 10;

  score += 5;
  print(score);

  score -= 3;
  print(score);
}
```

## Output

```text
15
12
```

## Meaning

### `=`

Assigns a value.

```dart
int count = 1;
```

### `+=`

Adds and assigns.

```dart
count += 2;
```

Equivalent to:

```dart
count = count + 2;
```

### `-=`

Subtracts and assigns.

### `*=`

Multiplies and assigns.

### `/=`

Divides and assigns.

## Real-World Example

```dart
void main() {
  double walletBalance = 5000;

  walletBalance -= 1200;
  print('After payment: $walletBalance');

  walletBalance += 300;
  print('After cashback: $walletBalance');
}
```

## Senior Trick: Prefer Explicitness When Logic Gets Busy

This is fine for simple updates:

```dart
score += 10;
```

But if the update has business meaning, name it:

```dart
double cashback = 300;
walletBalance += cashback;
```

That version is easier to maintain.

## Common Mistake: Mutating Too Many Times In One Place

If a variable is updated repeatedly in a long block, it becomes harder to reason about.

A better pattern is:

- keep updates close to their meaning
- give important values names
- avoid hidden side effects

## Summary

- assignment operators store and update values
- compound operators like `+=` and `-=` shorten common patterns
- use them clearly, not excessively
- named values improve maintainability

## Flutter Connection

In Flutter, assignment-style updates happen in:

- counters
- totals
- form state
- quantity selectors
- local calculations before UI rendering

Clear updates help prevent state confusion.
