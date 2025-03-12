## Assignment 28: Promise Assignment

**Objective:**  
Utilize Scala’s `Promise` to create a controlled asynchronous computation that can be externally completed, demonstrating a key pattern in asynchronous coordination.

**Learning Outcomes:**  
- Understand the relationship between `Promise` and `Future` in Scala.  
- Learn how to create, complete, and transform Promises in response to external events or callbacks.  
- Gain practical experience in coordinating asynchronous operations with Promises.

**Tasks:**  
- **Promise Creation:** Implement a function that returns a `Future` along with its corresponding `Promise`.  
- **External Completion:** Simulate an external event (e.g., a delayed callback, user input, or a network signal) that triggers the completion of the Promise.  
- **Error and Success Cases:** Demonstrate how to complete a Promise successfully as well as how to handle failure scenarios by completing it with an exception.  
- **Chaining Operations:** Use combinators to chain further asynchronous operations once the Promise is completed.

**Validation:**  
- Write unit tests covering scenarios where the Promise is completed successfully and where it fails with an exception.  
- Validate that the `Future` derived from the Promise correctly reflects its completed state.  
- Include tests that simulate concurrent attempts to complete the Promise and verify that only the first completion is effective.
