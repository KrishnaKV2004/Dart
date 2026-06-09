# Best Practices

## Learning Goal

In this lesson, you will learn strong null-safety habits that help keep Dart and Flutter code reliable.

## 1. Prefer Non-Nullable By Default

Start with non-nullable types unless the value can genuinely be missing.

Good:

```dart
String appName = 'TaskFlow';
```

Only make it nullable when needed:

```dart
String? referralCode;
```

## 2. Use Nullable Types Honestly

If something is optional in the real world, model it that way.

Examples:

- optional nickname
- profile image URL
- delivery note

## 3. Avoid Using `!` As A Shortcut

Weak habit:

```dart
print(userName!.length);
```

Better:

```dart
if (userName != null) {
  print(userName.length);
}
```

Use `!` only when the program has already guaranteed safety.

## 4. Prefer Null-Aware Operators For Simple Cases

```dart
String displayName = nickname ?? 'Guest';
```

This is often clearer than a longer `if-else`.

## 5. Use `late` Carefully

`late` is useful, but it is not magic.
If the value might be forgotten before use, that is a design risk.

## 6. Design Functions And Models Clearly

When writing functions or classes, think carefully about which fields and parameters:

- must exist
- may be missing

That clarity improves your whole codebase.

## Real-World Example

```dart
void showProfile(String userName, String? profileImageUrl) {
  print('User: $userName');
  print('Image: ${profileImageUrl ?? 'default_profile.png'}');
}
```

This is a nice example of:

- non-nullable required data
- nullable optional data
- safe fallback handling

## Senior Trick: Model Missing States Explicitly

Instead of hoping data exists, ask:

- What should happen if it is null?
- Should I show fallback UI?
- Should I block the action?
- Should I wait until data is loaded?

That mindset is what keeps real apps stable.

## Summary

- prefer non-nullable by default
- make types nullable only when needed
- avoid careless `!`
- use null-aware operators for simple safe handling
- treat nullability as part of the data model

## Flutter Connection

These best practices are especially important in Flutter because app UIs constantly react to:

- async loading states
- optional input
- missing backend fields
- delayed initialization

Strong null-safety habits prevent many production bugs.
