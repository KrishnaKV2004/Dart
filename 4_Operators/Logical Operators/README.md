# Logical Operators

## Learning Goal

In this lesson, you will learn how to combine or invert conditions in Dart using logical operators.

## What Are Logical Operators

Logical operators work with boolean values:

- `&&` and
- `||` or
- `!` not

## Basic Example

```dart
void main() {
  bool isLoggedIn = true;
  bool isPremiumUser = false;

  print(isLoggedIn && isPremiumUser);
  print(isLoggedIn || isPremiumUser);
  print(!isLoggedIn);
}
```

## Meaning

### `&&`

Both conditions must be true.

### `||`

At least one condition must be true.

### `!`

Reverses a boolean value.

## Real-World Example

```dart
void main() {
  bool isLoggedIn = true;
  bool hasCompletedProfile = true;

  if (isLoggedIn && hasCompletedProfile) {
    print('Open dashboard');
  } else {
    print('Complete setup first');
  }
}
```

## Using `||`

```dart
void main() {
  bool isAdmin = false;
  bool isModerator = true;

  if (isAdmin || isModerator) {
    print('Access granted');
  } else {
    print('Access denied');
  }
}
```

## Using `!`

```dart
void main() {
  bool isLoading = false;

  if (!isLoading) {
    print('Show content');
  }
}
```

## Senior Trick: Break Complex Logic Into Named Booleans

Less readable:

```dart
if (isLoggedIn && hasSubscription && !isBanned) {
  print('Access allowed');
}
```

Better:

```dart
bool canAccessContent = isLoggedIn && hasSubscription && !isBanned;

if (canAccessContent) {
  print('Access allowed');
}
```

This makes code easier to scan and discuss with teammates.

## Summary

- `&&` means both conditions must be true
- `||` means at least one must be true
- `!` reverses a boolean value
- named boolean expressions improve readability

## Flutter Connection

Logical operators are used heavily in Flutter for:

- access control
- validation rules
- loading and visibility checks
- deciding which widget tree branch to show

Readable logic here pays off quickly in UI code.
