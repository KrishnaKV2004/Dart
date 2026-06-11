# Enhanced Enums

## Learning Goal

In this lesson, you will learn how enhanced enums let enums hold values, fields, and behavior.

## What Is An Enhanced Enum

An enhanced enum is an enum that can include additional data and methods.

That makes enums much more useful than simple named constants.

## Basic Example

```dart
enum Status {
  pending('Pending'),
  success('Success'),
  failed('Failed');

  final String label;

  const Status(this.label);
}

void main() {
  print(Status.success.label);
}
```

Expected output:

```text
Success
```

The enum stores a label with each value.

## Why This Is Useful

Enhanced enums are useful when each enum value has:

- a display label
- a code
- a custom behavior
- a meaningful property

## Real-World Example

```dart
enum PaymentStatus {
  pending('Waiting'),
  paid('Completed'),
  failed('Failed');

  final String text;

  const PaymentStatus(this.text);
}

void main() {
  final status = PaymentStatus.paid;
  print('Status: ${status.text}');
}
```

Expected output:

```text
Status: Completed
```

This is a clean way to keep display data with the enum itself.

## Senior Trick: Put Shared Meaning In The Enum

If every value needs the same kind of metadata, the enum is a great home for it.

That keeps related information together instead of spreading it across the code base.

## Senior Trick: Use Enums For Small Fixed Sets

Enums work best when the set of values is closed and known ahead of time.

If the list is expected to grow dynamically, another structure may be better.

## Summary

- enhanced enums can store data and behavior
- they are more expressive than simple enums
- they are useful for fixed sets with metadata
- they help keep related meaning together

## Flutter Connection

Enhanced enums are useful in Flutter for statuses, tabs, states, labels, and other small fixed sets of options.
