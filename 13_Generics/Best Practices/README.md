# Best Practices

## Learning Goal

In this lesson, you will learn how to use generics in a way that improves code quality instead of making code harder to understand.

## What Good Generic Code Looks Like

Good generic code is:

- type-safe
- easy to read
- focused on one job
- reusable for the right reasons

The goal is not to make everything generic.
The goal is to make the right things generic.

## Basic Example

```dart
class Pair<T> {
  final T first;
  final T second;

  Pair(this.first, this.second);
}
```

This is simple, clear, and useful because the shape is stable while the value type changes.

## Common Best Practices

### 1. Use Meaningful Type Names

`T` is fine for a single general type parameter.

For more descriptive cases, use names like:

- `T`
- `E`
- `K`
- `V`

These are standard and easy to understand.

### 2. Prefer Type Inference When It Is Clear

Let Dart infer the type when the code remains easy to read.

Too many explicit type arguments can make code noisy.

### 3. Avoid `dynamic` When Generics Will Do

`dynamic` removes type safety.

Generics keep the compiler helpful while still allowing flexibility.

### 4. Do Not Over-Generalize

If a class or function only ever works with one type, making it generic may add unnecessary complexity.

### 5. Add Constraints When Needed

If the type must support a capability, express that requirement with a constraint instead of hoping for the best.

## Senior Trick: Generic Does Not Mean Better

Some developers make code generic too early.

That can hide the real design and make simple logic harder to follow.

Use generics when they genuinely improve reuse, safety, or clarity.

## Senior Trick: Design For The Call Site

A good generic API should feel natural when someone uses it.

If the call site becomes confusing, the generic design may need to be simpler.

## Summary

- use generics when the type is part of the design
- keep generic APIs readable
- use constraints when a type needs specific capabilities
- avoid overusing generics when simple code is enough

## Flutter Connection

Generics are essential in Flutter code, but the best Flutter code still stays readable.

Use them for:

- models
- repositories
- collections
- helper utilities

Use them carefully so the app stays maintainable as it grows.
