# Function Basics

## Learning Goal

In this lesson, you will learn what a function is, how to define one, and why functions are central to clean software design.

## What Is A Function

A function is a named block of code that performs a task.

Instead of writing the same logic repeatedly, you can place it in a function and call it whenever needed.

## Basic Example

```dart
void greetUser() {
  print('Welcome to Dart');
}

void main() {
  greetUser();
}
```

## Explanation

### `void`

This means the function does not return a value.

### `greetUser()`

This is the name of the function.

### `{ }`

The code inside the braces is the function body.

### `greetUser();`

This calls the function.

## Why Functions Matter

Without functions, code quickly becomes repetitive and harder to manage.

Example without a function:

```dart
void main() {
  print('Welcome to Dart');
  print('Welcome to Dart');
  print('Welcome to Dart');
}
```

Better:

```dart
void greetUser() {
  print('Welcome to Dart');
}

void main() {
  greetUser();
  greetUser();
  greetUser();
}
```

## Real-World Example

```dart
void showInvoiceHeader() {
  print('=== Invoice ===');
}

void main() {
  showInvoiceHeader();
  print('Customer: Mina');
  print('Total: 2450.75');
}
```

This makes the code cleaner and reusable.

## Senior Trick: Name Functions By Behavior

Weak:

```dart
void doThing() {
  print('Running');
}
```

Better:

```dart
void sendWelcomeEmail() {
  print('Sending welcome email');
}
```

Good function names reduce the need for extra explanation.

## Senior Trick: Keep Functions Small

A good beginner rule is:

- one function
- one clear purpose

If a function loads data, validates input, updates state, and prints output all at once, it is probably too large.

## Summary

- a function is a reusable block of code
- functions make programs cleaner and easier to maintain
- good function names describe behavior clearly
- small functions are easier to understand and trust

## Flutter Connection

In Flutter, small helper functions make widget code much easier to read.
They are also essential for event handling, validation, and reusable business logic.
