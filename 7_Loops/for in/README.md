# for in

## Learning Goal

In this lesson, you will learn how to iterate through collections cleanly using `for in`.

## What Is `for in`

`for in` is used to loop through each item in a collection, such as a list.

## Basic Example

```dart
void main() {
  List<String> fruits = ['Apple', 'Banana', 'Mango'];

  for (String fruit in fruits) {
    print(fruit);
  }
}
```

## Why `for in` Is Useful

It is often cleaner than an index-based loop when you only need the items themselves.

## Compare With Index-Based `for`

```dart
for (int i = 0; i < fruits.length; i++) {
  print(fruits[i]);
}
```

This works, but if you do not need `i`, `for in` is more direct.

## Real-World Example

```dart
void main() {
  List<String> notifications = [
    'Payment received',
    'New message',
    'Order shipped',
  ];

  for (String notification in notifications) {
    print('Notification: $notification');
  }
}
```

## Senior Trick: Prefer `for in` When You Do Not Need The Index

This keeps code focused on the real data instead of the mechanics of counting.

## When Not To Use `for in`

If you need:

- index positions
- custom stepping
- backward movement

then a traditional `for` loop may be better.

## Summary

- `for in` loops through each item in a collection
- it is clean and readable when you only need the values
- use a normal `for` loop when index control matters

## Flutter Connection

In Flutter, `for in` is great for:

- processing lists of models
- building repeated output from data
- validating or transforming collections before display

It is one of the most readable loop styles for real app data.
