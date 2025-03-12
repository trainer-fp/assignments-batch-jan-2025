## Assignment 24: Future Assignment - 1

**Objective:**  
Build a simple asynchronous application using Scala’s `Future` along with a custom `ExecutionContext` to better understand thread management and performance tuning.

**Learning Outcomes:**  
- Learn how to create a custom `ExecutionContext` using a configurable thread pool.  
- Understand how the execution context influences the behavior and performance of Futures.  
- Gain experience in executing asynchronous tasks and comparing performance against Scala’s default context.

**Tasks:**  
- **Custom ExecutionContext:** Create a custom `ExecutionContext` backed by a configurable thread pool.  
- **Simple Future:** Implement a basic function that executes a computation asynchronously using your custom context.  
- **Comparison:** Measure the performance of your custom execution context against Scala’s default context using simple benchmarks.  
- **Logging and Monitoring:** Integrate logging to track thread usage and task execution times.

**Validation:**  
- Write unit tests to ensure that asynchronous tasks complete correctly using the custom context.  
- Benchmark and document the differences between the custom and default execution contexts.  
- Verify that the custom thread pool properly limits the number of concurrent threads and handles queued tasks as expected.

---