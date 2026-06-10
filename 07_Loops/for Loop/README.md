# for Loop

## Learning Goal

In this lesson, you will learn how to repeat code a fixed number of times using a `for` loop.

## What Is A `for` Loop

A `for` loop is useful when you know:

- where to start
- when to stop
- how the loop should move each time

## Basic Example

```dart
void main() {
  for (int i = 1; i <= 5; i++) {
    print(i);
  }
}
```

## Output

```text
1
2
3
4
5
```

## Structure

```dart
for (initialization; condition; update) {
  // code
}
```

### Initialization

Runs once at the beginning.

### Condition

The loop continues while this remains true.

### Update

Runs after each iteration.

## Real-World Example

```dart
void main() {
  for (int invoiceNumber = 1; invoiceNumber <= 3; invoiceNumber++) {
    print('Processing invoice #$invoiceNumber');
  }
}
```

## Senior Trick: Make Loop Variables Meaningful When It Helps

Short names like `i` are common for small loops.
But if the loop has business meaning, better names can help.

Example:

```dart
for (int pageNumber = 1; pageNumber <= 5; pageNumber++) {
  print('Loading page $pageNumber');
}
```

## Common Mistake: Off-By-One Errors

This is one of the most common loop bugs.

Example:

```dart
for (int i = 1; i < 5; i++) {
  print(i);
}
```

This prints:

```text
1
2
3
4
```

not `5`.

Pay close attention to:

- `<`
- `<=`

## Senior Trick: Keep Loop Bodies Small

If a loop does too many things, it gets harder to debug.

Better:

```dart
void main() {
  for (int i = 1; i <= 3; i++) {
    showOrderStatus(i);
  }
}

void showOrderStatus(int orderNumber) {
  print('Order $orderNumber is ready');
}
```

## Summary

- `for` loops repeat code a controlled number of times
- they are ideal when the start, stop, and update are clear
- watch out for off-by-one mistakes
- small loop bodies are easier to trust

## Flutter Connection

In Flutter, `for` loops are useful for:

- generating repeated UI items
- processing lists by index
- handling repeated setup logic

They are a basic but powerful part of app development.
