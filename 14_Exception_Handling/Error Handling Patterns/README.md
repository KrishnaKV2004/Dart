# Error Handling Patterns

## Learning Goal

In this lesson, you will learn practical patterns for handling errors cleanly in real Dart code.

## What Is An Error Handling Pattern

An error handling pattern is a repeatable way of dealing with failures in a clear, safe, and maintainable way.

## Common Patterns

### 1. Fail Fast

Stop early when the input or state is invalid.

This prevents bad data from spreading through the program.

### 2. Validate Before You Act

Check data before doing the risky operation.

This is often better than catching a failure after the fact.

### 3. Catch Close To The Source

Handle the exception near the code that can actually recover from it.

That keeps logic easier to follow.

### 4. Rethrow With Context

Sometimes you catch a low-level exception and rethrow a more meaningful one.

That helps higher layers understand the failure better.

### 5. Use `finally` For Cleanup

If a resource must always be released or reset, put that in `finally`.

## Real-World Example

```dart
String safeParse(String value) {
  try {
    return int.parse(value).toString();
  } catch (e) {
    return '0';
  }
}
```

This is a simple fallback pattern.

## Senior Trick: Do Not Swallow Exceptions Silently

If you catch an error and do nothing, you may hide bugs and make debugging much harder.

At minimum, be intentional about:

- logging
- fallback behavior
- rethrowing
- returning a safe result

## Senior Trick: Match The Pattern To The Layer

Different layers often need different responses:

- UI layer: show a friendly message
- service layer: transform or rethrow
- low-level utility: validate or fail fast

Good architecture uses the right response at the right level.

## Summary

- error handling patterns make failure handling repeatable
- validate early when possible
- catch where recovery makes sense
- rethrow with context when needed
- avoid silent failures

## Flutter Connection

These patterns are very important in Flutter apps for forms, repositories, services, and async network flows.
