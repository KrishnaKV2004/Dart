# Anonymous Functions

## Learning Goal

In this lesson, you will learn what anonymous functions are and why they are useful in modern Dart code.

## What Is An Anonymous Function

An anonymous function is a function without a name.

It is often used when a function is needed only once, usually as an argument to another function.

## Basic Example

```dart
void main() {
  List<String> users = ['Asha', 'Ravi', 'Nina'];

  users.forEach((user) {
    print('Hello, $user');
  });
}
```

## Why This Is Useful

The function is short and only needed in that one place.

Giving it a separate name would not add much value here.

## Real-World Example

```dart
void main() {
  List<double> prices = [500, 1200, 800];

  prices.forEach((price) {
    print('Price: $price');
  });
}
```

## Senior Trick: Anonymous Functions Are Great For Local Behavior

Use them when:

- the behavior is short
- the behavior is only used once
- keeping the logic close to the call improves readability

If the logic gets large, move it into a named function.

## Summary

- anonymous functions have no name
- they are useful for short one-time behavior
- they are common when passing functions into other functions

## Flutter Connection

In Flutter, anonymous functions are used constantly for:

- button `onPressed` handlers
- callbacks
- inline event logic

This is one of the most practical function styles to understand early.
