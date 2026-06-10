# `every()`

## Learning Goal

In this lesson, you will learn how `every()` checks whether all items in a collection match a condition.

## What Does `every()` Do

`every()` returns `true` only if every item satisfies the condition.

If even one item fails, it returns `false`.

## Basic Example

```dart
void main() {
  List<int> numbers = [2, 4, 6];
  bool allEven = numbers.every((n) => n % 2 == 0);

  print(allEven);
}
```

All items match, so the result is `true`.

## Why This Is Useful

`every()` is useful for validation and consistency checks.

It is a clean way to ask whether the whole collection meets a rule.

## Real-World Example

```dart
void main() {
  List<String> usernames = ['ash', 'ravi', 'nina'];
  bool allShort = usernames.every((name) => name.length <= 5);

  print(allShort);
}
```

This checks a rule across the entire collection.

## Senior Trick: Use `every()` For Whole-Set Validation

If you need to know whether all items pass a condition, `every()` is much clearer than manual looping.

It expresses the idea directly.

## Senior Trick: Do Not Confuse `any()` And `every()`

`any()` asks if at least one item matches.

`every()` asks if all items match.

Keeping that difference clear avoids logic bugs.

## Summary

- `every()` checks whether all items match a condition
- it returns a boolean
- it is useful for validation
- it is different from `any()`

## Flutter Connection

`every()` is useful in Flutter for validation rules, consistency checks, and collection-based decision logic.
