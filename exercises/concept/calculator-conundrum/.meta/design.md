# Design

## Learning Objectives

- Know the concept of exception handling in Java.
- Know how and when to throw an exception.
- Know how to catch an exception.

## Out of scope

- The `finally` keyword.

## Concepts

- `exceptions`: know what exceptions are, how and when to throw an exception, know how to catch an exception.

## Prerequisites

- `conditionals-if`: know how to do conditional logic.
- `switch-statement`: know how to work with a `switch` statement.

## Analyzer Comments for CalculatorConundrum.calculate()

### Comments for Code Validation

1. **Essential: Handle valid operations**
   - Ensure that the method handles valid operations (`+`, `*`, `/`) and returns the result in the format `operand1 operation operand2 = result`. This is critical for meeting the exercise requirements.

2. **Essential: Handle `null` operation argument**
   - When the `operation` argument is `null`, an `IllegalArgumentException` should be thrown with the message "Operation cannot be null". This ensures the method gracefully handles invalid inputs.

3. **Essential: Handle empty operation argument**
   - If the `operation` argument is an empty string (`""`), an `IllegalArgumentException` should be thrown with the message "Operation cannot be empty". This guards against incorrect user input.

4. **Essential: Handle unsupported operations**
   - For operations other than `+`, `*`, or `/`, the method should throw an `IllegalOperationException` with the message `"Operation '{operation}' does not exist"`. This prevents execution with invalid operations.

5. **Essential: Handle division by zero**
   - If a division by zero occurs, the method should catch the `ArithmeticException` and rethrow it as an `IllegalOperationException` with the message `"Division by zero is not allowed"`. This helps maintain robust error handling.

### Actionable Suggestions

1. **Actionable: Simplify operation checks**
   - If using multiple `if/else` statements to check for valid operations, consider using a `switch` statement for improved readability and clarity.

2. **Actionable: Consolidate exception handling**
   - If separate exception blocks are used for different operations, consider consolidating them into a single block where appropriate to reduce redundancy.

### Celebratory Comments

1. **Celebratory: Handle invalid inputs with exceptions**
   - Great job implementing appropriate exception handling for invalid inputs such as `null`, empty, and unsupported operations. This is key to making the calculator robust and user-friendly.

2. **Celebratory: Division by zero handled effectively**
   - Excellent work catching division by zero errors and chaining the `ArithmeticException` to a custom `IllegalOperationException`. This approach provides clear feedback to the user.
