# switch

## Learning Goal

In this lesson, you will learn how to use `switch` when one value needs to be matched against multiple known cases.

## What Is `switch`

`switch` is often cleaner than a long `else if` chain when:

- one variable is being checked
- against several known values

## Basic Example

```dart
void main() {
  String day = 'Monday';

  switch (day) {
    case 'Monday':
      print('Start of work week');
    case 'Friday':
      print('Almost weekend');
    default:
      print('Regular day');
  }
}
```

## Important Note About Dart `switch`

In modern Dart, each case must end cleanly and cannot accidentally fall through in the old C-style way.
That makes `switch` safer and easier to reason about.

## Better Example

```dart
void main() {
  String orderStatus = 'processing';

  switch (orderStatus) {
    case 'pending':
      print('Order received');
    case 'processing':
      print('Preparing your order');
    case 'shipped':
      print('Order is on the way');
    default:
      print('Unknown status');
  }
}
```

## Why `switch` Is Useful

It makes category-based logic easier to scan.

Compared with a long `else if`, `switch` often looks cleaner when all branches depend on the same value.

## Senior Trick: Use `switch` For Known States

`switch` is a strong choice for values like:

- order status
- screen state
- menu action
- role name
- enum values later on

## Example With User Roles

```dart
void main() {
  String role = 'admin';

  switch (role) {
    case 'admin':
      print('Full access');
    case 'editor':
      print('Can modify content');
    case 'viewer':
      print('Read-only access');
    default:
      print('Role not recognized');
  }
}
```

## When Not To Use `switch`

If your conditions depend on ranges like:

- score > 80
- total >= 2000

then `if`, `if else`, or `else if` may be more natural.

## Summary

- `switch` is useful when one value is compared against many known cases
- it often reads more clearly than a long `else if` chain
- use it for categories, states, and fixed labels

## Flutter Connection

In Flutter, `switch` is helpful for:

- rendering by status
- handling screen modes
- reacting to enum-like app states
- mapping actions to known cases

It becomes even more valuable as apps grow.
