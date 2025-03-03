## Assignment 20: Using Option in Scala

**Objective:**  
Develop safe handling of nullable or missing values by leveraging Scala’s `Option` type.

**Learning Outcomes:**  
- Understand the concept of `Option` and its use in representing optional values.  
- Use pattern matching to handle `Some` and `None` cases.  
- Write functions that return `Option` to avoid null-related errors.

**Tasks:**  
- Implement a function that retrieves an element from a collection by index and returns it as an `Option[T]`.  
- Create a method that transforms the optional value using `map` and `flatMap`.  
- Demonstrate safe chaining of operations on optional values with for-comprehensions.

**Validation:**  
- Write unit tests that verify correct behavior when values are present (`Some`) and when they are absent (`None`).  
- Ensure that pattern matching correctly distinguishes between both cases.
