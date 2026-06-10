# Error Handling

## Learning Goal

In this lesson, you will learn how to handle errors properly in asynchronous code.

## Why Async Error Handling Matters

Async failures can happen later than the code that started the work.

That means you need to think carefully about where the error will be caught and how it will be reported.

## Basic Example

```dart
Future<void> loadData() async {
  try {
    throw Exception('Network failed');
  } catch (e) {
    print('Failed: $e');
  }
}
```

The error is handled inside the async flow.

## Common Async Error Cases

- failed network requests
- parsing errors
- timeout issues
- stream errors
- task cancellation or interruption

## Real-World Example

```dart
Future<String> fetchUser() async {
  try {
    return 'Asha';
  } catch (e) {
    return 'Guest';
  }
}
```

This gives the caller a fallback value.

## Senior Trick: Handle Errors Where Recovery Is Possible

If the current layer cannot recover, it may be better to rethrow or pass the error upward.

That keeps responsibilities clear.

## Senior Trick: Do Not Ignore Async Failures

Ignoring errors in async code can make bugs feel random and hard to reproduce.

Always decide whether you are logging, recovering, rethrowing, or surfacing the issue.

## Summary

- async error handling needs careful placement
- errors can happen later than expected
- handle where recovery is possible
- avoid silent async failures

## Flutter Connection

Async error handling is critical in Flutter for repositories, network calls, streams, and background tasks.
