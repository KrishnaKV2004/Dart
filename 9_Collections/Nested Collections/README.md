# Nested Collections

## Learning Goal

In this lesson, you will learn what nested collections are and how to work with them carefully.

## What Are Nested Collections

Nested collections are collections inside other collections.

Examples:

- a list of maps
- a map containing lists
- a list of lists

These structures are very common in real application data.

## Example: List Of Maps

```dart
void main() {
  List<Map<String, dynamic>> products = [
    {'name': 'Phone', 'price': 40000},
    {'name': 'Laptop', 'price': 65000},
  ];

  print(products[0]['name']);
  print(products[1]['price']);
}
```

## Example: Map With A List

```dart
void main() {
  Map<String, dynamic> order = {
    'customer': 'Asha',
    'items': ['Mouse', 'Keyboard'],
  };

  print(order['customer']);
  print(order['items']);
}
```

## Why Nested Collections Matter

Real APIs and app data are often nested.

For example:

- a user has many addresses
- an order has many items
- a dashboard has sections with different lists

## Senior Trick: Give Nested Data Strong Types When Possible

This:

```dart
List<Map<String, dynamic>> products = [];
```

is common for raw data.

But as apps grow, it is often better to move toward model classes instead of staying with deep nested maps forever.

That improves:

- readability
- safety
- maintainability

## Real-World Example

```dart
void main() {
  List<Map<String, dynamic>> notifications = [
    {'title': 'Payment Received', 'isRead': true},
    {'title': 'New Offer', 'isRead': false},
  ];

  for (Map<String, dynamic> notification in notifications) {
    print('Title: ${notification['title']}');
    print('Read: ${notification['isRead']}');
  }
}
```

## Summary

- nested collections are collections inside collections
- they are very common in real app and API data
- they are powerful but can become complex
- strong typing and good structure become more important as nesting grows

## Flutter Connection

Nested collections show up constantly in Flutter apps when dealing with:

- API responses
- grouped UI data
- configuration structures
- temporary raw models before conversion into proper classes

Understanding them now prepares you well for real-world data handling.
