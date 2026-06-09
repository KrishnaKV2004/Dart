# Null Aware Operator

## Learning Goal

In this lesson, you will learn how null-aware operators help you work safely with nullable values.

## Common Null-Aware Operators

Some of the most useful null-aware operators in Dart are:

- `??`
- `?.`
- `??=`

## `??` Fallback Operator

`??` gives a fallback value when something is `null`.

```dart
void main() {
  String? nickname;
  String displayName = nickname ?? 'Guest';

  print(displayName);
}
```

## `?.` Safe Access Operator

`?.` safely accesses a property or method only if the value is not null.

```dart
void main() {
  String? userName;
  print(userName?.length);
}
```

If `userName` is `null`, the result is also `null` instead of crashing.

## `??=` Assign If Null

`??=` assigns a value only if the variable is currently `null`.

```dart
void main() {
  String? city;
  city ??= 'Unknown';

  print(city);
}
```

## Real-World Example

```dart
void main() {
  String? profileImageUrl;
  String imageToShow = profileImageUrl ?? 'default_profile.png';

  print(imageToShow);
}
```

This is exactly the kind of fallback logic used in real apps.

## Senior Trick: Prefer Null-Aware Operators Over Unnecessary `if` Blocks When The Intent Is Simple

Sometimes:

```dart
String displayName = nickname ?? 'Guest';
```

is clearer than:

```dart
String displayName;

if (nickname != null) {
  displayName = nickname;
} else {
  displayName = 'Guest';
}
```

Use the simpler form when it stays readable.

## Summary

- `??` provides a fallback
- `?.` safely accesses members
- `??=` assigns only if the variable is null
- null-aware operators help reduce crashes and boilerplate

## Flutter Connection

In Flutter, null-aware operators are used constantly for:

- fallback text
- optional images
- nullable models
- delayed values

They are a core part of writing clean modern Dart code.
