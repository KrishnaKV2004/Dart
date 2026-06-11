# `dart:math`

## Learning Goal

In this lesson, you will learn how `dart:math` helps with random numbers, numeric operations, and common math utilities.

## What Is `dart:math`

`dart:math` provides math-related helpers such as:

- `Random`
- `max`
- `min`
- `pow`
- trigonometric functions

## Basic Example

```dart
import 'dart:math';

void main() {
  final random = Random();
  final number = random.nextInt(10);

  print(number);
}
```

Expected output:

```text
6
```

The exact number changes each run.

## Why This Is Useful

This library is useful for:

- generating random values
- numeric calculations
- comparisons
- basic math operations

## Real-World Example

```dart
import 'dart:math';

void main() {
  final values = [12, 8, 19, 4];
  final highest = values.reduce(max);
  final lowest = values.reduce(min);

  print('Highest: $highest');
  print('Lowest: $lowest');
}
```

Expected output:

```text
Highest: 19
Lowest: 4
```

This shows how `dart:math` can help with common numeric tasks.

## Senior Trick: Use Math Helpers Instead Of Rewriting Logic

If the SDK already provides a reliable helper like `max` or `min`, use it.

That makes code shorter and easier to trust.

## Senior Trick: Be Careful With Randomness In Production Logic

Randomness is great for demos, testing ideas, and some app features.

But if your program depends on a random value, make sure that is really what you want.

## Summary

- `dart:math` provides math and random helpers
- it is useful for numbers and comparisons
- it reduces the need for custom math utilities
- random logic should be used intentionally

## Flutter Connection

Flutter apps use `dart:math` for layout calculations, random UI effects, sample data, and numeric helpers.
