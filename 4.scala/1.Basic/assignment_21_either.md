## Assignment 21: Leveraging Either for Error Handling

**Objective:**  
Implement robust error handling by using Scala’s `Either` type to represent computations that may succeed or fail.

**Learning Outcomes:**  
- Understand the usage of `Either` to encapsulate a result that can be a success (`Right`) or an error (`Left`).  
- Implement functions that return `Either[String, T]` to convey error messages on failure.  
- Use combinators like `map`, `flatMap`, and for-comprehensions to chain operations while handling errors gracefully.

**Tasks:**  
- Create a function that processes input data and returns an `Either[String, T]`, where the error case is signified by a `Left` containing an error message.  
- Chain multiple computations that may fail, ensuring that the error propagates correctly through the chain.  
- Integrate error handling into a small-scale application or module, demonstrating how to recover from errors.

**Validation:**  
- Develop unit tests covering both success (returning `Right`) and failure (returning `Left`) cases.  
- Test that chained operations correctly short-circuit on error, preserving the original error message.
