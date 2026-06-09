# Sealed Classes

## Learning Goal

In this lesson, you will learn what sealed classes are and why they are powerful for modeling closed sets of states.

## What Is A Sealed Class

A sealed class restricts which classes can extend or implement it.

In practice, it is useful when you want a type to have a known, limited set of possible subtypes.

## Why Sealed Classes Matter

Sealed classes are excellent for state modeling.

Examples:

- loading
- success
- error

This is very common in app development.

## Basic Example

```dart
sealed class LoginState {}

class LoginLoading extends LoginState {}

class LoginSuccess extends LoginState {
  final String userName;

  LoginSuccess(this.userName);
}

class LoginError extends LoginState {
  final String message;

  LoginError(this.message);
}
```

## Why This Is Powerful

The set of possible states is clear and controlled.

That makes your logic easier to:

- reason about
- switch over
- maintain

## Senior Trick: Sealed Classes Are Great For App State

They are especially useful when a value should be one of a few known shapes.

That is much better than vague boolean combinations like:

- `isLoading`
- `hasError`
- `hasData`

which can become confusing together.

## Summary

- sealed classes define a closed family of related subtypes
- they are excellent for state modeling
- they improve clarity and exhaustiveness in logic

## Flutter Connection

Sealed classes are extremely useful in Flutter for screen states, async states, and result modeling.
