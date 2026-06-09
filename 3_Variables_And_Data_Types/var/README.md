# var

## Learning Goal

In this lesson, you will learn what `var` means, how it relates to type inference, and how to use it clearly without making code vague.

## What Is `var`

`var` tells Dart:

- create a variable
- infer its type from the assigned value

## Basic Example

```dart
void main() {
  var name = 'Sana';
  var age = 24;

  print(name);
  print(age);
}
```

Here:

- `name` becomes `String`
- `age` becomes `int`

## Important Rule

Even though you wrote `var`, Dart still infers a type.

So this is not valid:

```dart
void main() {
  var age = 24;
  age = 'twenty four';
}
```

Because `age` was inferred as `int`.

## Why `var` Is Useful

It reduces noise when the type is obvious.

Example:

```dart
var totalUsers = 150;
var city = 'Pune';
```

These are easy to understand without repeating the type.

## When `var` Is Good

- the type is obvious from the right side
- the variable is local and easy to understand
- using the full type would add little value

## When Explicit Types Are Better

If the meaning is not obvious, explicit types can improve readability.

Example:

```dart
final result = fetchSomething();
```

Depending on context, this may be less clear than:

```dart
final String result = fetchSomething();
```

## Senior Trick: Use `var` For Clarity, Not For Laziness

The question is not:

- "Can I shorten this?"

The question is:

- "Will the reader still understand this easily?"

If yes, `var` is fine.
If no, prefer the explicit type.

## Example

Good:

```dart
var itemCount = 5;
var userName = 'Nikhil';
```

Less clear:

```dart
var response = processData();
```

Better:

```dart
Map<String, dynamic> response = processData();
```

if the exact type helps understanding.

## Summary

- `var` lets Dart infer the type
- it does not mean the variable can become any type
- use it when the type is already obvious
- prefer explicit types when they improve readability

## Flutter Connection

In Flutter, `var` is common for local variables in build methods and helper logic, but the best Flutter code still values clarity over shortness.
