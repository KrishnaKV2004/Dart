# Interface Classes

## Learning Goal

In this lesson, you will learn what an interface class is and how it helps separate implementation from contract.

## What Is An Interface Class

An interface class is designed to be implemented, not necessarily inherited for code reuse.

It is a way to define a contract clearly.

## Basic Example

```dart
interface class StorageService {
  void save(String key, String value) {
    throw UnimplementedError();
  }
}

class LocalStorageService implements StorageService {
  @override
  void save(String key, String value) {
    print('Saved $key = $value locally');
  }
}
```

## Why Interface Classes Matter

They help make it clear that:

- other code should depend on the capability
- not on inherited implementation details

## Senior Trick: Use Interface Classes For Contracts That Should Be Swappable

This is useful for:

- storage services
- analytics services
- auth providers
- repositories

## Summary

- interface classes define contracts for implementation
- they help separate usage from implementation details
- they are useful for testable and flexible architecture

## Flutter Connection

Interface-style design is very useful in Flutter for dependency injection, testing, and service-based architecture.
