# Why Null Safety

## Learning Goal

In this lesson, you will understand why null safety exists and why it is such an important feature in Dart.

## The Core Problem

In many languages, a variable can unexpectedly contain `null`.

If the code assumes a value exists and tries to use it, the program may crash.

## Example Of The Problem

Imagine code like this:

```dart
void main() {
  String? userName;
  print(userName!.length);
}
```

If `userName` is `null`, this will fail at runtime.

## Why This Happens In Real Apps

Real app data is often incomplete:

- user skipped an optional field
- API did not return a value
- data has not loaded yet
- object is initialized later

Null safety helps you think about these cases before the app breaks.

## What Null Safety Gives You

Null safety helps Dart:

- catch mistakes earlier
- reduce runtime crashes
- make data expectations clearer
- improve code readability

## Example Of Safer Thinking

```dart
void main() {
  String? userName;

  if (userName != null) {
    print(userName.length);
  } else {
    print('No user name available');
  }
}
```

This code handles the missing case safely.

## Senior Trick: Model Reality Honestly

If a value can truly be missing, make it nullable.
If it should always exist, design the code so it is non-nullable.

Good software design is often about being honest about what data can and cannot guarantee.

## Real-World Example

```dart
void main() {
  String? profileImageUrl;

  if (profileImageUrl == null) {
    print('Show default profile image');
  } else {
    print('Load image from $profileImageUrl');
  }
}
```

This is very common in app development.

## Summary

- null safety exists to prevent bugs caused by missing values
- it helps Dart catch problems earlier
- it makes your code describe data expectations more clearly
- it is one of the biggest reasons Dart code can be so reliable

## Flutter Connection

In Flutter, null safety helps protect your app from crashes related to:

- optional API fields
- not-yet-loaded data
- missing user information
- delayed state initialization
