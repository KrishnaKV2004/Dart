# Collection Methods

## Learning Goal

In this lesson, you will learn how built-in collection methods help you process data more cleanly and expressively.

## Why Collection Methods Matter

Instead of writing manual loops for everything, Dart provides methods that make collection code shorter and often clearer.

Common methods include:

- `add()`
- `remove()`
- `contains()`
- `length`
- `isEmpty`
- `isNotEmpty`

Later, you will also use more functional methods like `map()` and `where()`.

## Basic Example

```dart
void main() {
  List<String> items = ['Pen', 'Notebook'];

  items.add('Bag');
  print(items);

  items.remove('Pen');
  print(items);
}
```

## Checking Values

```dart
void main() {
  List<String> users = ['Aman', 'Riya', 'Sara'];

  print(users.contains('Riya'));
  print(users.length);
  print(users.isEmpty);
}
```

## Real-World Example

```dart
void main() {
  List<String> notifications = ['Order shipped', 'Payment received'];

  if (notifications.isNotEmpty) {
    print('You have ${notifications.length} notifications');
  }
}
```

## Senior Trick: Prefer Intent-Revealing Methods

This:

```dart
if (notifications.length > 0) {
  print('Has notifications');
}
```

works, but this is often cleaner:

```dart
if (notifications.isNotEmpty) {
  print('Has notifications');
}
```

The second version communicates intent better.

## Summary

- collection methods help you manage and inspect data
- they reduce the need for manual repetitive logic
- methods like `contains`, `isEmpty`, and `length` are used constantly

## Flutter Connection

In Flutter, collection methods are used all the time for:

- checking whether to show empty states
- counting items
- removing or adding data
- deciding how UI should react to a collection

These methods quickly become part of everyday coding.
