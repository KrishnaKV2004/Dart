# Reading Input

## Learning Goal

In this lesson, you will learn how to read user input in a Dart console program and how to handle it safely.

## Why Input Matters

Without input, programs only work with hardcoded values.
With input, users can provide their own data.

Examples:

- name
- age
- amount
- menu choice
- search text

## Reading Input In Dart

To read input from the console, you use `dart:io`.

### Basic Example

```dart
import 'dart:io';

void main() {
  stdout.write('Enter your name: ');
  String? name = stdin.readLineSync();

  print('Hello, ${name ?? 'Guest'}');
}
```

## Explanation

### `import 'dart:io';`

This imports input/output tools from Dart's standard library.

### `stdout.write()`

This displays a prompt without automatically moving to a new line.

### `stdin.readLineSync()`

This reads text entered by the user.

### `String?`

The result can be `null`, so the type is nullable.

### `??`

Provides a fallback value if the input is `null`.

## Why `stdout.write()` Is Often Better For Prompts

Using:

```dart
stdout.write('Enter your age: ');
```

keeps the cursor on the same line, which feels more natural for prompts.

## Real-World Example

```dart
import 'dart:io';

void main() {
  stdout.write('Enter product name: ');
  String? productName = stdin.readLineSync();

  stdout.write('Enter quantity: ');
  String? quantityInput = stdin.readLineSync();

  print('Product: ${productName ?? 'Unknown'}');
  print('Quantity entered: ${quantityInput ?? '0'}');
}
```

## Senior Trick: Separate Raw Input From Parsed Meaning

Instead of doing too much at once, experienced developers often keep steps clear:

1. read the raw string
2. parse it
3. validate it
4. use it

Example:

```dart
import 'dart:io';

void main() {
  stdout.write('Enter your age: ');
  String? ageInput = stdin.readLineSync();

  int age = int.tryParse(ageInput ?? '') ?? 0;

  print('Age: $age');
}
```

## Why `int.tryParse()` Is Better Than Assuming

If the user types invalid input like `abc`, direct parsing can fail.

`tryParse()` is safer because it returns `null` instead of crashing.

## Example With Validation Thinking

```dart
import 'dart:io';

void main() {
  stdout.write('Enter quantity: ');
  String? quantityInput = stdin.readLineSync();

  int quantity = int.tryParse(quantityInput ?? '') ?? 0;

  if (quantity > 0) {
    print('Added $quantity items to cart');
  } else {
    print('Please enter a valid quantity');
  }
}
```

## Senior Trick: Never Trust User Input Blindly

This is a core professional habit.

Users may enter:

- empty text
- letters where numbers are expected
- extra spaces
- unexpected values

Good programs handle this gracefully.

## Summary

- `dart:io` lets Dart console programs read input
- `stdin.readLineSync()` reads user text
- user input is often nullable
- parsing and validation should be handled carefully

## Flutter Connection

In Flutter, input usually comes from text fields, forms, and user actions instead of the console.
But the same rule still applies:

- read input
- validate it
- convert it safely
- then use it

That habit matters a lot in real apps.
