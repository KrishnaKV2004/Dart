# Collection If

## Learning Goal

In this lesson, you will learn how to conditionally include items inside a collection using `if`.

## What Is Collection `if`

Collection `if` lets you put conditions directly inside a collection literal.

That means an item is included only if the condition is true.

## Basic Example

```dart
void main() {
  bool isPremiumUser = true;

  List<String> menuItems = [
    'Home',
    'Profile',
    if (isPremiumUser) 'Premium Content',
  ];

  print(menuItems);
}
```

## Why This Is Useful

Without collection `if`, you would need to:

- create the list
- check a condition later
- manually add items

Collection `if` keeps the logic closer to the data definition.

## Real-World Example

```dart
void main() {
  bool showDiscount = true;

  List<String> orderSummary = [
    'Subtotal: 2000',
    if (showDiscount) 'Discount: 200',
    'Final Total: 1800',
  ];

  print(orderSummary);
}
```

## Senior Trick: Use Collection `if` For Declarative Data Building

This style is especially powerful when you want your code to describe:

- what should exist
- instead of how to mutate a list step by step

That is one reason it fits Flutter so well.

## Summary

- collection `if` conditionally includes items in a collection literal
- it keeps collection-building code cleaner and more declarative
- it is very useful for dynamic data and UI construction

## Flutter Connection

In Flutter, collection `if` is used constantly for:

- optional widgets
- dynamic menu items
- conditional action buttons
- state-based UI pieces

This is a very important modern Dart feature for Flutter developers.
