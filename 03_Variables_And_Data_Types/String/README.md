# String

## Learning Goal

In this lesson, you will learn what `String` is, how to work with text, and why strings are central to nearly every app.

## What Is `String`

`String` is the data type for text.

Examples:

- names
- messages
- labels
- emails
- product titles

## Basic Example

```dart
void main() {
  String name = 'Maya';
  String city = 'Delhi';

  print(name);
  print(city);
}
```

## String Interpolation

One of the most useful features in Dart is interpolation:

```dart
void main() {
  String name = 'Maya';
  print('Welcome, $name');
}
```

For expressions:

```dart
void main() {
  int items = 4;
  print('Total items: ${items + 1}');
}
```

## Why Strings Matter So Much

Almost every app works with text:

- usernames
- passwords
- screen titles
- API values
- search input
- error messages

## Real-World Example

```dart
void main() {
  String productName = 'Bluetooth Speaker';
  String status = 'In Stock';

  print('Product: $productName');
  print('Status: $status');
}
```

## Single Quotes And Double Quotes

Both are valid:

```dart
String first = 'Hello';
String second = "World";
```

Choose one style and stay consistent.

## Multi-Line String

```dart
void main() {
  String message = '''
Welcome to the app.
Please complete your profile.
Enjoy your experience.
''';

  print(message);
}
```

## Senior Trick: Treat Strings As Data, Not Just Display

Beginners often think strings are only for showing text.
But strings are also used for:

- IDs
- API payload fields
- route names
- search terms
- dates in raw text form

That means naming and validation matter.

## Common Mistakes

### Forgetting quotes

```dart
String name = Maya;
```

This is invalid because text must be wrapped in quotes.

### Using strings for numbers without reason

```dart
String price = '499';
```

If the value is truly numeric and needs calculations, prefer `int` or `double`.

## Summary

- `String` stores text
- it is used for names, labels, messages, and many real app values
- string interpolation makes output more readable
- strings should be named clearly and used intentionally

## Flutter Connection

In Flutter, strings are used constantly for:

- widget text
- form input
- navigation labels
- API fields
- validation messages

Strong string handling is a very practical skill for app development.
