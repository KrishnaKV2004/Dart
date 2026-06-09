# Lesson 13: Generics

This section teaches how to write code that works with multiple types while staying type-safe and reusable.

Generics are one of the most practical Dart features for building code that is flexible without becoming messy.

## Topics In This Lesson

1. [Generic Classes](./Generic%20Classes/README.md)
2. [Generic Functions](./Generic%20Functions/README.md)
3. [Type Constraints](./Type%20Constraints/README.md)
4. [Best Practices](./Best%20Practices/README.md)

## Why This Lesson Matters

Without generics, you often end up writing the same structure again and again for different types.

For example:

- a container for `String`
- a container for `int`
- a container for `double`
- a container for custom objects

Generics let you write that structure once and reuse it safely.

## Senior Developer Mindset For Generics

Strong developers use generics to make APIs clearer and safer, not more complicated.

A good rule is:

- use generics when the type is part of the design
- avoid generics when a simple concrete type is easier to understand

Generics should reduce duplication and improve correctness.
They should not make basic code harder to read.

## What You Should Learn Here

By the end of this section, you should be able to:

- understand how generic types improve reuse
- create generic classes and functions
- use type parameters like `T`
- add constraints when a generic type needs specific capabilities
- recognize when generics are overkill

## Real-World Example

```dart
class Box<T> {
  final T value;

  Box(this.value);
}

void main() {
  Box<String> nameBox = Box('Asha');
  Box<int> numberBox = Box(42);

  print(nameBox.value);
  print(numberBox.value);
}
```

The same class works for different types without losing type safety.

## Senior Trick: Let The Type Explain The Data

When you use generics well, the type becomes part of the documentation.

For example:

- `List<String>` clearly says "this list holds strings"
- `Map<String, int>` clearly says "this map connects strings to integers"
- `Box<User>` clearly says "this container holds a User"

That kind of clarity helps both beginners and experienced developers read code faster.

## Senior Trick: Constrain Types When Needed

If a generic type must support certain methods or properties, add a constraint instead of assuming everything will work.

That is safer than writing code that only works for some hidden cases.

## Summary

- generics let you write reusable code for multiple types
- they improve type safety and reduce duplication
- generic classes and functions are core Dart tools
- constraints help generics stay correct and intentional

## Flutter Connection

Generics are everywhere in Flutter and Dart:

- widget collections
- API response models
- repositories
- helper utilities
- state containers

If you understand generics well, a lot of Flutter and package code becomes much easier to read and design.
