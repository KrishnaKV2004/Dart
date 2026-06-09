# Base Classes

## Learning Goal

In this lesson, you will learn what a base class is and why Dart uses it to make inheritance more intentional.

## What Is A Base Class

A base class is a class that is meant to be inherited in a controlled way.

It tells Dart and other developers:

- this class is part of an inheritance hierarchy
- extending it should be intentional

## Basic Example

```dart
base class Vehicle {
  void start() {
    print('Vehicle started');
  }
}

class Car extends Vehicle {}
```

## Why Base Classes Matter

They make class hierarchy design more explicit.

This helps protect APIs and communicate intent better than plain inheritance alone.

## Senior Trick: Use Base When Inheritance Is Intended, But Not Arbitrary

If a class is part of a designed extension hierarchy, `base` can make that intent clearer.

## Summary

- a base class is designed for controlled inheritance
- it makes class hierarchy intent more explicit
- it helps communicate architectural boundaries

## Flutter Connection

Base classes are more relevant in library and framework-style design, but understanding them helps when building structured app architectures or shared internal libraries.
