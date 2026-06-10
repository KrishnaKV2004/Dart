# `fold()`

## Learning Goal

In this lesson, you will learn how `fold()` combines a collection into a single result.

## What Does `fold()` Do

`fold()` starts with an initial value and then combines each item into one final result.

It is used when you want to summarize data.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4];
  int total = numbers.fold(0, (sum, n) => sum + n);

  print(total);
}
```

The items are combined into a single total.

## Why This Is Useful

`fold()` is great for:

- totals
- concatenation
- summaries
- derived values

It gives you one result from many inputs.

## Real-World Example

```dart
void main() {
  List<String> words = ['Dart', 'is', 'fun'];
  String sentence = words.fold('', (result, word) => '$result $word').trim();

  print(sentence);
}
```

This builds a final string from a list of pieces.

## Senior Trick: Choose A Clear Initial Value

The initial value is part of the logic.

Make sure it makes sense for the final result you want.

## Senior Trick: Use `fold()` When You Need Control Over The Accumulator

`fold()` is useful when the accumulation logic is custom and you want to control the starting value.

That makes it more flexible than a simple sum helper.

## Summary

- `fold()` reduces many items into one result
- it starts with an initial value
- it is useful for summaries and totals
- it gives you control over accumulation

## Flutter Connection

`fold()` is often useful in Flutter for building summaries, totals, labels, and derived display values.
