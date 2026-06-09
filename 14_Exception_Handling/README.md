# Lesson 14: Exception Handling

This section teaches how to handle runtime problems safely so your Dart programs can fail in a controlled and understandable way.

Exception handling is a core skill because real code does not always get perfect input, perfect data, or perfect network conditions.

## Topics In This Lesson

1. [Exceptions](./Exceptions/README.md)
2. [throw](./throw/README.md)
3. [try](./try/README.md)
4. [catch](./catch/README.md)
5. [on](./on/README.md)
6. [finally](./finally/README.md)
7. [Custom Exceptions](./Custom%20Exceptions/README.md)
8. [Error Handling Patterns](./Error%20Handling%20Patterns/README.md)

## Why This Lesson Matters

Programs fail for many reasons:

- invalid input
- missing data
- network issues
- file problems
- unexpected runtime values

If you do not handle those cases, your app can crash or behave in confusing ways.

Exception handling helps you respond with control instead of panic.

## Senior Developer Mindset For Exception Handling

Strong developers do not try to hide failures.
They design for them.

A good rule is:

- handle expected problems gracefully
- let truly unexpected failures be visible
- keep error handling close to the point of failure when possible
- avoid swallowing exceptions silently

Good exception handling makes systems easier to trust and debug.

## What You Should Learn Here

By the end of this section, you should be able to:

- recognize what exceptions are
- use `throw` to signal failures
- wrap risky code in `try` blocks
- handle exceptions with `catch` and `on`
- clean up resources with `finally`
- create custom exception types
- apply practical error handling patterns

## Real-World Example

```dart
void main() {
  try {
    int age = int.parse('not a number');
    print(age);
  } catch (e) {
    print('Invalid input: $e');
  }
}
```

This keeps the program from crashing immediately when parsing fails.

## Senior Trick: Treat Exceptions As Part Of The Design

Exception handling should not be an afterthought.

It should answer questions like:

- what can fail here?
- who should handle the failure?
- what message should the user see?
- what cleanup must happen no matter what?

That mindset leads to cleaner, safer code.

## Summary

- exceptions represent runtime problems
- `throw` creates failures intentionally
- `try` and `catch` let you handle risky code safely
- `finally` runs cleanup code
- custom exceptions and patterns improve clarity

## Flutter Connection

Exception handling is very important in Flutter for:

- form validation
- API requests
- JSON parsing
- file access
- asynchronous operations

If you handle exceptions well, Flutter apps feel more stable and professional.
