# Named Parameters

## Learning Goal

In this lesson, you will learn how named parameters make function calls clearer and safer.

## What Are Named Parameters

Named parameters let you pass arguments by name instead of only by position.

They are written inside curly braces in the function definition.

## Basic Example

```dart
void createUser({
  required String name,
  required int age,
}) {
  print('Name: $name');
  print('Age: $age');
}

void main() {
  createUser(name: 'Karan', age: 25);
}
```

## Why Named Parameters Are So Useful

They make function calls self-explanatory.

Compare:

```dart
createUser('Karan', 25);
```

with:

```dart
createUser(name: 'Karan', age: 25);
```

The second version is clearer, especially as functions grow.

## Real-World Example

```dart
void createOrder({
  required String productName,
  required int quantity,
  required double price,
}) {
  print('Product: $productName');
  print('Quantity: $quantity');
  print('Price: $price');
}
```

## Senior Trick: Prefer Named Parameters When Meaning Matters More Than Order

Named parameters are especially helpful when:

- several arguments have similar types
- call sites should read like a sentence
- you want to reduce argument-order mistakes

## Required Named Parameters

Use `required` when the caller must provide the value.

This gives the clarity of names without losing safety.

## Summary

- named parameters are passed by name
- they improve readability and reduce mistakes
- `required` makes important named parameters mandatory

## Flutter Connection

Named parameters are everywhere in Flutter:

- widget constructors
- style configuration
- helper methods

Mastering them now gives you a huge advantage later.
