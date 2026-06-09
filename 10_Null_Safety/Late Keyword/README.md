# Late Keyword

## Learning Goal

In this lesson, you will learn what `late` means and when it is useful.

## What Does `late` Mean

`late` tells Dart:

- this non-nullable variable will be initialized later
- but it must be assigned before use

## Basic Example

```dart
late String userName;

void main() {
  userName = 'Aditi';
  print(userName);
}
```

## Why `late` Exists

Sometimes a value is not available immediately, but you still want it to be non-nullable once initialized.

Examples:

- value loaded during setup
- controller assigned later
- dependency created after startup

## The Risk Of `late`

If you try to use a `late` variable before assigning it, you get a runtime error.

```dart
late String userName;

void main() {
  print(userName);
}
```

This is unsafe because the variable was never initialized.

## Senior Trick: Use `late` For Delayed Initialization, Not To Avoid Proper Design

`late` is useful, but it should not be a shortcut for unclear lifecycle management.

Ask:

- Can I initialize this value directly?
- Does it truly need delayed setup?

If yes, `late` may be appropriate.

## Real-World Example

```dart
late String apiToken;

void main() {
  apiToken = 'secure_token_123';
  print('Token ready: $apiToken');
}
```

## Summary

- `late` means initialize later
- it allows a variable to stay non-nullable
- it is useful for delayed setup
- it must be assigned before use

## Flutter Connection

In Flutter, `late` is commonly seen with:

- controllers
- dependencies
- values initialized in lifecycle methods

It is helpful, but it should be used carefully and intentionally.
