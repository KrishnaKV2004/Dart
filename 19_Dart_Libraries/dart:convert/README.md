# `dart:convert`

## Learning Goal

In this lesson, you will learn how `dart:convert` helps you encode and decode data such as JSON and UTF-8 text.

## What Is `dart:convert`

`dart:convert` provides utilities for converting data between formats.

It is often used for:

- JSON
- UTF-8
- base64
- text conversion

## Basic Example

```dart
import 'dart:convert';

void main() {
  final jsonString = '{"name":"Asha","age":21}';
  final data = jsonDecode(jsonString);

  print(data);
}
```

Expected output:

```text
{name: Asha, age: 21}
```

The JSON string becomes a Dart map-like structure.

## Why This Is Useful

This library is essential when working with:

- APIs
- local storage
- text processing
- data interchange formats

## Real-World Example

```dart
import 'dart:convert';

void main() {
  final data = {'product': 'Laptop', 'price': 55000};
  final jsonString = jsonEncode(data);

  print(jsonString);
}
```

Expected output:

```text
{"product":"Laptop","price":55000}
```

This is one of the most common tasks in Dart applications.

## Senior Trick: Convert At The Boundary

Convert data when it enters or leaves your app boundary.

Inside your app, keep data in a clean Dart structure as long as possible.

## Senior Trick: Keep Serialization Logic Predictable

If JSON or text conversion becomes complicated, separate it into a helper or model layer.

That makes debugging much easier.

## Summary

- `dart:convert` handles data format conversion
- it is heavily used for JSON and text
- it sits at the boundary between external data and Dart objects
- clean conversion logic improves maintainability

## Flutter Connection

Flutter apps use `dart:convert` constantly for API requests, local persistence, and decoding server data.
