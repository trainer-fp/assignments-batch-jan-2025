## Assignment 22: Handling Exceptions with Try

**Objective:**  
Capture and manage exceptions in a functional style using Scala’s `Try` type.

**Learning Outcomes:**  
- Understand how `Try` encapsulates computations that may throw exceptions, producing `Success` or `Failure`.  
- Use `Try` to safely execute potentially unsafe operations without crashing the application.  
- Apply functional combinators to transform and chain operations on `Try` values.

**Tasks:**  
- Wrap a computation that might throw an exception inside a `Try` block.  
- Implement functions that operate on `Try` values using methods like `map`, `flatMap`, and pattern matching.  
- Demonstrate error recovery by using `recover` or `recoverWith` to provide fallback behavior in case of a failure.

**Validation:**  
- Write unit tests that simulate both successful executions (yielding `Success`) and exceptional cases (yielding `Failure`).  
- Ensure that the exception handling mechanism gracefully recovers from errors, providing meaningful output or fallback values.
