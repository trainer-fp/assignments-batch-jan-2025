
# Assignment 18: Givens

## Objective
Understand and use the `given` keyword for defining implicit values.

## Learning Outcomes
- Define implicit values using `given`.
- Use context parameters with `using`.
- Apply context bounds to simplify function signatures.

## Tasks

### 1. Given Instances
- Provide a `given` instance of `Ordering` for a custom class.

### 2. Context Parameters
- Write a function that sorts a list of custom objects using the implicit `Ordering`.

### 3. Context Bounds
- Refactor the function to use a context bound `[T: Ordering]`.

### 4. Validation
- Unit tests should confirm that sorting works with custom types.
- Verify that implicit values are correctly resolved.
