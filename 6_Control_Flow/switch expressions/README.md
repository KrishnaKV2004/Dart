# switch expressions

## Learning Goal

In this lesson, you will learn what switch expressions are and why they are a powerful modern Dart feature.

## What Is A Switch Expression

A switch expression lets you return a value directly based on matching cases.

This is one of the modern improvements in Dart that helps make decision code more compact and expressive.

## Basic Example

```dart
void main() {
  String status = 'success';

  String message = switch (status) {
    'success' => 'Payment completed',
    'pending' => 'Payment is pending',
    'failed' => 'Payment failed',
    _ => 'Unknown status',
  };

  print(message);
}
```

## Why This Is Useful

Instead of writing:

```dart
String message;

if (status == 'success') {
  message = 'Payment completed';
} else if (status == 'pending') {
  message = 'Payment is pending';
} else {
  message = 'Unknown status';
}
```

You can directly produce the value in one structured expression.

## Senior Trick: Use Switch Expressions For Value Selection, Not Big Side Effects

Good use:

```dart
String buttonLabel = switch (userRole) {
  'admin' => 'Manage',
  'editor' => 'Edit',
  _ => 'View',
};
```

Less ideal use would be trying to bury too much unrelated behavior inside a decision that should simply choose a value.

## Real-World Example

```dart
void main() {
  String membership = 'gold';

  double discount = switch (membership) {
    'gold' => 20,
    'silver' => 10,
    'bronze' => 5,
    _ => 0,
  };

  print('Discount: $discount%');
}
```

## Why This Matters

This style becomes very useful when your program needs to select:

- text
- color names
- labels
- percentages
- modes

based on one known state.

## Summary

- switch expressions return values directly
- they are compact and expressive
- they are especially useful for mapping one state to one result
- they help modern Dart code stay readable when used well

## Flutter Connection

In Flutter, switch expressions are useful for:

- selecting text by state
- choosing icons or labels
- mapping app states to UI-friendly values

They fit nicely into modern, declarative UI code.
