# Optional Parameters

## Learning Goal

In this lesson, you will learn what optional parameters are and how they make functions more flexible.

## What Are Optional Parameters

Optional parameters are parameters that do not always need to be provided when the function is called.

In Dart, optional positional parameters are written inside square brackets.

## Basic Example

```dart
void greetUser(String name, [String? title]) {
  if (title != null) {
    print('Hello, $title $name');
  } else {
    print('Hello, $name');
  }
}

void main() {
  greetUser('Riya');
  greetUser('Riya', 'Dr.');
}
```

## Why Optional Parameters Matter

Sometimes a function has:

- required core data
- extra data that is nice to have

Optional parameters let you support both cases.

## Real-World Example

```dart
void createNotification(String message, [String? priority]) {
  print('Message: $message');
  print('Priority: ${priority ?? 'normal'}');
}

void main() {
  createNotification('Backup completed');
  createNotification('Server offline', 'high');
}
```

## Senior Trick: Use Optional Parameters For Genuine Optional Meaning

Do not make parameters optional just to avoid thinking about function design.

Ask:

- Is this information truly optional?
- Does the function still make sense without it?

If yes, optional parameters may be a good fit.

## Summary

- optional parameters do not always need to be passed
- they make functions more flexible
- use them only when the argument is genuinely optional

## Flutter Connection

Optional parameters are useful in Flutter when helper methods or components can work in a basic form but also support extra configuration.
