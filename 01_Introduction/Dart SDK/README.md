# Dart SDK

## Learning Goal

In this lesson, you will understand what the Dart SDK is, what it contains, and why it is essential for writing and running Dart programs.

## What Is SDK

SDK stands for Software Development Kit.

The Dart SDK is the collection of tools and libraries you need to develop Dart applications.

Without the SDK, you cannot properly:

- run Dart programs
- compile code
- manage packages
- format code
- analyze code
- test applications

## Simple Definition

You can think of the Dart SDK as the full toolbox for Dart development.

## What The Dart SDK Contains

The Dart SDK mainly includes:

- Dart runtime and compiler support
- built-in libraries
- package management tools
- code formatter
- static analyzer
- testing support through Dart tooling

## Common SDK Commands

Here are some commands you will use often.

### Check Dart version

```bash
dart --version
```

### Run a Dart file

```bash
dart run
```

### Format code

```bash
dart format .
```

### Analyze code

```bash
dart analyze
```

### Manage packages

```bash
dart pub get
```

## First Program With SDK In Mind

Create a file called `main.dart`:

```dart
void main() {
  print('Dart SDK is working');
}
```

Run it with:

```bash
dart run main.dart
```

## What Happened Behind The Scenes

When you run the program:

- the SDK reads your Dart file
- it checks the program
- it executes the code
- it prints the result

So the SDK is not just installed software sitting on your computer.
It actively powers your development workflow.

## Built-In Libraries In The SDK

The SDK includes core libraries that save you from writing everything from scratch.

Example:

```dart
import 'dart:math';

void main() {
  double result = sqrt(81);
  print(result);
}
```

### Explanation

- `dart:math` is part of the SDK
- `sqrt(81)` returns the square root of `81`
- the result is printed as `9.0`

## Analyzer Example

The SDK can catch mistakes before you run the app.

```dart
void main() {
  int age = '25';
  print(age);
}
```

This is wrong because a `String` is being assigned to an `int`.

The analyzer helps detect this early.

## Why This Matters In Real Projects

In a large Flutter app, early error detection is very valuable.

Imagine catching these issues before release:

- wrong data type from an API
- missing required value in a model
- invalid method call

That is exactly why SDK tooling matters.

## Package Management With The SDK

The SDK also helps you use external packages.

Example:

```bash
dart pub get
```

This command reads your `pubspec.yaml` file and downloads required packages.

## Real-World Scenario

Suppose you are building a note-taking app.

You may need:

- local file storage
- date formatting
- test tools
- clean code formatting

The SDK helps you:

- run the project
- manage libraries
- format code
- analyze mistakes

So the SDK supports both coding and project maintenance.

## Relationship Between SDK And Flutter

This is important:

Flutter development also depends on Dart.

When you write Flutter code, you are still using:

- Dart syntax
- Dart type system
- Dart classes
- Dart async features
- Dart package tools

That means understanding the Dart SDK now will help you later when working with Flutter commands and project tooling.

## Example Of A Small Useful Program

```dart
import 'dart:io';

void main() {
  stdout.write('Enter your name: ');
  String? name = stdin.readLineSync();

  print('Welcome, ${name ?? 'Guest'}');
}
```

## What This Uses

- `dart:io` from the SDK
- console input/output
- null safety using `String?`
- null-aware fallback using `??`

This is a great early example because it combines multiple Dart ideas in one small program.

## Common Beginner Confusion

### Language vs SDK

The language is the set of rules and syntax.
The SDK is the toolkit used to work with that language.

### Example

- Dart language: `class`, `if`, `List`, `Future`
- Dart SDK: `dart run`, `dart analyze`, `dart format`, built-in libraries

## Summary

- the Dart SDK is the complete toolkit for Dart development
- it includes tools for running, formatting, analyzing, and managing code
- it also includes useful built-in libraries
- the SDK is essential for both learning Dart and building real apps

## Flutter Connection

When you move into Flutter, you will still rely on your Dart foundation.
Knowing the Dart SDK helps you understand:

- package workflows
- code analysis
- project structure
- how Dart code powers Flutter apps under the hood
