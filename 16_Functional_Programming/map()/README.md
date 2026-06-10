# `map()`

## Learning Goal

In this lesson, you will learn how `map()` transforms each item in a collection into a new value.

## What Does `map()` Do

`map()` applies a function to each item and returns a new iterable with the transformed results.

It is used when you want to change the shape of data.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 2, 3];
  List<int> doubled = numbers.map((n) => n * 2).toList();

  print(doubled);
}
```

Each number is transformed into a new number.

## Why This Is Useful

`map()` helps you convert data cleanly without manually building a new list with a loop.

## Real-World Example

```dart
void main() {
  List<String> names = ['Asha', 'Ravi'];
  List<String> labels = names.map((name) => 'User: $name').toList();

  print(labels);
}
```

This is a direct way to transform values for display or processing.

## Senior Trick: Use `map()` For Transformation, Not Filtering

`map()` changes values.

If you want to remove values, use a filtering method like `where()`.

That separation keeps the intent clear.

## Senior Trick: Convert To A List Only When Needed

`map()` returns an iterable.

If you do not need a list immediately, keep it lazy for as long as possible.

## Summary

- `map()` transforms each item in a collection
- it returns a new iterable
- it is best for data conversion
- it is not meant for filtering

## Flutter Connection

`map()` is very common in Flutter for building widget lists, model lists, and display-friendly data.
