# DartPad

## Learning Goal

In this lesson, you will learn what DartPad is, when to use it, and how to use it effectively for fast practice and experimentation.

## What Is DartPad

DartPad is an online editor for Dart.
It lets you write and run Dart code in the browser without installing anything.

This is especially useful for:

- beginners starting quickly
- testing small examples
- sharing code snippets
- experimenting with syntax

## Why DartPad Is So Useful

DartPad removes setup friction.
That means you can focus on learning concepts first.

Instead of thinking:

- "Did I install everything correctly?"

you can think:

- "What does this code do?"

## First Example In DartPad

```dart
void main() {
  print('Learning Dart with DartPad');
}
```

This makes DartPad perfect for your first exercises.

## What DartPad Is Best For

- basic syntax practice
- trying variables and operators
- testing conditions and loops
- sharing examples with others
- learning concepts quickly

## What DartPad Is Not Best For

DartPad is not ideal for:

- large multi-file projects
- full package-based workflows
- deep project structure practice
- long-term app organization

So think of DartPad as a fast lab, not your final workspace.

## Senior Trick: Use DartPad To Test Ideas Before Editing Bigger Code

Experienced developers often isolate logic in a tiny environment first.

For example, before putting logic inside a Flutter widget, you can test the pure Dart part in a small snippet.

Example:

```dart
void main() {
  double originalPrice = 1200;
  double discount = 10;

  double finalPrice = originalPrice - (originalPrice * discount / 100);

  print('Final price: $finalPrice');
}
```

If the logic works here, moving it into a larger app becomes safer.

## Example: Testing User Logic

```dart
class User {
  String name;
  bool isActive;

  User(this.name, this.isActive);
}

void main() {
  User user = User('Nina', true);

  if (user.isActive) {
    print('${user.name} can access the app.');
  } else {
    print('${user.name} is blocked.');
  }
}
```

This is a great example of learning OOP in a lightweight way.

## Why This Matters For Flutter

A lot of Flutter development becomes easier when you can first test:

- class design
- validation logic
- calculations
- conditional behavior

in plain Dart.

DartPad is excellent for that.

## Example: Safe Experimentation

Try changing values in this code:

```dart
void main() {
  int cartItems = 2;
  bool hasCoupon = true;

  if (cartItems > 0 && hasCoupon) {
    print('Apply discount');
  } else {
    print('Normal checkout');
  }
}
```

Change:

- `cartItems`
- `hasCoupon`

Then predict the output before running.

That is how you build real understanding.

## Senior Trick: Use DartPad For Micro-Learning

When learning a new feature, create the smallest possible demo.

Examples:

- one program only for `if`
- one program only for `List`
- one program only for classes

This keeps your brain focused on one idea at a time.

## Common Beginner Mistake

Some learners treat DartPad like only a playground for random code.

A better approach is to use it intentionally:

- one concept
- one small example
- one question to answer

For example:

- "What happens if this variable is nullable?"
- "How does string interpolation work?"
- "What if I change this `if` condition?"

That makes DartPad a serious learning tool.

## Mini Practice

Write and run this:

```dart
void main() {
  String appName = 'Task Manager';
  int totalTasks = 4;

  print('App: $appName');
  print('Tasks today: $totalTasks');
}
```

Then modify it to:

- change the app name
- add one more `print()`
- replace the number with another value

## Summary

- DartPad lets you run Dart in the browser
- it is ideal for quick practice and tiny experiments
- it is especially useful for testing logic before scaling it
- strong developers use small sandboxes to validate ideas quickly

## Flutter Connection

Later in Flutter, you can use DartPad-like thinking to isolate:

- business rules
- class behavior
- conditional logic
- calculations

before mixing them into UI code.
