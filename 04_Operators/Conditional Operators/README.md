# Conditional Operators

## Learning Goal

In this lesson, you will learn how conditional operators let you choose values compactly and clearly.

## Main Conditional Operators In Dart

The most common ones are:

- ternary operator: `condition ? value1 : value2`
- null-coalescing operator: `??`

## Ternary Operator

The ternary operator is a short form of `if-else` when choosing between two values.

### Basic Example

```dart
void main() {
  int age = 20;
  String result = age >= 18 ? 'Adult' : 'Minor';

  print(result);
}
```

## Equivalent `if-else`

```dart
void main() {
  int age = 20;
  String result;

  if (age >= 18) {
    result = 'Adult';
  } else {
    result = 'Minor';
  }

  print(result);
}
```

## When To Use Ternary

Use it when:

- the condition is simple
- the result is a single value choice

Avoid it when the logic becomes long or nested.

## Senior Trick: Keep Ternary Short

Good:

```dart
String buttonText = isLoggedIn ? 'Logout' : 'Login';
```

Less good:

```dart
String message = isLoggedIn
    ? hasProfile
        ? 'Open dashboard'
        : 'Complete profile'
    : 'Please log in';
```

If logic becomes layered, use normal `if-else` or named booleans.

## Null-Coalescing Operator `??`

`??` provides a fallback when a value is `null`.

### Example

```dart
void main() {
  String? nickname;
  String displayName = nickname ?? 'Guest';

  print(displayName);
}
```

## Why `??` Is Useful

It is very common in real apps for some values to be optional:

- profile photo
- nickname
- coupon code
- delivery notes

`??` lets you provide a safe default.

## Real-World Example

```dart
void main() {
  String? couponCode;
  String appliedCoupon = couponCode ?? 'No coupon applied';

  print(appliedCoupon);
}
```

## Summary

- the ternary operator chooses between two values
- `??` provides a fallback for `null`
- use conditional operators for concise, readable value selection
- do not compress complex logic into unreadable one-liners

## Flutter Connection

Conditional operators are used constantly in Flutter for:

- button labels
- fallback text
- optional image URLs
- dynamic UI values

They are small tools, but they show up everywhere in app code.
