## Assignment 25: Future - Directory Search

**Objective:**  
Develop an asynchronous directory search utility that, given a directory path, lists all files in the directory and its subdirectories using Scala Futures.

**Learning Outcomes:**  
- Apply asynchronous programming to perform I/O-bound operations.  
- Use Futures to execute recursive directory searches concurrently.  
- Learn to manage and combine multiple asynchronous tasks efficiently.

**Tasks:**  
- **Recursive File Listing:** Implement a function to recursively traverse a given directory and return a list of file paths.  
- **Asynchronous Execution:** Use Futures to perform the file search concurrently for each subdirectory.  
- **Aggregation:** Combine the results of the asynchronous searches into a single aggregated list of file paths.  
- **Error Handling:** Integrate proper error handling to manage inaccessible directories or I/O errors using combinators like `recover` or `recoverWith`.

**Validation:**  
- Write unit tests that validate correct behavior with various directory structures, including nested subdirectories.  
- Test error scenarios (e.g., non-existent directory, permission issues) to ensure graceful failure and recovery.  
- Measure the performance and responsiveness of the directory search compared to a synchronous implementation.
