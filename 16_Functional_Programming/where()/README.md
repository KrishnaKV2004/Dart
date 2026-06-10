# `where()`

## Learning Goal

In this lesson, you will learn how `where()` filters items in a collection based on a condition.

## What Does `where()` Do

`where()` returns only the items that match the condition you provide.

It is used when you want to keep some values and discard others.

## Basic Example

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  List<int> evenNumbers = numbers.where((n) => n % 2 == 0).toList();

  print(evenNumbers);
}
```

Only even numbers remain.

## Why This Is Useful

Filtering is one of the most common data tasks in programming.

`where()` makes that intent very clear.

## Real-World Example

```dart
void main() {
  List<String> names = ['Asha', 'Ravi', 'Anu'];
  List<String> shortNames = names.where((name) => name.length <= 4).toList();

  print(shortNames);
}
```

This is a clean way to keep only matching values.

## Senior Trick: Use `where()` For Conditions, Not Transformations

If the job is to test whether an item should stay, `where()` is the right tool.

If the job is to change the item, use `map()`.

## Senior Trick: Keep Predicates Simple

The condition passed to `where()` should be easy to understand at a glance.

If it becomes too complex, extract it into a named function.

## Summary

- `where()` filters items using a condition
- it keeps matching values
- it is different from `map()`
- simple conditions make code easier to read

## Flutter Connection

`where()` is common in Flutter for filtering lists before rendering or passing data into widgets.
