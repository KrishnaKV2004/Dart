# Higher Order Functions

## Learning Goal

In this lesson, you will learn what higher-order functions are and why they are powerful in Dart.

## What Is A Higher-Order Function

A higher-order function is a function that:

- takes another function as a parameter
- returns a function
- or both

## Basic Example

```dart
void performAction(void Function() action) {
  action();
}

void main() {
  performAction(() {
    print('Action executed');
  });
}
```

## Why This Matters

Higher-order functions make code more flexible.

They let you separate:

- what should happen
- from when or how it should happen

## Real-World Example

```dart
void processPayment(void Function() onSuccess) {
  print('Processing payment...');
  onSuccess();
}

void main() {
  processPayment(() {
    print('Payment successful');
  });
}
```

## Senior Trick: Use Higher-Order Functions To Reuse Structure

This pattern is powerful when many tasks follow the same overall flow but differ in one step.

For example:

- retry logic
- event handling
- validation pipelines
- collection operations

## Summary

- higher-order functions work with other functions
- they make behavior reusable and flexible
- they are a core idea in modern Dart programming

## Flutter Connection

Higher-order functions appear all over Flutter in:

- callbacks
- builders
- handlers
- collection helpers

Understanding them now will make a lot of Flutter code feel much more natural later.
