# Final Classes

## Learning Goal

In this lesson, you will learn what a final class is and when it is useful.

## What Is A Final Class

A final class is a class that cannot be extended or implemented outside its intended boundary.

It communicates that the class design should remain closed.

## Basic Example

```dart
final class AppConfig {
  final String environment;

  AppConfig(this.environment);
}
```

## Why Final Classes Matter

Sometimes a class should be used as-is.

Reasons may include:

- protecting invariants
- preventing fragile subclassing
- keeping API behavior stable

## Senior Trick: Close A Class When Extension Would Be Harmful

Not every class should be designed for inheritance.

In fact, many classes are safer when they are not open for extension by default.

## Summary

- final classes are closed to outside extension and implementation
- they help protect design boundaries
- they are useful when a class should remain stable as-is

## Flutter Connection

Final classes matter more in library and package design, but the idea is useful when you want strong control over critical app types.
