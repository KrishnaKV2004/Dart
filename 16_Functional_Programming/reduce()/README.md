# `reduce()`

## Learning Goal

In this lesson, you will learn how `reduce()` combines items in a collection without needing an explicit initial value.

## What Does `reduce()` Do

`reduce()` merges collection items into a single result by repeatedly combining two values at a time.

It uses the first item as the starting point.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4];
  int total = numbers.reduce((value, element) => value + element);

  print(total);
}
```

The values are combined until one result remains.

## Why This Is Useful

`reduce()` is useful when the collection already has a natural starting item.

It can make combination logic compact and readable.

## Real-World Example

```dart
void main() {
  List<String> names = ['Asha', 'Ravi', 'Nina'];
  String combined = names.reduce((a, b) => '$a, $b');

  print(combined);
}
```

This joins values into one output string.

## Senior Trick: Use `reduce()` Only When The Collection Is Not Empty

`reduce()` depends on having at least one item.

If the list may be empty, `fold()` is usually safer.

## Senior Trick: Choose The Right Tool Between `fold()` And `reduce()`

Use `fold()` when you need an initial value.

Use `reduce()` when the collection already provides the starting value naturally.

## Summary

- `reduce()` combines items into one result
- it does not use an explicit initial value
- it is best for non-empty collections
- `fold()` is safer for empty collections

## Flutter Connection

`reduce()` is useful in Flutter for combining values, building labels, and summarizing list data when you know the collection is not empty.
