# else if

## Learning Goal

In this lesson, you will learn how to handle multiple conditions using `else if`.

## What Is `else if`

Use `else if` when there are more than two possible paths.

The program checks conditions from top to bottom.
The first matching condition runs.

## Basic Example

```dart
void main() {
  int marks = 78;

  if (marks >= 90) {
    print('Grade A');
  } else if (marks >= 75) {
    print('Grade B');
  } else if (marks >= 50) {
    print('Grade C');
  } else {
    print('Fail');
  }
}
```

## Why Order Matters

Conditions are checked in sequence.

That means the order should go from:

- most specific or highest priority
- down to broader cases

## Real-World Example

```dart
void main() {
  int batteryLevel = 15;

  if (batteryLevel >= 80) {
    print('Battery high');
  } else if (batteryLevel >= 30) {
    print('Battery normal');
  } else if (batteryLevel > 0) {
    print('Battery low');
  } else {
    print('Device is off');
  }
}
```

## Senior Trick: Make Branches Exclusive

Each branch should represent a clear and distinct meaning.

Good:

```dart
if (age < 13) {
  print('Child');
} else if (age < 20) {
  print('Teen');
} else {
  print('Adult');
}
```

This reads as a clean classification.

## Avoid Messy Overlap

If conditions overlap in confusing ways, code becomes harder to trust.

Use clear ranges and order them carefully.

## Example With App Status

```dart
void main() {
  String orderStatus = 'shipped';

  if (orderStatus == 'pending') {
    print('Order received');
  } else if (orderStatus == 'processing') {
    print('Preparing your order');
  } else if (orderStatus == 'shipped') {
    print('Order is on the way');
  } else {
    print('Unknown status');
  }
}
```

## Senior Trick: If A Long `else if` Chain Feels Like Categories, Consider `switch`

When you are checking one variable against many known cases, `switch` is often cleaner.

That is why the next lessons matter.

## Summary

- `else if` handles more than two paths
- conditions are checked from top to bottom
- order matters
- use clear, non-confusing branch meanings

## Flutter Connection

In Flutter, `else if` is useful for:

- status messages
- multi-state UI
- validation outcomes
- permission and account state branching

When screens behave differently for multiple states, this pattern appears often.
