# Generic Classes

## Learning Goal

In this lesson, you will learn how to create classes that work with different types while staying type-safe.

## What Is A Generic Class

A generic class is a class that can work with one or more type parameters.

Instead of hardcoding the value type, you make the class flexible with a placeholder such as `T`.

## Basic Example

```dart
class Box<T> {
  final T value;

  Box(this.value);
}

void main() {
  Box<String> nameBox = Box('Asha');
  Box<int> ageBox = Box(21);

  print(nameBox.value);
  print(ageBox.value);
}
```

## Why This Is Useful

Without generics, you might need separate classes for each type of data.

For example:

- `StringBox`
- `IntBox`
- `UserBox`

With a generic class, one design can serve all of them.

## Real-World Example

```dart
class ApiResponse<T> {
  final T data;
  final bool success;

  ApiResponse({
    required this.data,
    required this.success,
  });
}

void main() {
  ApiResponse<String> textResponse = ApiResponse(
    data: 'Loaded',
    success: true,
  );

  print(textResponse.data);
}
```

This pattern is common in apps because different endpoints can return different model types.

## Senior Trick: Use Generic Classes When The Shape Stays The Same

Generics are a great fit when the structure is identical, but the value type changes.

Good use cases:

- containers
- wrappers
- cache entries
- response models

If the class behavior changes heavily by type, separate classes may be clearer.

## Senior Trick: Let The Type Flow Through The API

Good generic classes do not hide the type.

They make the type obvious at the call site so the code explains itself.

## Summary

- generic classes use type parameters like `T`
- they let one class work with many types
- they improve type safety and reduce duplication
- they are useful when the class structure stays consistent

## Flutter Connection

Generic classes are common in Flutter for:

- API response wrappers
- state containers
- reusable model holders
- utility classes

They help keep app code flexible without losing clarity.
