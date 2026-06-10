# Maps

## Learning Goal

In this lesson, you will learn how `Map` stores data as key-value pairs and why maps are essential in real applications.

## What Is A Map

A `Map` stores values using keys.

This means each value is associated with a name or identifier instead of a numeric index.

## Basic Example

```dart
void main() {
  Map<String, String> user = {
    'name': 'Rina',
    'city': 'Jaipur',
  };

  print(user['name']);
}
```

## Why Maps Matter

Maps are excellent for structured data.

Examples:

- user details
- settings
- API response fields
- configuration objects

## Adding And Updating Values

```dart
void main() {
  Map<String, dynamic> profile = {
    'name': 'Kunal',
    'age': 24,
  };

  profile['city'] = 'Indore';
  profile['age'] = 25;

  print(profile);
}
```

## Real-World Example

```dart
void main() {
  Map<String, dynamic> product = {
    'name': 'Laptop',
    'price': 55000,
    'inStock': true,
  };

  print('Product: ${product['name']}');
  print('Price: ${product['price']}');
}
```

This is very similar to data returned from APIs.

## Senior Trick: Use Specific Map Types When Possible

Good:

```dart
Map<String, String> settings = {
  'theme': 'light',
  'language': 'en',
};
```

Use `Map<String, dynamic>` only when values truly differ in type.

## Common Mistake: Assuming A Missing Key Always Exists

```dart
void main() {
  Map<String, String> user = {'name': 'Rina'};
  print(user['email']);
}
```

This returns `null` because the key does not exist.

That is why safe handling matters.

## Summary

- a `Map` stores key-value pairs
- it is useful for structured named data
- map values are accessed by keys
- maps are extremely common in real application data

## Flutter Connection

In Flutter, maps are used for:

- raw JSON-style API data
- settings
- temporary structured state
- configuration objects

Understanding maps well helps a lot with backend data and UI integration.
