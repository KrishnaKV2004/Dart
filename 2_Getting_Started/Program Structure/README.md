# Program Structure

## Learning Goal

In this lesson, you will learn how a Dart program is organized and how to keep it clean as it grows.

## Why Program Structure Matters Early

Many beginners focus only on syntax:

- variables
- loops
- conditions

But experienced developers also care about shape:

- where code starts
- what belongs together
- how to make code readable
- how to keep growth manageable

That is what program structure is about.

## Basic Dart Program Structure

Here is a small program:

```dart
void main() {
  greetUser();
  showAppVersion();
}

void greetUser() {
  print('Welcome back, user');
}

void showAppVersion() {
  print('Version 1.0.0');
}
```

## Main Parts Of This Program

### `main()`

The entry point.
Execution starts here.

### Functions

`greetUser()` and `showAppVersion()` are separate functions.
They keep responsibilities small and clear.

## Why This Is Better Than One Big `main()`

This works:

```dart
void main() {
  print('Welcome back, user');
  print('Version 1.0.0');
}
```

But the earlier version is better for growth because:

- each task has a name
- code is easier to scan
- behavior is easier to reuse
- future changes are easier

## Senior Trick: Keep `main()` Thin

A strong habit is to keep `main()` simple and delegate work.

Good:

```dart
void main() {
  startApplication();
}

void startApplication() {
  print('App started');
}
```

Less ideal:

```dart
void main() {
  print('App started');
  print('Loading user');
  print('Checking settings');
  print('Preparing dashboard');
}
```

As programs grow, a thin `main()` becomes much easier to maintain.

## Example With Real App Thinking

```dart
void main() {
  loadUserProfile();
  loadNotifications();
}

void loadUserProfile() {
  print('Loading user profile...');
}

void loadNotifications() {
  print('Loading notifications...');
}
```

This mirrors how real apps are organized:

- one task per function
- readable flow from top to bottom
- names that describe behavior

## Common Elements In A Dart File

A Dart file may contain:

- imports
- constants
- variables
- functions
- classes
- `main()`

Example:

```dart
const String appName = 'ShopEasy';

void main() {
  print('Starting $appName');
}
```

## Recommended Early Structure

For simple files, a good order is:

1. imports
2. constants
3. `main()`
4. helper functions
5. classes

This is not a strict law, but it keeps files readable.

## Senior Trick: One Function, One Purpose

Weak example:

```dart
void processEverything() {
  print('Login user');
  print('Fetch products');
  print('Show cart');
}
```

Better:

```dart
void main() {
  loginUser();
  fetchProducts();
  showCart();
}

void loginUser() {
  print('Login user');
}

void fetchProducts() {
  print('Fetch products');
}

void showCart() {
  print('Show cart');
}
```

This structure becomes especially useful when debugging.

## Example: Small But Clean Program

```dart
void main() {
  displayHeader();
  calculateFinalPrice();
}

void displayHeader() {
  print('=== Invoice Calculator ===');
}

void calculateFinalPrice() {
  double itemPrice = 1500;
  double tax = 150;
  double total = itemPrice + tax;

  print('Final amount: $total');
}
```

## Why This Is Good

- the flow is easy to understand
- functions are named by purpose
- values are local to the function that uses them
- the code is ready to expand later

## Structure And OOP

Program structure is also your bridge into object-oriented programming.

Later, instead of storing everything in loose functions, you will often group related data and behavior into classes.

For example:

```dart
class Cart {
  double total = 0;

  void addItem(double price) {
    total += price;
  }
}

void main() {
  Cart cart = Cart();
  cart.addItem(499);
  print(cart.total);
}
```

This is the same structural thinking, just one level more organized.

## Real-World Scenario

Imagine you are building a Flutter app for food ordering.

Bad early structure:

- all logic inside one place
- unclear names
- repeated code

Better structure:

- one function for loading data
- one function for calculating totals
- one class for order data
- one class for user data

That kind of thinking starts here, even in small Dart files.

## Common Beginner Mistakes

- putting everything inside `main()`
- giving functions vague names
- mixing unrelated logic in one function
- writing code in a way that is hard to scan

## Best Practices

- keep `main()` short
- split logic into small named functions
- give each function one responsibility
- use readable naming
- organize code for future growth, not only today

## Summary

- a Dart program starts from `main()`
- functions help split work into clear units
- a clean structure makes code easier to read, test, and extend
- good structure today prepares you for OOP and Flutter architecture later

## Flutter Connection

In Flutter, structure matters even more because apps grow fast.
If you learn early to:

- separate responsibilities
- keep entry points clean
- use small reusable units

you will have a much easier time when building real screens, models, and app features.
