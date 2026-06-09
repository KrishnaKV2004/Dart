# Lists

## Learning Goal

In this lesson, you will learn what a `List` is, when to use it, and why lists are one of the most common collection types in Dart.

## What Is A List

A `List` stores multiple values in an ordered collection.

That means:

- items keep their order
- items can be accessed by index
- duplicates are allowed

## Basic Example

```dart
void main() {
  List<String> fruits = ['Apple', 'Banana', 'Mango'];

  print(fruits);
  print(fruits[0]);
}
```

## Why Lists Matter

Lists are perfect when you have many items in a sequence.

Examples:

- product list
- chat messages
- order history
- task list

## Adding And Removing Items

```dart
void main() {
  List<String> tasks = ['Login', 'Choose plan'];

  tasks.add('Complete payment');
  print(tasks);

  tasks.remove('Login');
  print(tasks);
}
```

## Access By Index

```dart
void main() {
  List<String> cities = ['Delhi', 'Mumbai', 'Pune'];

  print(cities[1]);
}
```

This prints:

```text
Mumbai
```

## Real-World Example

```dart
void main() {
  List<String> cartItems = ['Laptop', 'Mouse', 'Keyboard'];

  for (String item in cartItems) {
    print('Cart item: $item');
  }
}
```

This is very close to the kind of data loop you use in app development.

## Senior Trick: Use Typed Lists

Prefer:

```dart
List<String> names = ['Asha', 'Ravi'];
```

over weakly typed or unclear lists.

Typed lists make:

- tooling better
- bugs fewer
- code easier to understand

## Common Mistake: Invalid Index Access

```dart
void main() {
  List<String> items = ['A', 'B'];
  print(items[5]);
}
```

This fails because index `5` does not exist.

Remember:

- lists are zero-based
- the first item is index `0`

## Senior Trick: Use `final` For List References When Appropriate

```dart
final List<String> tags = ['dart', 'flutter'];
tags.add('mobile');
```

This keeps the variable reference fixed while still allowing list updates.

That pattern is common in Dart.

## Summary

- a `List` stores ordered items
- lists allow duplicates
- items are accessed by index
- lists are one of the most common tools in real apps

## Flutter Connection

In Flutter, lists are used for:

- rendering repeated widgets
- storing model collections
- working with API result arrays
- handling dynamic content

If you get comfortable with lists, a lot of app logic starts feeling natural.
