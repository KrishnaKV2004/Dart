# Lesson 15: Asynchronous Programming

This section teaches how to work with tasks that do not finish immediately, such as network requests, file access, and stream-based data.

Asynchronous programming is essential in Dart because real apps often need to keep running while other work happens in the background.

## Topics In This Lesson

1. [Futures](./Futures/README.md)
2. [async](./async/README.md)
3. [await](./await/README.md)
4. [Future Chaining](./Future%20Chaining/README.md)
5. [Streams](./Streams/README.md)
6. [Stream Controllers](./Stream%20Controllers/README.md)
7. [Async Generators](./Async%20Generators/README.md)
8. [Error Handling](./Error%20Handling/README.md)
9. [Isolates](./Isolates/README.md)

## Why This Lesson Matters

Not every task in a program is instant.

Some work takes time:

- fetching API data
- reading files
- waiting for user input
- processing streams of events
- doing heavy computation

If you write all of that synchronously, your app can freeze or become difficult to use.

## Senior Developer Mindset For Async Code

Strong developers think carefully about timing, not just syntax.

A good rule is:

- use async code when the operation is not immediate
- keep async flows easy to read
- avoid nesting too deeply
- handle errors intentionally
- separate UI work from background work when needed

Good async code feels calm and predictable.

## What You Should Learn Here

By the end of this section, you should be able to:

- understand what futures represent
- use `async` and `await`
- chain future operations cleanly
- work with streams and controllers
- generate values asynchronously
- handle async errors properly
- recognize when isolates are useful

## Real-World Example

```dart
Future<String> fetchUserName() async {
  await Future.delayed(const Duration(seconds: 1));
  return 'Asha';
}

void main() async {
  String name = await fetchUserName();
  print(name);
}
```

This simulates work that finishes later instead of immediately.

## Senior Trick: Read Async Code As A Timeline

When you read async code, do not just read the lines.

Think about:

- what starts now
- what pauses
- what resumes later
- what can fail

That habit makes async code much easier to reason about.

## Summary

- async programming handles work that finishes later
- futures represent a value available in the future
- `async` and `await` make async code easier to read
- streams handle multiple values over time
- isolates help with heavy work

## Flutter Connection

Asynchronous programming is everywhere in Flutter:

- API calls
- loading data
- stream updates
- animations and timers
- state updates after async work

If you understand async Dart well, Flutter becomes much easier to build and debug.
