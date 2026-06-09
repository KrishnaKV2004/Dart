# Labels

## Learning Goal

In this lesson, you will learn what labels are and when they can help with nested loops.

## What Are Labels

Labels give a name to a loop or block so you can target it with `break` or `continue`.

## Basic Example

```dart
void main() {
  outerLoop:
  for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
      if (i == 2 && j == 2) {
        break outerLoop;
      }

      print('i = $i, j = $j');
    }
  }
}
```

## What Happened

Without the label, `break` would only exit the inner loop.
With `break outerLoop`, the outer loop also stops.

## When Labels Are Useful

Labels are most useful in nested loops where you need precise control.

## Senior Trick: Use Labels Sparingly

Labels are valid and sometimes helpful, but if you need many of them, it may be a sign that the loop logic should be refactored.

Often a better structure is:

- extract logic into functions
- return early from functions
- simplify nested looping

## Summary

- labels let you target outer loops with `break` or `continue`
- they are mainly useful in nested loops
- use them carefully and not as a replacement for clear structure

## Flutter Connection

Labels are less common in day-to-day Flutter code, but understanding them helps when reading more advanced Dart logic involving nested iteration or search behavior.
