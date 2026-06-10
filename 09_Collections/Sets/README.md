# Sets

## Learning Goal

In this lesson, you will learn what a `Set` is and when it is a better choice than a list.

## What Is A Set

A `Set` stores unique values.

That means:

- duplicates are not allowed
- each item appears only once

## Basic Example

```dart
void main() {
  Set<String> tags = {'dart', 'flutter', 'dart'};

  print(tags);
}
```

The duplicate `'dart'` is automatically ignored.

## Why Sets Matter

Sets are useful when uniqueness is important.

Examples:

- selected categories
- visited pages
- user roles
- unique tags

## Adding Values

```dart
void main() {
  Set<String> permissions = {'read'};

  permissions.add('write');
  permissions.add('read');

  print(permissions);
}
```

Even though `'read'` is added again, it only appears once.

## Real-World Example

```dart
void main() {
  Set<String> selectedFilters = {'Electronics', 'Books'};

  selectedFilters.add('Books');
  selectedFilters.add('Fashion');

  print(selectedFilters);
}
```

This is useful in filter or tag-selection logic.

## Senior Trick: Use A Set When You Mean Uniqueness

If duplicates should never matter, a set often expresses the domain better than a list.

Using the right collection type communicates intent.

## Summary

- a `Set` stores unique values
- duplicates are automatically ignored
- sets are useful when uniqueness matters more than repetition

## Flutter Connection

In Flutter, sets are useful for:

- selected IDs
- active filters
- unique options
- permission-style values

They are especially handy when the same item should not be added twice.
