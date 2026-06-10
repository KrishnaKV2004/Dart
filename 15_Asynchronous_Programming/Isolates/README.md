# Isolates

## Learning Goal

In this lesson, you will learn what isolates are and why they matter for heavy asynchronous work in Dart.

## What Is An Isolate

An isolate is a separate execution unit with its own memory and event loop.

It is used when you want work to happen without blocking the main thread of execution.

## Basic Idea

Dart uses isolates to separate expensive computation from the main flow.

This helps keep apps responsive.

## Why Isolates Matter

Isolates are useful for:

- heavy computation
- CPU-intensive parsing
- background processing
- keeping UI responsive

## Real-World Example

```dart
void main() {
  print('Main work starts');
  print('Heavy work should be isolated when needed');
}
```

This example shows the idea, even though real isolate code would be more involved.

## Senior Trick: Use Isolates For CPU Work, Not Everything

Isolates are powerful, but they are not the answer for every async problem.

Use them when the work is heavy enough to justify the extra complexity.

## Senior Trick: Keep The Main Flow Responsive

The main goal is not just background work.

The goal is to keep the app responsive and predictable while the expensive work happens elsewhere.

## Summary

- isolates are separate execution units
- they help with heavy CPU work
- they protect responsiveness
- they are more advanced than ordinary futures and streams

## Flutter Connection

Isolates matter in Flutter when you need to keep the UI smooth during expensive computation, large parsing jobs, or background processing.
