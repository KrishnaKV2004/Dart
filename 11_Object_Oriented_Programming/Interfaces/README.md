# Interfaces

## Learning Goal

In this lesson, you will learn how interfaces define capabilities that classes can implement.

## What Is An Interface

An interface describes what a class must provide.

In Dart, any class can act as an interface, and another class can `implement` it.

## Basic Example

```dart
class Logger {
  void log(String message) {}
}

class ConsoleLogger implements Logger {
  @override
  void log(String message) {
    print(message);
  }
}
```

## Why Interfaces Matter

Interfaces help you depend on behavior instead of depending tightly on one specific implementation.

## Real-World Example

```dart
abstract class StorageService {
  void save(String key, String value);
}

class LocalStorageService implements StorageService {
  @override
  void save(String key, String value) {
    print('Saved $key = $value locally');
  }
}
```

## Senior Trick: Interfaces Make Swapping Implementations Easier

This is useful for:

- testing
- changing providers
- separating app layers

## Summary

- interfaces define required behavior
- `implements` creates a contract-based relationship
- interfaces help code stay flexible and testable

## Flutter Connection

Interfaces are very useful in Flutter architecture for repositories, services, analytics, storage, and test-friendly design.
