# Functional Patterns

## Learning Goal

In this lesson, you will learn how to recognize and use common functional programming patterns in Dart.

## What Is A Functional Pattern

A functional pattern is a repeatable way of using functions and collection helpers to transform, filter, check, or summarize data.

## Common Patterns

### 1. Transform Data

Use `map()` to change each item into a new form.

### 2. Filter Data

Use `where()` to keep only the items that match a rule.

### 3. Check Conditions

Use `any()` and `every()` to ask yes/no questions about a collection.

### 4. Combine Results

Use `fold()` or `reduce()` to turn many items into one result.

### 5. Compose Small Functions

Keep functions focused so they can be reused in pipelines.

## Real-World Example

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];

  int totalOfEvenSquares = numbers
      .where((n) => n % 2 == 0)
      .map((n) => n * n)
      .fold(0, (sum, n) => sum + n);

  print(totalOfEvenSquares);
}
```

This filters, transforms, and combines the data in one clear flow.

## Senior Trick: Prefer Small Pipelines Over Big Loops When It Improves Clarity

A well-shaped pipeline can be easier to read than a manual loop because each step has a clear purpose.

## Senior Trick: Do Not Chain So Much That The Intent Gets Lost

Pipelines are useful, but they can become hard to read if too many steps are squeezed together.

If that happens, break the flow into named intermediate values.

## Summary

- functional patterns help structure data flow
- `map`, `where`, `any`, `every`, `fold`, and `reduce` cover many common tasks
- small, readable pipelines are often a good design choice
- clarity should guide the style

## Flutter Connection

Functional patterns are everywhere in Flutter for building UI lists, deriving state, and transforming data before display.
