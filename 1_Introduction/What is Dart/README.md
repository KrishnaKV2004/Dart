# What Is Dart

## Learning Goal

In this lesson, you will understand what Dart is, why it was created, where it is used, and why it is such a good language for Flutter development.

## Simple Definition

Dart is a modern programming language created by Google. It is designed to build fast, reliable, and maintainable applications.

Dart is especially popular because it is the main language used with Flutter to build:

- Android apps
- iOS apps
- web apps
- desktop apps
- backend and command-line tools

## Why Dart Exists

Every programming language is created to solve certain problems well.

Dart was designed to give developers:

- clean syntax that is easy to read
- good performance
- strong support for object-oriented programming
- modern features like async programming and null safety
- the ability to build cross-platform apps from one codebase

This is one reason Dart works so nicely with Flutter. Flutter needs a language that can describe UI clearly, rebuild screens quickly, and scale well in large apps.

## Dart In One Sentence

Dart is a language that helps developers write expressive code that can run efficiently across many platforms.

## Your First Dart Example

```dart
void main() {
  print('Hello, Dart!');
}
```

## Explanation

### `void`

`void` means the function does not return a value.

### `main()`

`main()` is the entry point of a Dart program. Execution starts here.

### `{ }`

Curly braces define the body of the function.

### `print()`

`print()` displays output in the console.

### `;`

A semicolon ends a statement.

## A Slightly More Real Example

```dart
void main() {
  String userName = 'Asha';
  int cartItems = 3;

  print('Welcome, $userName');
  print('You have $cartItems items in your cart.');
}
```

## What This Teaches

This small program already shows a few important ideas:

- Dart can store data in variables
- Dart supports strings and numbers
- Dart can build readable output using string interpolation

These are the same building blocks you will use later in Flutter apps for:

- user profiles
- shopping carts
- dashboard counters
- form values

## Real-World Analogy

Think of Dart as the language you use to describe how an app should behave.

For example:

- when the user taps a button
- when data is loaded from an API
- when a product is added to a cart
- when a screen should show a loading indicator

Flutter handles the visual side, but Dart handles the logic behind it.

## Dart And Flutter

This is one of the most important ideas to understand early:

Flutter is the UI toolkit.
Dart is the language used to write Flutter apps.

In simple terms:

- Flutter gives you tools to build the interface
- Dart gives you the language to control the app

## Example Of App Logic Written In Dart

```dart
class Counter {
  int value = 0;

  void increment() {
    value++;
  }
}

void main() {
  Counter counter = Counter();

  counter.increment();
  counter.increment();

  print(counter.value);
}
```

## Why This Matters For Flutter

This example introduces object-oriented programming in a simple way.

The `Counter` object stores state and behavior:

- state: `value`
- behavior: `increment()`

Later in Flutter, many app features are built around this same idea:

- a `User` object
- a `Product` object
- a `Cart` object
- a `Message` object

So when you learn OOP in Dart, you are also preparing for app architecture in Flutter.

## Where Dart Can Run

Dart can be used in multiple environments:

- command-line applications
- backend services
- web applications
- Flutter mobile apps
- Flutter desktop apps

## Example: Same Thinking Across Platforms

```dart
class User {
  String name;
  bool isLoggedIn;

  User(this.name, this.isLoggedIn);
}

void main() {
  User user = User('Riya', true);

  if (user.isLoggedIn) {
    print('${user.name} can access the dashboard.');
  } else {
    print('${user.name} must log in first.');
  }
}
```

This kind of logic works whether you are writing:

- a console app
- a web app
- a Flutter app

That is why learning pure Dart first is so powerful.

## Why Beginners Often Like Dart

Dart is often easier to learn than many other languages because:

- its syntax is readable
- it feels consistent
- it supports both beginner-friendly and advanced patterns
- it gives useful compile-time checks

You can start with small programs and gradually grow into professional app development.

## Key Idea: Dart Is Not Just Syntax

Many beginners think learning a language means memorizing keywords.
That is not enough.

Learning Dart really means learning how to model real problems in code.

For example:

- represent a user
- validate login input
- fetch data from a server
- update screen state
- organize app logic using classes and functions

## Mini Practice

Try to predict the output before running this:

```dart
void main() {
  String appName = 'Task Planner';
  int totalTasks = 5;
  bool isPremiumUser = true;

  print('App: $appName');
  print('Tasks: $totalTasks');
  print('Premium: $isPremiumUser');
}
```

## Expected Output

```text
App: Task Planner
Tasks: 5
Premium: true
```

## Summary

- Dart is a modern programming language by Google
- it is the main language used with Flutter
- it supports building apps for multiple platforms
- it is clean, fast, and good for both beginners and professionals
- learning Dart well helps you build stronger Flutter apps later

## Flutter Connection

When you later build Flutter apps, Dart will be used for:

- widget logic
- state handling
- API calls
- models and classes
- validation and business rules

That is why this language is worth understanding deeply from the start.
