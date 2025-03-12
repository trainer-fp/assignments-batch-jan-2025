## Assignment 26: Future Hard Assignment

**Objective:**  
Design and implement a complex asynchronous pipeline using Scala’s Futures that involves multiple stages of processing with dependencies, error propagation, and cancellation support.

**Learning Outcomes:**  
- Master the composition of multiple asynchronous operations using combinators (`flatMap`, `map`, `zip`, etc.).  
- Handle errors gracefully across complex Future chains, ensuring robust propagation and recovery.  
- Understand strategies for cancellation and timeouts in asynchronous workflows.

**Tasks:**  
- **Multi-Stage Pipeline:** Create a multi-step pipeline where the output of one Future feeds into the next stage.  
- **Error Propagation:** Implement comprehensive error handling so that if any stage fails, the pipeline responds appropriately (e.g., using `recoverWith`).  
- **Timeouts and Cancellation:** Add support for timeouts in each stage of the pipeline, and demonstrate how to cancel long-running tasks.  
- **Integration:** Combine I/O-bound tasks (e.g., network calls or file operations) with CPU-bound computations to simulate a realistic processing pipeline.

**Validation:**  
- Develop integration tests that simulate different failure scenarios and validate proper error propagation and recovery.  
- Measure performance metrics (latency, throughput) of the pipeline under various loads.  
- Document cases where cancellation and timeout mechanisms are triggered, ensuring that the pipeline cleans up resources appropriately.
