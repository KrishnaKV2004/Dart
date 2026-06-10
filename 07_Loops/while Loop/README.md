# while Loop

## Learning Goal

In this lesson, you will learn how to use a `while` loop when repetition depends on a condition instead of a fixed count.

## What Is A `while` Loop

A `while` loop keeps running as long as its condition is true.

## Basic Example

```dart
void main() {
  int count = 1;

  while (count <= 3) {
    print(count);
    count++;
  }
}
```

## Why `while` Is Useful

Use `while` when you do not want the loop structure to focus on counting syntax.

It is often helpful when the loop represents a state-based process.

## Real-World Example

```dart
void main() {
  int retryCount = 0;

  while (retryCount < 3) {
    print('Retry attempt ${retryCount + 1}');
    retryCount++;
  }
}
```

This is similar to retry logic in networking or login flows.

## Common Danger: Infinite Loops

If the condition never becomes false, the loop never stops.

Wrong:

```dart
void main() {
  int count = 1;

  while (count <= 3) {
    print(count);
  }
}
```

This never updates `count`, so it keeps running.

## Senior Trick: Make Progress Visible

Every loop should have a clear path toward ending.

Ask:

- What changes on each iteration?
- What eventually makes the condition false?

If that is not obvious, the loop needs improvement.

## Summary

- `while` loops repeat while a condition remains true
- they are useful for condition-driven repetition
- always make sure something changes so the loop can end
- infinite loops usually come from missing updates

## Flutter Connection

In Flutter, you may use similar condition-driven repetition in pure Dart logic, data processing, or retry workflows, even if UI code itself is more declarative.
