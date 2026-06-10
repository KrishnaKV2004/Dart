# Lesson 16: Functional Programming

This section teaches how to use functions as values and how to write code that transforms data in a clean, predictable way.

Functional programming ideas show up everywhere in Dart, especially when working with collections, callbacks, and data pipelines.

## Topics In This Lesson

1. [First Class Functions](./First%20Class%20Functions/README.md)
2. [Closures](./Closures/README.md)
3. [`map()`](./map%28%29/README.md)
4. [`where()`](./where%28%29/README.md)
5. [`any()`](./any%28%29/README.md)
6. [`every()`](./every%28%29/README.md)
7. [`fold()`](./fold%28%29/README.md)
8. [`reduce()`](./reduce%28%29/README.md)
9. [Functional Patterns](./Functional%20Patterns/README.md)

## Why This Lesson Matters

Functional ideas help you write code that is:

- shorter
- more expressive
- easier to transform
- easier to test
- easier to reuse

Instead of writing long loops for every task, you can often describe the operation directly.

## Senior Developer Mindset For Functional Programming

Strong developers use functional techniques to make data flow clearer.

A good rule is:

- choose the simplest readable approach
- use higher-level collection methods when they make the intent obvious
- keep functions small and pure when possible
- avoid turning simple code into a clever puzzle

Functional programming should improve clarity, not decorate it.

## What You Should Learn Here

By the end of this section, you should be able to:

- treat functions as values
- understand closures
- use collection helpers like `map`, `where`, `any`, `every`, `fold`, and `reduce`
- recognize common functional patterns
- write cleaner transformation logic

## Real-World Example

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];

  List<int> doubled = numbers.map((n) => n * 2).toList();
  print(doubled);
}
```

This transforms the data directly instead of building a manual loop.

## Senior Trick: Focus On Intent

The best functional code makes the goal obvious:

- transform
- filter
- check
- combine
- summarize

If the code reads like a description of the problem, you are probably using functional style well.

## Summary

- functions can be treated like values
- closures capture surrounding context
- collection helpers make data processing cleaner
- folding and reducing help summarize data
- functional patterns reduce boilerplate

## Flutter Connection

Functional programming is used constantly in Flutter for:

- widget builders
- list transformations
- callbacks
- state derivation
- rendering logic

If you understand these tools well, Flutter code becomes much easier to read and shape.
