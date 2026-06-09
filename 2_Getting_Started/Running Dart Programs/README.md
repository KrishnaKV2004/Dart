# Running Dart Programs

## Learning Goal

In this lesson, you will learn how to run Dart code, understand common commands, and build a reliable workflow for testing programs quickly.

## Why Running Code Often Matters

One of the fastest ways to improve is to shorten the loop between:

- writing code
- running code
- observing results
- fixing mistakes

Senior developers do this constantly.
They do not wait until a file becomes large before testing it.

## Basic Way To Run A File

Suppose you have a file named `main.dart`:

```dart
void main() {
  print('Running a Dart program');
}
```

Run it with:

```bash
dart run main.dart
```

## Output

```text
Running a Dart program
```

## Understanding The Command

### `dart`

Calls the Dart tool from the SDK.

### `run`

Tells Dart to execute a program.

### `main.dart`

The file to run.

## A More Practical Example

```dart
void main() {
  String userName = 'Priya';
  bool isLoggedIn = true;

  print('User: $userName');
  print('Logged in: $isLoggedIn');
}
```

Run it:

```bash
dart run main.dart
```

## Senior Trick: Run After Every Meaningful Change

Do not write 100 lines and only then test.

A better workflow is:

1. write a small piece
2. run it
3. confirm the result
4. add the next piece

This makes bugs easier to find because you know what changed.

## Running Inside A Project

In many Dart projects, you can simply run:

```bash
dart run
```

This is common when the project is already structured and Dart knows the main entry file.

## Useful Commands Around Running

### Check version

```bash
dart --version
```

### Analyze code

```bash
dart analyze
```

### Format code

```bash
dart format .
```

## Why `dart analyze` Matters

Example:

```dart
void main() {
  int total = '50';
  print(total);
}
```

This is invalid because a string is assigned to an integer.

The analyzer can catch issues like this before or while you run the program.

## Real-World Debugging Example

Suppose you write:

```dart
void main() {
  double itemPrice = 250.0;
  int quantity = 3;

  print('Total: ${itemPrice * quantity}');
}
```

Expected output:

```text
Total: 750.0
```

Now imagine the result looks wrong in a larger program.
A senior developer might simplify the code and print intermediate values:

```dart
void main() {
  double itemPrice = 250.0;
  int quantity = 3;
  double total = itemPrice * quantity;

  print('itemPrice = $itemPrice');
  print('quantity = $quantity');
  print('total = $total');
}
```

This technique is simple, but extremely effective.

## Common Problems When Running Programs

### Problem: `dart` command not found

Possible cause:

- Dart is not installed
- path is not configured correctly

### Problem: file not found

Possible cause:

- you are in the wrong directory
- the filename is incorrect

### Problem: syntax error

Possible cause:

- missing bracket
- missing semicolon
- invalid string or type usage

## Senior Trick: Keep Your Terminal In The Project Folder

Many beginner issues come from running commands in the wrong directory.

A good habit:

- open terminal in the project folder
- keep filenames consistent
- use simple file names early on

## Example Of A Tiny Test Workflow

```dart
void main() {
  int score = 80;

  if (score >= 50) {
    print('Pass');
  } else {
    print('Fail');
  }
}
```

Run it, then change:

- `80` to `30`
- `50` to `75`

This teaches you more than reading the code once.

## Best Practice: Format Before You Trust The Shape

If code looks messy, run:

```bash
dart format .
```

Experienced developers trust formatting tools because:

- formatting reduces visual confusion
- bracket mistakes become easier to spot
- consistent structure helps review and maintenance

## Summary

- use `dart run main.dart` to run a file
- use `dart run` inside structured projects
- test code in small increments
- use `dart analyze` and `dart format .` regularly
- the fastest learners run and verify code often

## Flutter Connection

This workflow carries directly into Flutter:

- write a change
- run it
- inspect behavior
- fix fast

That tight feedback loop is one of the most important professional habits you can build.
