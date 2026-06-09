# if else

## Learning Goal

In this lesson, you will learn how to choose between two paths using `if else`.

## What Is `if else`

`if else` is used when your program must choose one of two possible outcomes.

If the condition is true, the `if` block runs.
Otherwise, the `else` block runs.

## Basic Example

```dart
void main() {
  int score = 45;

  if (score >= 50) {
    print('Pass');
  } else {
    print('Fail');
  }
}
```

## Why `if else` Is Useful

Many real decisions are two-way:

- logged in or not
- premium or standard
- available or unavailable
- success or failure

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

## Senior Trick: Keep The Condition Positive When Possible

This is often easier to read:

```dart
if (isLoggedIn) {
  print('Open dashboard');
} else {
  print('Show login screen');
}
```

than deeply negative logic like:

```dart
if (!isLoggedOut) {
  print('Open dashboard');
}
```

Positive names reduce mental effort.

## Example With Real App Thinking

```dart
void main() {
  double walletBalance = 1500;
  double purchaseAmount = 1800;

  if (walletBalance >= purchaseAmount) {
    print('Payment successful');
  } else {
    print('Insufficient balance');
  }
}
```

This is the type of branching you will use in payment and validation flows.

## Senior Trick: If Both Branches Get Large, Move Them Into Functions

Instead of:

```dart
if (isLoggedIn) {
  print('Load user profile');
  print('Load dashboard');
  print('Load notifications');
} else {
  print('Show login');
  print('Show sign up');
}
```

Prefer:

```dart
void main() {
  bool isLoggedIn = true;

  if (isLoggedIn) {
    openDashboard();
  } else {
    showAuthOptions();
  }
}

void openDashboard() {
  print('Load user profile');
  print('Load dashboard');
  print('Load notifications');
}

void showAuthOptions() {
  print('Show login');
  print('Show sign up');
}
```

This keeps the decision readable.

## Summary

- `if else` chooses between two paths
- it is ideal for yes/no style business rules
- positive condition names improve readability
- large branches should often be moved into small functions

## Flutter Connection

In Flutter, `if else` is used for:

- loading vs content
- success vs error UI
- authenticated vs guest screens
- enabled vs disabled actions

Clear branching makes interfaces easier to reason about.
