# const

## Learning Goal

In this lesson, you will learn what `const` means, how it differs from `final`, and why it matters in both Dart and Flutter.

## What Is `const`

`const` creates a compile-time constant.

That means the value must be known before the program runs.

## Basic Example

```dart
void main() {
  const double pi = 3.14159;
  print(pi);
}
```

This is valid because the value is fixed and known immediately.

## `const` vs `final`

This is one of the most important distinctions:

- `final`: assigned once at runtime
- `const`: fixed at compile time

Example:

```dart
void main() {
  final currentTime = DateTime.now();
  print(currentTime);
}
```

This works with `final` because the value is decided when the program runs.

This would not work with `const`:

```dart
void main() {
  const currentTime = DateTime.now();
}
```

Why:

- `DateTime.now()` is not known at compile time

## Good Use Cases For `const`

- mathematical constants
- fixed configuration values
- values that should never change in any run of the program

## Real Example

```dart
const int maxLoginAttempts = 5;
const String companyName = 'Acme Tech';
const double taxRate = 0.18;
```

## `const` Collections

```dart
void main() {
  const List<String> roles = ['admin', 'editor', 'viewer'];
  print(roles);
}
```

A `const` collection cannot be modified.

```dart
void main() {
  const List<String> roles = ['admin', 'editor', 'viewer'];
  roles.add('guest');
}
```

This is invalid.

## Why `const` Is Useful

`const` makes your intent very strong:

- this value is fixed
- this value is deeply immutable
- this value can be treated as a true constant

## Senior Trick: Use `const` Only When You Mean True Constant

Do not force `const` everywhere.

Ask:

- Is this value truly permanent?
- Is it known before runtime?

If yes, `const` is great.
If not, prefer `final`.

## Example: `const` In App Thinking

```dart
const String appTitle = 'Finance Tracker';
const int maxItemsPerPage = 20;
```

These are fixed rules or labels that do not depend on user behavior.

## Common Beginner Confusion

### "If it does not change, should I always use `const`?"

No.

Example:

```dart
void main() {
  final userName = getUserName();
  print(userName);
}

String getUserName() {
  return 'Kiran';
}
```

Even if `userName` never changes after assignment, it is still a runtime value, so `final` is correct.

## Senior Trick: Prefer `final`, Upgrade To `const` When Truly Constant

That is a simple and safe rule for many developers.

## Summary

- `const` means compile-time constant
- use it for values known before the program runs
- `const` is stricter than `final`
- if the value comes from runtime, use `final` instead

## Flutter Connection

In Flutter, `const` becomes especially valuable for:

- constant widgets
- fixed styling values
- immutable configuration

You do not need to master all Flutter uses yet, but understanding `const` here gives you a big advantage later.
