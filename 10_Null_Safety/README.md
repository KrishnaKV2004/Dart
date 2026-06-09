# Lesson 10: Null Safety

This section teaches one of Dart's most valuable features: null safety.

Null safety helps prevent one of the most common causes of bugs in real software:

- assuming a value exists when it does not

## Topics In This Lesson

1. [Why Null Safety](./Why%20Null%20Safety/README.md)
2. [Nullable Types](./Nullable%20Types/README.md)
3. [Non Nullable Types](./Non%20Nullable%20Types/README.md)
4. [Null Assertion Operator](./Null%20Assertion%20Operator/README.md)
5. [Null Aware Operator](./Null%20Aware%20Operator/README.md)
6. [Late Keyword](./Late%20Keyword/README.md)
7. [Best Practices](./Best%20Practices/README.md)

## Why This Lesson Matters

In real applications, some data is missing sometimes:

- profile photo may not exist
- nickname may be optional
- API field may be absent
- user may not be logged in yet

Without careful null handling, these situations can cause crashes and confusing bugs.

## Senior Developer Mindset For Null Safety

Strong developers do not treat `null` as an inconvenience.
They treat it as part of the data model.

They ask:

- Can this value genuinely be missing?
- If it is missing, what should the app do?
- Should this be nullable, or should the code guarantee it exists?

That mindset leads to safer and clearer code.

## What You Should Learn Here

By the end of this section, you should be able to:

- understand why null safety exists
- mark values as nullable only when appropriate
- work safely with nullable data
- use null-aware operators correctly
- avoid risky null assertion habits

## Flutter Connection

Null safety matters a lot in Flutter because apps constantly deal with:

- async data
- optional user input
- API responses
- delayed initialization
- conditional UI state

Strong null-safety habits make Flutter apps much more reliable.
