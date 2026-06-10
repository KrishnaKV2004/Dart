# Versioning

## Learning Goal

In this lesson, you will learn why version numbers matter in Dart dependencies and package management.

## What Is Versioning

Versioning is the practice of labeling different releases of software so users can depend on the correct one.

In Dart, this is especially important for package compatibility.

## Basic Example

```yaml
dependencies:
  http: ^1.0.0
```

The version constraint tells Dart which releases are acceptable.

## Why This Is Useful

Versioning helps you:

- control updates
- avoid breaking changes
- keep builds reproducible
- communicate compatibility

## Real-World Example

```yaml
environment:
  sdk: ^3.0.0

dependencies:
  path: ^1.9.0
```

This setup says what SDK range and dependency range the package supports.

## Senior Trick: Do Not Update Versions Blindly

A new version may fix bugs, but it may also introduce breaking changes.

Review version changes before upgrading important dependencies.

## Senior Trick: Stable Dependencies Make Debugging Easier

If your dependency tree changes constantly, reproducing bugs becomes harder.

Version discipline makes teams calmer and releases safer.

## Summary

- versioning identifies software releases
- it helps manage compatibility
- it keeps dependency updates safer
- careful version choices reduce surprises

## Flutter Connection

Versioning is crucial in Flutter because package updates can affect app builds, behavior, and long-term maintainability.
