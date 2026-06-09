# continue

## Learning Goal

In this lesson, you will learn how to skip the current iteration and move to the next one using `continue`.

## What Does `continue` Do

`continue` skips the rest of the current loop iteration and jumps to the next iteration.

## Basic Example

```dart
void main() {
  for (int i = 1; i <= 5; i++) {
    if (i == 3) {
      continue;
    }

    print(i);
  }
}
```

## Output

```text
1
2
4
5
```

The value `3` is skipped.

## Real-World Example

```dart
void main() {
  List<String> products = ['Laptop', '', 'Keyboard', 'Mouse'];

  for (String product in products) {
    if (product.isEmpty) {
      continue;
    }

    print('Product: $product');
  }
}
```

This skips invalid or empty values while continuing to process the rest.

## Senior Trick: Use `continue` To Reduce Nesting

Sometimes `continue` makes loops cleaner by handling edge cases early.

Instead of:

```dart
for (String product in products) {
  if (product.isNotEmpty) {
    print(product);
  }
}
```

you might use `continue` when there are several early-skip cases.

## Summary

- `continue` skips the rest of the current iteration
- it is useful for ignoring unwanted cases
- it can make loops flatter and easier to read

## Flutter Connection

In Flutter-related Dart logic, `continue` is useful when filtering or skipping data during processing before it reaches the UI.
