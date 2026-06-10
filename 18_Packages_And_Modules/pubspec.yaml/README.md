# `pubspec.yaml`

## Learning Goal

In this lesson, you will learn what `pubspec.yaml` does and why it is central to Dart package configuration.

## What Is `pubspec.yaml`

`pubspec.yaml` is the configuration file that describes your Dart project or package.

It commonly includes:

- project name
- description
- environment constraints
- dependencies
- dev dependencies

## Basic Example

```yaml
name: my_app
description: A sample Dart project
version: 1.0.0

environment:
  sdk: ^3.0.0

dependencies:
  http: ^1.0.0

dev_dependencies:
  lints: ^3.0.0
```

## Why This Is Useful

This file tells Dart:

- what your package is called
- which SDK range it supports
- which packages it depends on
- which tools you use for development

## Real-World Example

```yaml
name: lesson18_demo
description: Demo project for packages and modules

environment:
  sdk: ^3.0.0

dependencies:
  path: ^1.9.0
```

This is the kind of metadata a package manager needs to work correctly.

## Senior Trick: Treat Version Constraints Carefully

Version numbers are not just decoration.

They affect:

- compatibility
- reproducibility
- upgrade safety

Use them intentionally.

## Senior Trick: Keep Dependencies Honest

If a project does not need a package, do not add it.

Every dependency has a maintenance cost.

## Summary

- `pubspec.yaml` configures the project
- it defines dependencies and metadata
- it controls SDK compatibility
- version choices matter a lot

## Flutter Connection

In Flutter, `pubspec.yaml` also controls assets, fonts, and package dependencies, so it is one of the most important files in the project.
