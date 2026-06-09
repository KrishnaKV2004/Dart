# finally

## Learning Goal

In this lesson, you will learn how to use `finally` for cleanup code that must run no matter what happens.

## What Does `finally` Do

The `finally` block runs after `try` and `catch`, whether an exception happened or not.

## Basic Example

```dart
void main() {
  try {
    print(int.parse('abc'));
  } catch (e) {
    print('Failed to parse');
  } finally {
    print('Cleanup finished');
  }
}
```

The `finally` block runs even after the failure.

## Why This Is Useful

`finally` is ideal for cleanup tasks such as:

- closing resources
- resetting state
- stopping loading indicators
- releasing temporary locks

## Real-World Example

```dart
void main() {
  bool loading = true;

  try {
    print('Running task...');
  } catch (e) {
    print('Task failed');
  } finally {
    loading = false;
    print('Loading is now $loading');
  }
}
```

The cleanup step happens regardless of success or failure.

## Senior Trick: Put Cleanup In `finally`, Not Business Logic

`finally` should be for things that must always happen.

It should not be used to hide normal logic that belongs elsewhere.

## Senior Trick: Think About Resource Safety

Any time code opens, creates, or reserves something, ask what must happen if an exception interrupts the flow.

That is where `finally` becomes valuable.

## Summary

- `finally` runs whether an exception happens or not
- it is best for cleanup work
- it helps keep code resource-safe
- it should stay focused on cleanup

## Flutter Connection

In Flutter, `finally` is often useful for stopping spinners, resetting flags, or cleaning up work after async operations.
