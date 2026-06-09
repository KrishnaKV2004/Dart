# num

## Learning Goal

In this lesson, you will learn what `num` is, when it can be useful, and why it should be used thoughtfully.

## What Is `num`

`num` is a general numeric type in Dart.
It can hold either:

- an `int`
- a `double`

## Basic Example

```dart
void main() {
  num value = 10;
  print(value);

  value = 10.5;
  print(value);
}
```

## Why `num` Exists

Sometimes your logic only cares that something is numeric, not whether it is a whole number or decimal.

## Example

```dart
void printNumber(num value) {
  print('Number: $value');
}

void main() {
  printNumber(5);
  printNumber(5.75);
}
```

## When `num` Is Useful

- shared numeric utility functions
- calculations that accept both `int` and `double`
- generic number handling

## When `num` Is Not Ideal

If you know the exact meaning, `int` or `double` is usually better.

Example:

```dart
num itemCount = 3;
```

Better:

```dart
int itemCount = 3;
```

Because item count should be whole.

## Senior Trick: Prefer Specific Types Over Broad Types

Use `num` when flexibility is truly needed.
Otherwise:

- choose `int` for whole numbers
- choose `double` for decimal values

Specific types communicate intent better.

## Real-World Example

```dart
num applyTax(num amount, num taxRatePercent) {
  return amount + (amount * taxRatePercent / 100);
}

void main() {
  print(applyTax(100, 18));
  print(applyTax(249.99, 5));
}
```

This works because the function only needs numeric behavior.

## Common Beginner Mistake

Some learners use `num` everywhere because it feels flexible.

That often weakens the code because the reader loses information about what the value really represents.

## Summary

- `num` can hold `int` or `double`
- it is useful when code should accept either numeric type
- do not use it as a lazy replacement for more specific types
- specific types usually make code clearer

## Flutter Connection

You may see `num` in utility logic or generalized calculations, but in Flutter apps you will usually prefer clear domain types like:

- `int` for counts
- `double` for sizes and prices

That keeps UI code easier to understand.
