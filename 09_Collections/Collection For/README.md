# Collection For

## Learning Goal

In this lesson, you will learn how to generate collection items dynamically using `for` inside collection literals.

## What Is Collection `for`

Collection `for` lets you create items inside a collection using a loop directly in the collection literal.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 2, 3];

  List<String> labels = [
    for (int number in numbers) 'Item $number',
  ];

  print(labels);
}
```

## Why This Is Useful

It lets you transform data while building a new collection.

Instead of:

- creating an empty collection
- looping later
- adding items one by one

you can express the transformation directly.

## Real-World Example

```dart
void main() {
  List<String> products = ['Phone', 'Laptop', 'Watch'];

  List<String> productLabels = [
    for (String product in products) 'Product: $product',
  ];

  print(productLabels);
}
```

## Senior Trick: Collection `for` Encourages Declarative Thinking

This style helps code read more like:

- "build this collection from that data"

instead of:

- "start empty, mutate, add, update"

That mindset becomes very valuable in Flutter.

## Summary

- collection `for` builds items dynamically inside collection literals
- it is useful for transforming data into another collection
- it supports a cleaner, more declarative style

## Flutter Connection

Collection `for` is very useful in Flutter for:

- generating widget lists
- transforming model data into UI pieces
- building repeated sections from app data

It is one of the most practical bridges between Dart collections and Flutter UI.
