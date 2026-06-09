# Lesson 3: Variables And Data Types

This section teaches one of the most important foundations in Dart: how data is stored, described, and safely used.

If this part becomes clear, many later topics become much easier:

- conditions
- loops
- functions
- collections
- null safety
- classes
- Flutter state and models

## Topics In This Lesson

1. [Variables](./Variables/README.md)
2. [final](./final/README.md)
3. [const](./const/README.md)
4. [int](./int/README.md)
5. [double](./double/README.md)
6. [num](./num/README.md)
7. [String](./String/README.md)
8. [bool](./bool/README.md)
9. [dynamic](./dynamic/README.md)
10. [var](./var/README.md)
11. [Type Inference](./Type%20Inference/README.md)

## Why This Lesson Matters So Much

Variables are how your program remembers things.
Data types are how your program understands what kind of thing it is working with.

For example:

- a user's name is text
- an age is a number
- a price may contain decimals
- a login status is true or false

When you choose the right type, your code becomes:

- safer
- easier to read
- easier to debug
- easier to scale

## Senior Developer Mindset For This Section

Strong Dart developers do not choose types randomly.
They use types to communicate intent.

Good type choices help answer questions like:

- Can this value change?
- Should this value ever be null?
- Is this whole number or decimal?
- Is this value truly flexible, or am I being too loose?

## What You Should Learn Here

By the end of this section, you should be able to:

- declare variables clearly
- choose the correct basic data type
- understand when to use `var`, `final`, and `const`
- know why `dynamic` should be used carefully
- read and write code with stronger type confidence

## Flutter Connection

This lesson directly prepares you for Flutter, because Flutter apps constantly work with typed data such as:

- `String` for titles, names, labels
- `int` for item counts and indexes
- `double` for prices, ratings, spacing values
- `bool` for UI states like loading, enabled, selected
- `final` for immutable widget fields and models

If you build strong habits here, your future Flutter code will be much cleaner.
