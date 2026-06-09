# Comments

## Learning Goal

In this lesson, you will learn what comments are, how to write them in Dart, and how to use them wisely like a professional developer.

## What Are Comments

Comments are notes in the code that Dart ignores during execution.

They are meant for humans, not for the compiler.

Comments help explain:

- intent
- assumptions
- warnings
- tricky logic

## Types Of Comments In Dart

### Single-line comment

```dart
void main() {
  // This prints a welcome message.
  print('Welcome to Dart');
}
```

### Multi-line comment

```dart
void main() {
  /*
    This program shows
    a simple multi-line comment.
  */
  print('Hello');
}
```

### Documentation comment

```dart
/// Returns the total price after tax.
double calculateTotal(double price, double tax) {
  return price + tax;
}
```

Documentation comments are useful when writing reusable functions, classes, and APIs.

## The Most Important Rule About Comments

Good code should explain the "what".
Comments should usually explain the "why".

For example, this comment is weak:

```dart
int age = 20; // Store age
```

Why it is weak:

- the code already says that

This is more useful:

```dart
int retryCount = 3; // Keep retries low to avoid duplicate payments.
```

Now the comment adds real context.

## Senior Trick: Prefer Clear Names Before Adding Comments

Bad naming:

```dart
double x = 1200;
double y = 0.18;
```

Better naming:

```dart
double productPrice = 1200;
double taxRate = 0.18;
```

Often strong naming removes the need for extra comments.

## Example: Useful Comment In Real Logic

```dart
void main() {
  double orderTotal = 2500;

  // Free delivery is available for orders above 2000.
  if (orderTotal > 2000) {
    print('Free delivery applied');
  } else {
    print('Delivery charges apply');
  }
}
```

This comment is useful because it explains a business rule.

## Example: Unnecessary Comment

```dart
void main() {
  // Print order total
  print('Order total');
}
```

This comment adds no value because the code is already obvious.

## When Comments Are Helpful

Use comments when:

- the logic is not immediately obvious
- you are documenting a business rule
- you want to warn future developers
- you are writing public functions or classes

## When Comments Become Harmful

Comments become harmful when they are:

- outdated
- obvious
- too many
- used to hide messy code

## Senior Trick: If You Need Too Many Comments, Simplify The Code

If you feel forced to explain every line, the issue may be the code structure.

For example, instead of this:

```dart
void main() {
  // Get price
  double p = 500;
  // Get discount
  double d = 50;
  // Subtract discount from price
  double f = p - d;
  // Print final value
  print(f);
}
```

Write clearer code:

```dart
void main() {
  double productPrice = 500;
  double discountAmount = 50;
  double finalPrice = productPrice - discountAmount;

  print(finalPrice);
}
```

This version teaches more through code quality than through comments.

## Documentation Comment Example

```dart
/// Checks whether a user can access premium content.
bool canAccessPremium(bool isPremiumUser) {
  return isPremiumUser;
}
```

This is useful later when your codebase grows and multiple developers use the same function.

## Real-World Scenario

Imagine a payment app with a special rule:

- refunds above a certain amount need manual review

Code:

```dart
bool needsManualReview(double refundAmount) {
  // Large refunds are manually reviewed to reduce fraud risk.
  return refundAmount > 10000;
}
```

That comment helps future developers understand the business reason behind the condition.

## Best Practices

- write comments that add meaning
- delete comments that repeat the code
- keep comments updated when logic changes
- prefer documentation comments for reusable APIs
- do not use comments as a replacement for clean design

## Summary

- comments are for explaining intent and context
- Dart supports single-line, multi-line, and documentation comments
- the best comments explain why, not what
- clear names often reduce the need for comments

## Flutter Connection

In Flutter projects, comments are useful for:

- complex UI logic
- state management rules
- API assumptions
- reusable classes and services

But the same rule stays true: clean code first, comments second.
