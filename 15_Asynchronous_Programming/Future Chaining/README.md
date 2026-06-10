# Future Chaining

## Learning Goal

In this lesson, you will learn how to connect multiple future steps together in a clean flow.

## What Is Future Chaining

Future chaining means taking the result of one future and using it to continue with the next step.

This is often done with `then`, `catchError`, and `whenComplete`.

## Basic Example

```dart
Future<String> getName() {
  return Future.value('Asha');
}

void main() {
  getName()
      .then((name) => print('Name: $name'))
      .catchError((error) => print('Error: $error'));
}
```

The next action depends on the previous future result.

## Why This Is Useful

Chaining helps you build pipelines of async work.

It is useful when:

- one operation depends on another
- you want a clear sequence of async steps
- you want to handle errors in one flow

## Real-World Example

```dart
Future<String> fetchUser() {
  return Future.value('User loaded');
}

Future<void> main() {
  fetchUser()
      .then((value) => print(value))
      .whenComplete(() => print('Done'));
}
```

This keeps the async flow connected from start to finish.

## Senior Trick: Prefer The Style That Reads Best

For many cases, `async` and `await` are easier to understand than deep chaining.

Use chaining when it genuinely makes the flow clearer or matches the API style.

## Senior Trick: Handle Errors Deliberately In The Chain

When chaining futures, always think about where failures should be handled.

Otherwise the flow can become hard to debug.

## Summary

- future chaining connects async steps
- it often uses `then`, `catchError`, and `whenComplete`
- it is useful for pipelines and event flows
- readability should guide the choice of style

## Flutter Connection

Future chaining appears in Flutter when working with async utilities, service layers, and stream/future transformations.
