# Closures

## Learning Goal

In this lesson, you will learn what a closure is and how a function can remember values from its surrounding scope.

## What Is A Closure

A closure is a function that captures variables from the surrounding context.

Even after the outer function has finished, the inner function can still use those captured values.

## Basic Example

```dart
Function counter() {
  int count = 0;

  return () {
    count++;
    print(count);
  };
}

void main() {
  var increment = counter();
  increment();
  increment();
}
```

The returned function remembers `count`.

## Why This Is Useful

Closures are useful when a function needs to keep state without using a class.

They are common in:

- callbacks
- factories
- event handlers
- small stateful utilities

## Real-World Example

```dart
Function multiplier(int factor) {
  return (int value) => value * factor;
}

void main() {
  var doubleValue = multiplier(2);
  print(doubleValue(5));
}
```

The returned function remembers `factor`.

## Senior Trick: Use Closures For Small Local State

Closures are a clean way to keep tiny pieces of state close to the logic that uses them.

If the state becomes more complex, a class may be easier to maintain.

## Senior Trick: Be Careful With Captured Variables

Because closures keep references to outer variables, make sure you understand what value is being shared and when it changes.

That matters in loops, callbacks, and asynchronous code.

## Summary

- closures capture variables from surrounding scope
- they let functions remember state
- they are useful for small stateful behaviors
- they should stay simple and understandable

## Flutter Connection

Closures are used often in Flutter for event handlers, builders, and local state logic inside widgets.
