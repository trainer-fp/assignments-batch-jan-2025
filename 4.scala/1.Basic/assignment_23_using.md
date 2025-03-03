## Assignment 23: Resource Management with Using

**Objective:**  
Demonstrate effective resource management by leveraging Scala’s `Using` construct to safely acquire and release resources, such as files, network connections, or database handles.

**Learning Outcomes:**  
- Understand the risks of resource leaks and the importance of proper resource management.  
- Learn how to use Scala’s `Using` (available in Scala 2.13 and later) to ensure that resources are automatically closed after use.  
- Gain experience integrating error handling with resource management by combining `Using` with functional error-handling constructs like `Try`.

**Tasks:**  
- **File Reading:** Implement a function that reads from a file using `Using`. Ensure that the file is automatically closed after reading, regardless of whether the operation succeeds or fails.  
- **Error Handling:** Enhance the file-reading function to gracefully handle exceptions. Use combinators like `recover` or integrate with `Try` to provide meaningful fallback behavior in case of errors.  
- **Extended Example:** Optionally, extend the assignment to include writing to a file. Implement both read and write operations using `Using` to manage resources effectively.

**Validation:**  
- Write unit tests to confirm that the resource (e.g., file handle) is properly closed after the operation, even when an exception is thrown.  
- Verify that the function behaves correctly in both successful and failure scenarios by simulating file access errors or non-existent files.  
- Include benchmarks or logging to demonstrate that resource acquisition and release occur as expected without any resource leakage.
