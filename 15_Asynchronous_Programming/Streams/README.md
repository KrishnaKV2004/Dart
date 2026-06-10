# Streams

## Learning Goal

In this lesson, you will learn what streams are and why they are used for multiple values over time.

## What Is A Stream

A stream is a sequence of asynchronous events.

Unlike a future, which gives one result later, a stream can deliver many values over time.

## Basic Example

```dart
Stream<int> countNumbers() async* {
  yield 1;
  yield 2;
  yield 3;
}
```

This stream produces multiple values.

## Why Streams Matter

Streams are useful when data arrives repeatedly, such as:

- user input events
- live updates
- sensor data
- socket messages
- progress updates

## Real-World Example

```dart
Stream<String> chatMessages() async* {
  yield 'Hello';
  yield 'How are you?';
  yield 'See you soon';
}
```

This models a flow of messages over time.

## Senior Trick: Use Streams When The Data Is Ongoing

Do not force everything into a stream.

If the result is a single response, a future is usually simpler.

Use streams when the data naturally changes over time.

## Senior Trick: Think In Events, Not Just Values

Streams are about ongoing events.

That mindset helps you design better UI updates and data flows.

## Summary

- streams deliver multiple values over time
- they are asynchronous sequences
- they are useful for event-driven data
- they are different from futures

## Flutter Connection

Streams are common in Flutter for text changes, app events, live data, and reactive state.
