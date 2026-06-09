# break

## Learning Goal

In this lesson, you will learn how to stop a loop early using `break`.

## What Does `break` Do

`break` immediately exits the current loop.

## Basic Example

```dart
void main() {
  for (int i = 1; i <= 5; i++) {
    if (i == 3) {
      break;
    }

    print(i);
  }
}
```

## Output

```text
1
2
```

When `i` becomes `3`, the loop stops completely.

## Real-World Example

```dart
void main() {
  List<String> users = ['Amit', 'Neha', 'Sara', 'Ravi'];

  for (String user in users) {
    if (user == 'Sara') {
      print('User found');
      break;
    }

    print('Checking $user');
  }
}
```

This is useful when you can stop once the target is found.

## Senior Trick: Use `break` To Stop Unnecessary Work

If the answer is already known, continuing the loop wastes time and makes the code less efficient.

## Summary

- `break` exits the current loop immediately
- it is useful when the loop has already achieved its goal
- it can improve both clarity and efficiency

## Flutter Connection

In Flutter-related Dart logic, `break` can be useful when scanning collections or checking states where work should stop after a match is found.
