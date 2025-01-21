# Uncommon Exception Handling in Scala
This repository demonstrates a potential issue in Scala exception handling related to the use of `IllegalArgumentException`. The core problem stems from directly throwing an exception within a setter method, which might not always be the ideal approach, especially in complex scenarios. While functional, it might differ from alternative approaches like using `Option` or custom exception classes.

## How to Reproduce
1. Clone this repository.
2. Compile and run `Main.scala`.
3. Observe the `IllegalArgumentException` when attempting to set a negative age.

## Potential Improvements
- Using `Option[Int]` for age instead of `Int` to allow for the possibility of an unset or invalid age.
- Creating a custom exception class to provide more context-specific information, making debugging and error handling easier. 
- Using a more sophisticated validation mechanism for the `age` property.

## Additional notes:
The exception handling demonstrated is not inherently wrong, but it's important to consider the context and potential alternatives when deciding on how to handle invalid input.