# Installing Dart

## Learning Goal

In this lesson, you will learn how to install Dart, verify the installation, and run your first program.

## Why Installation Matters

Learning is much easier when your environment is ready.

A proper Dart setup allows you to:

- run code locally
- experiment freely
- install packages
- practice real project workflows

## Ways To Use Dart

You can start Dart in two common ways:

1. use DartPad in the browser
2. install Dart locally on your computer

## Option 1: Use DartPad

DartPad is great for beginners because it requires no installation.

You can:

- write Dart in the browser
- run examples instantly
- test small snippets quickly

This is perfect for:

- trying syntax
- practicing small examples
- understanding concepts fast

## Option 2: Install Dart Locally

Local installation is better when you want to:

- work on multiple files
- learn project structure
- use packages
- practice command-line workflows
- prepare for Flutter development

## General Installation Flow

The exact steps depend on your operating system, but the usual process is:

1. download Dart SDK
2. install it
3. add it to your system path if needed
4. verify the installation

## Verify Installation

After installation, run:

```bash
dart --version
```

If Dart is installed correctly, the terminal prints the installed version.

## Create Your First File

Create `main.dart`:

```dart
void main() {
  print('My Dart setup works');
}
```

Run it:

```bash
dart run main.dart
```

## Expected Output

```text
My Dart setup works
```

## Understanding The Command

### `dart`

This calls the Dart tool from the SDK.

### `run`

This tells Dart to execute a program.

### `main.dart`

This is the file you want to run.

## Try A More Practical Example

```dart
void main() {
  String appName = 'Expense Tracker';
  double monthlyBudget = 15000;

  print('App: $appName');
  print('Monthly budget: $monthlyBudget');
}
```

This helps confirm that:

- your editor can save `.dart` files
- your terminal can run Dart code
- your setup is ready for real examples

## Recommended Setup For Serious Learning

If you want to continue toward Flutter, it helps to set up:

- Dart SDK
- a code editor like VS Code or Android Studio
- terminal access

Useful editor features:

- syntax highlighting
- auto-completion
- error checking
- formatting support

## Helpful Commands After Installation

```bash
dart create my_first_project
dart run
dart analyze
dart format .
```

## What These Commands Mean

### `dart create my_first_project`

Creates a new Dart project.

### `dart run`

Runs the current project or entry file.

### `dart analyze`

Checks for coding issues.

### `dart format .`

Formats all files in the current directory.

## Real-World Scenario

Imagine two learners:

- one only reads syntax
- one installs Dart and runs every example

The second learner improves faster because real learning happens when you:

- make mistakes
- read errors
- fix programs
- experiment with code

That habit becomes extremely valuable in Flutter development.

## Common Problems After Installation

### Problem: `dart` command not found

Possible reason:

- Dart is not installed correctly
- system path is not configured

### Problem: file does not run

Possible reason:

- wrong file name
- incorrect syntax
- running command from the wrong directory

## Quick Check Program

Use this to confirm everything works:

```dart
void main() {
  int a = 10;
  int b = 20;

  print('Sum: ${a + b}');
}
```

If this runs successfully, your environment is ready for the next lessons.

## Why This Helps With Flutter Later

Flutter uses Dart heavily, so getting comfortable with:

- terminal commands
- SDK tools
- project setup
- code execution

will make the Flutter learning curve smoother.

## Summary

- Dart can be used online with DartPad or locally with the SDK
- local installation is better for serious practice
- `dart --version` verifies installation
- `dart run` executes your code
- a working setup is the foundation for future Dart and Flutter projects
