# Variables

## Learning Goal

In this lesson, you will learn what variables are, why they matter, and how to use them clearly in real Dart programs.

## What Is A Variable

A variable is a named place in memory that stores a value.

You use variables when your program needs to remember something, such as:

- a user's name
- a product price
- a login state
- a score

## Basic Example

```dart
void main() {
  String userName = 'Aarav';
  int age = 21;

  print(userName);
  print(age);
}
```

## Explanation

### `String userName`

This creates a variable named `userName` that stores text.

### `int age`

This creates a variable named `age` that stores a whole number.

### `=`

This assigns a value to the variable.

## Why Variables Matter

Without variables, you would have to repeat raw values everywhere:

```dart
void main() {
  print('Aarav');
  print('Aarav');
  print('Aarav');
}
```

That is hard to maintain.

With a variable:

```dart
void main() {
  String userName = 'Aarav';

  print(userName);
  print(userName);
  print(userName);
}
```

Now you only update the value once if it changes.

## Real-World Example

```dart
void main() {
  String productName = 'Wireless Mouse';
  double price = 899.0;
  bool inStock = true;

  print('Product: $productName');
  print('Price: $price');
  print('Available: $inStock');
}
```

This is already similar to the data you would handle in an app or API.

## Senior Trick: Name Variables By Meaning, Not By Type

Weak:

```dart
String s = 'Ravi';
int x = 5;
```

Better:

```dart
String customerName = 'Ravi';
int cartItemCount = 5;
```

Good variable names reduce confusion and reduce the need for comments.

## Variables Can Change

```dart
void main() {
  int score = 10;
  print(score);

  score = 20;
  print(score);
}
```

## Output

```text
10
20
```

This is useful when values naturally change during the program.

Examples:

- cart total updates
- score changes
- page number changes
- quantity increases

## Common Beginner Mistakes

### Using unclear names

```dart
int a = 10;
```

### Mixing the wrong type

```dart
int age = '21';
```

This is invalid because `'21'` is text, not an integer.

### Reusing one variable for unrelated meanings

```dart
dynamic value = 'Riya';
value = 99;
value = true;
```

Technically possible in some cases, but usually bad design for beginner code.

## Senior Trick: Keep Variable Scope Small

Declare variables close to where they are used.

```dart
void showInvoice() {
  double subtotal = 1200;
  double tax = 216;
  double total = subtotal + tax;

  print(total);
}
```

This is usually better than scattering shared variables everywhere without reason.

## Mini Practice

Write a program that stores:

- app name
- current version
- number of users online

One possible answer:

```dart
void main() {
  String appName = 'TaskFlow';
  String version = '1.0.0';
  int usersOnline = 145;

  print('App: $appName');
  print('Version: $version');
  print('Online users: $usersOnline');
}
```

## Summary

- variables store values
- each variable should have a clear purpose
- strong naming improves readability
- variables make programs flexible and maintainable

## Flutter Connection

In Flutter, variables are used everywhere:

- widget titles
- form values
- loading flags
- counters
- user and product data

Understanding variables well is one of the first steps toward clean app logic.
