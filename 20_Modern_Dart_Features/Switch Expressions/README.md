# Switch Expressions

## Learning Goal

In this lesson, you will learn how switch expressions provide a concise way to return values from branching logic.

## What Is A Switch Expression

A switch expression is a switch that produces a value directly.

This is cleaner than using a long switch statement when you just need a result.

## Basic Example

```dart
void main() {
  final day = 'Monday';

  final message = switch (day) {
    'Monday' => 'Start strong',
    'Friday' => 'Almost weekend',
    _ => 'Regular day',
  };

  print(message);
}
```

Expected output:

```text
Start strong
```

The switch returns a value directly.

## Why This Is Useful

Switch expressions are useful when:

- you need one result from many choices
- the branching logic is simple
- you want concise readable code

## Real-World Example

```dart
void main() {
  final score = 87;

  final grade = switch (score) {
    >= 90 => 'A',
    >= 80 => 'B',
    >= 70 => 'C',
    _ => 'Needs improvement',
  };

  print(grade);
}
```

Expected output:

```text
B
```

This shows how switch expressions can make decision logic very compact.

## Senior Trick: Use Switch Expressions For Value Selection

If your switch is really just choosing a result, a switch expression is usually a better fit than a statement.

It reads more directly.

## Senior Trick: Keep The Cases Clean

A switch expression should stay simple enough to understand at a glance.

If the branches become large, it may be better to move the logic into named functions.

## Summary

- switch expressions return a value directly
- they are concise and readable
- they work well for simple branching
- they are best when choosing one result

## Flutter Connection

Switch expressions are useful in Flutter for labels, state mapping, UI variants, and simple response selection.
