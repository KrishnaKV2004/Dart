# async

## Learning Goal

In this lesson, you will learn how `async` marks a function as asynchronous.

## What Does `async` Do

The `async` keyword tells Dart that a function may pause while waiting for a future.

It also lets the function use `await` inside its body.

## Basic Example

```dart
Future<String> greet() async {
  return 'Hello';
}
```

Even though this function returns immediately here, `async` makes it return a `Future`.

## Why This Is Useful

`async` makes it easier to write code that matches real-world timing.

You can write logic in a natural top-to-bottom style instead of deeply nesting callbacks.

## Real-World Example

```dart
Future<void> fetchProfile() async {
  print('Loading profile...');
  await Future.delayed(const Duration(seconds: 1));
  print('Profile loaded');
}
```

This is the kind of structure you use when work completes later.

## Senior Trick: Use `async` Only When The Function Really Needs It

Do not add `async` by habit.

If the function does not await anything, it may be simpler as a normal function.

## Senior Trick: Keep The Async Boundary Clear

Once a function becomes async, think about how its caller should handle the returned future.

That boundary is part of the API design.

## Summary

- `async` marks a function as asynchronous
- it allows the use of `await`
- it returns a `Future`
- it helps make async logic readable

## Flutter Connection

In Flutter, `async` appears in data loading, button handlers, initialization flows, and repository methods.
