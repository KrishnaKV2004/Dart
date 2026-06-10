# Spread Operator

## Learning Goal

In this lesson, you will learn how the spread operator helps combine collections cleanly.

## What Is The Spread Operator

The spread operator is `...`.

It lets you insert all items from one collection into another collection.

## Basic Example

```dart
void main() {
  List<String> baseItems = ['Phone', 'Charger'];
  List<String> fullItems = [...baseItems, 'Cover'];

  print(fullItems);
}
```

## Why It Matters

The spread operator is a very clean way to merge collections.

It is often easier to read than manual add operations.

## Real-World Example

```dart
void main() {
  List<String> defaultPermissions = ['read'];
  List<String> adminPermissions = [
    ...defaultPermissions,
    'write',
    'delete',
  ];

  print(adminPermissions);
}
```

## Senior Trick: Spread Makes Data Composition Cleaner

This style is especially useful when building data from:

- defaults
- conditionally added values
- existing lists plus new items

That style appears often in modern Dart and Flutter.

## Null-Aware Spread

There is also a null-aware spread:

```dart
void main() {
  List<String>? extraItems;
  List<String> items = ['Base', ...?extraItems];

  print(items);
}
```

If `extraItems` is `null`, nothing is added and no error occurs.

## Summary

- `...` spreads items from one collection into another
- it makes collection composition cleaner
- `...?` safely spreads nullable collections

## Flutter Connection

The spread operator is heavily used in Flutter for:

- widget lists
- menu items
- dynamic UI pieces
- merging default and custom values

This is one of the most practical modern Dart features for UI work.
