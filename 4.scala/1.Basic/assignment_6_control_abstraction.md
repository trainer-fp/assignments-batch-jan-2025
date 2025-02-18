
# Assignment 6: Control Abstraction

## Objective
Learn to abstract control patterns using higher-order functions.

## Learning Outcomes
- Implement custom control structures.
- Understand the use of call-by-name parameters.
- Create functions that accept other functions as parameters.

## Tasks

### 1. Custom Control Structure
- Implement a function `repeat(n: Int)(block: => Unit)` that executes a code block `n` times.

### 2. Resource Management
- Create a function `using(resource: Resource)(block: Resource => Unit)` to manage resource acquisition and release.

### 3. Validation
- Unit tests should confirm that `repeat` executes the block the correct number of times.
- Ensure that `using` properly manages resources.
