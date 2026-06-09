# Nullable Types

## Learning Goal

In this lesson, you will learn how to declare nullable types and when they are the correct choice.

## What Is A Nullable Type

A nullable type is a type that can hold either:

- a normal value
- `null`

In Dart, nullable types are marked with `?`.

## Basic Example

```dart
void main() {
  String? middleName = null;
  print(middleName);
}
```

Here, `middleName` can either store text or be `null`.

## Why Nullable Types Matter

Some values are optional in real life:

- middle name
- profile image
- referral code
- second phone number

Nullable types help model that honestly.

## Example With A Value

```dart
void main() {
  String? nickname = 'Ria';
  print(nickname);
}
```

Later it could also be:

```dart
nickname = null;
```

## Real-World Example

```dart
void main() {
  String? couponCode;

  if (couponCode == null) {
    print('No coupon applied');
  } else {
    print('Coupon: $couponCode');
  }
}
```

## Senior Trick: Nullable Does Not Mean "Use Everywhere"

Only mark a type nullable when it truly can be absent.

Overusing nullable types makes code noisier and weaker because you are telling the compiler:

- "This might be missing"

even when your design says it should always exist.

## Summary

- nullable types are marked with `?`
- they can hold a value or `null`
- they are useful for optional or not-yet-available data
- use them intentionally, not automatically

## Flutter Connection

In Flutter, nullable types are common for:

- optional form values
- image URLs
- delayed API data
- values loaded later in the widget lifecycle

Using them honestly makes app code safer.
