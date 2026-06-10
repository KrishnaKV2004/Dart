# bool

## Learning Goal

In this lesson, you will learn what `bool` is, how it controls decision-making, and why it is one of the most important types in app logic.

## What Is `bool`

`bool` stores one of two values:

- `true`
- `false`

It is used when something has a yes/no, on/off, or active/inactive state.

## Basic Example

```dart
void main() {
  bool isLoggedIn = true;
  bool isAdmin = false;

  print(isLoggedIn);
  print(isAdmin);
}
```

## Why `bool` Matters

Much of programming is about decisions.

Examples:

- Is the user logged in?
- Is the form valid?
- Is the payment complete?
- Is dark mode enabled?

## Example With `if`

```dart
void main() {
  bool isPremiumUser = true;

  if (isPremiumUser) {
    print('Show premium content');
  } else {
    print('Show standard content');
  }
}
```

## Real-World Example

```dart
void main() {
  bool isCartEmpty = false;

  if (isCartEmpty) {
    print('Your cart is empty');
  } else {
    print('Proceed to checkout');
  }
}
```

## Senior Trick: Name Boolean Variables Like Questions Or States

Weak:

```dart
bool value = true;
```

Better:

```dart
bool isLoading = true;
bool hasPermission = false;
bool canCheckout = true;
```

These names read naturally and make conditions easier to understand.

## Common Mistake: Comparing Bool To `true` Unnecessarily

Less clean:

```dart
if (isLoggedIn == true) {
  print('Welcome');
}
```

Better:

```dart
if (isLoggedIn) {
  print('Welcome');
}
```

And for false:

```dart
if (!isLoggedIn) {
  print('Please log in');
}
```

## Summary

- `bool` stores `true` or `false`
- it drives decisions and state checks
- clear boolean names make code much easier to read
- boolean logic is central to real applications

## Flutter Connection

In Flutter, booleans are constantly used for:

- loading indicators
- toggle switches
- validation states
- selected items
- visibility conditions

If you understand `bool` well, UI logic becomes much easier.
