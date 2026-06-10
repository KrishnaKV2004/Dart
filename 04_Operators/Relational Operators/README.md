# Relational Operators

## Learning Goal

In this lesson, you will learn how to compare values in Dart and use those comparisons to drive application decisions.

## What Are Relational Operators

Relational operators compare two values and return a `bool`:

- `==`
- `!=`
- `>`
- `<`
- `>=`
- `<=`

## Basic Example

```dart
void main() {
  int age = 20;

  print(age == 20);
  print(age != 18);
  print(age > 18);
  print(age < 30);
  print(age >= 20);
  print(age <= 25);
}
```

## Why They Matter

Most real application behavior depends on comparisons.

Examples:

- Is the user old enough?
- Is stock greater than zero?
- Is the password length valid?
- Is the order total above the free-shipping threshold?

## Real-World Example

```dart
void main() {
  double orderTotal = 2500;

  if (orderTotal >= 2000) {
    print('Free delivery available');
  } else {
    print('Delivery charges apply');
  }
}
```

## Senior Trick: Compare Business Rules, Not Just Numbers

Try to make comparisons read like the domain.

Good:

```dart
bool qualifiesForFreeShipping = orderTotal >= 2000;
```

Less expressive:

```dart
bool result = orderTotal >= 2000;
```

The first version explains the intent.

## `==` Versus `=`

This is a very common beginner mistake.

- `=` assigns a value
- `==` compares values

Correct:

```dart
bool isAdmin = true;
print(isAdmin == true);
```

## Summary

- relational operators compare values
- comparisons return `true` or `false`
- they are central to business rules and validation
- descriptive boolean variables make comparison logic clearer

## Flutter Connection

Relational operators are used constantly in Flutter for:

- showing or hiding widgets
- validating input
- checking list lengths
- controlling button states

Understanding them well makes UI behavior easier to reason about.
