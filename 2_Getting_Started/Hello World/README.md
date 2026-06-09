# Hello World

## Learning Goal

In this lesson, you will write your first Dart program, understand every part of it, and learn why even a tiny example is useful.

## The Classic First Program

```dart
void main() {
  print('Hello, World!');
}
```

## Output

```text
Hello, World!
```

## Line-By-Line Explanation

### `void`

`void` means this function does not return a value.

### `main()`

`main()` is the entry point of a Dart program.
When Dart runs your file, it starts here.

### `{ }`

Curly braces mark the body of the function.
Everything inside them belongs to `main()`.

### `print()`

`print()` displays text in the console.

### `;`

A semicolon ends a statement.

## Why "Hello World" Still Matters

Beginners sometimes think this program is too simple to matter.
Actually, it proves several important things:

- your Dart installation works
- your file is valid
- your editor is saving correctly
- your terminal command is working
- you understand where execution starts

That is why experienced developers also start small when testing a new environment.

## First Senior Trick: Use Tiny Programs To Isolate Problems

If your bigger program is not working, reduce it to the smallest possible example.

For example:

```dart
void main() {
  print('Test');
}
```

If this runs, your environment is fine and the issue is inside your larger code.

That habit saves a lot of time in real projects.

## Try Small Variations

### Example 1

```dart
void main() {
  print('Hello, Dart!');
}
```

### Example 2

```dart
void main() {
  print('Welcome to learning Dart.');
  print('This is my first program.');
}
```

### Example 3

```dart
void main() {
  String name = 'Rohan';
  print('Hello, $name');
}
```

## What You Are Already Learning

Even in the examples above, you are touching:

- functions
- strings
- variables
- string interpolation

This is why small programs are powerful.

## Real-World Scenario

Suppose you are starting a Flutter app later.
Before building UI, you may first test a business rule in plain Dart:

```dart
void main() {
  double price = 999.0;
  double discount = 100.0;

  print('Final price: ${price - discount}');
}
```

Strong developers often test logic in small, plain Dart examples before placing it inside widgets or app layers.

## Common Beginner Mistakes

### Missing semicolon

```dart
void main() {
  print('Hello')
}
```

This causes an error because the statement is not properly ended.

### Wrong quotes

```dart
void main() {
  print(Hello, World!);
}
```

Text must be inside quotes.

### Wrong entry point name

```dart
void start() {
  print('Hello');
}
```

This defines a function, but Dart normally looks for `main()` as the starting point.

## Senior Trick: Read Error Messages From Top To Bottom

When a program fails:

1. read the first error first
2. do not panic over multiple errors
3. fix the earliest error
4. run again

Often one mistake causes many follow-up errors.

## A Better First Example

```dart
void main() {
  String learnerName = 'Aditi';
  int practiceDay = 1;

  print('Hello, $learnerName');
  print('Today is practice day $practiceDay.');
}
```

## Why This Is Better For Learning

This still stays simple, but it introduces:

- naming variables clearly
- separating output into readable lines
- writing code that feels more like a real program

## Mini Practice

Write a program that prints:

```text
App Name: Budget Tracker
Version: 1
Status: Learning Mode
```

One possible answer:

```dart
void main() {
  print('App Name: Budget Tracker');
  print('Version: 1');
  print('Status: Learning Mode');
}
```

## Summary

- `main()` is where a Dart program starts
- `print()` shows output in the console
- small programs are useful for learning and debugging
- even simple examples can teach important habits

## Flutter Connection

In Flutter, you will still rely on the same mindset:

- start small
- verify behavior often
- isolate logic before scaling it

That is a senior habit worth keeping from day one.
