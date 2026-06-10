# await

## Learning Goal

In this lesson, you will learn how `await` pauses execution until a future is complete.

## What Does `await` Do

`await` waits for a future to finish and gives you the completed result.

It can only be used inside an `async` function.

## Basic Example

```dart
Future<String> loadName() async {
  return 'Asha';
}

Future<void> main() async {
  String name = await loadName();
  print(name);
}
```

The code waits for the result before continuing.

## Why This Is Useful

`await` makes async code much easier to read.

Instead of manually handling futures everywhere, you can write logic that looks almost synchronous.

## Real-World Example

```dart
Future<void> saveData() async {
  await Future.delayed(const Duration(seconds: 1));
  print('Data saved');
}
```

This reads in the order the work happens.

## Senior Trick: Await The Right Thing

Do not forget that `await` pauses only the current async function.

That means the structure of your code matters when you want work to happen in sequence.

## Senior Trick: Use `await` To Improve Readability, Not To Hide Flow

`await` makes code easier to read, but you still need to understand the timing.

Always ask what happens before, during, and after the wait.

## Summary

- `await` waits for a future
- it can only be used inside `async`
- it makes async code easier to read
- it helps you write sequential-looking logic

## Flutter Connection

`await` is everywhere in Flutter for API calls, local storage, initialization, and async event handling.
