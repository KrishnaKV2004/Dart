# Parameters

## Learning Goal

In this lesson, you will learn how to pass data into functions using parameters.

## What Are Parameters

Parameters are variables defined in a function so the function can receive input values.

## Basic Example

```dart
void greetUser(String name) {
  print('Hello, $name');
}

void main() {
  greetUser('Aarohi');
}
```

## Why Parameters Matter

Without parameters, a function can only do the same exact thing every time.

With parameters, the function becomes flexible.

## More Than One Parameter

```dart
void showProduct(String name, double price) {
  print('Product: $name');
  print('Price: $price');
}

void main() {
  showProduct('Keyboard', 1499.0);
}
```

## Senior Trick: Choose Parameter Names Carefully

Good parameter names make function calls easier to understand.

Weak:

```dart
void createUser(String a, int b) {
  print('$a - $b');
}
```

Better:

```dart
void createUser(String userName, int age) {
  print('$userName - $age');
}
```

## Order Matters In Positional Parameters

```dart
void bookTicket(String movieName, int seatCount) {
  print('Movie: $movieName');
  print('Seats: $seatCount');
}
```

You must pass values in the correct order:

```dart
bookTicket('Interstellar', 2);
```

## Real-World Example

```dart
void addToCart(String productName, int quantity) {
  print('Added $quantity x $productName to cart');
}

void main() {
  addToCart('Headphones', 2);
}
```

This is exactly the kind of reusable action you will have in app logic.

## Senior Trick: Keep Parameter Lists Reasonable

If a function needs too many parameters, it may be doing too much.

That can be a hint to:

- split the function
- group related data
- use named parameters later

## Summary

- parameters let functions receive input
- they make functions reusable and flexible
- good parameter names improve readability
- too many parameters may signal a design problem

## Flutter Connection

In Flutter, parameters are used everywhere:

- widget constructors
- event handlers
- helper functions
- validation methods

Learning to design clean parameters now will help a lot later.
