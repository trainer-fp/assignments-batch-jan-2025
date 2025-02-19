
# Assignment 8: Traits

## Objective
Understand how to use traits for code reuse and multiple inheritance.

## Learning Outcomes
- Define and implement traits.
- Mix traits into classes.
- Resolve conflicts when multiple traits have the same method.

## Tasks

### 1. Define Traits
- Create traits `Flying` and `Swimming` with methods `fly` and `swim`.

### 2. Mixing Traits
- Implement classes `Duck` and `Penguin` that mix in `Flying` and `Swimming` appropriately.

### 3. Method Conflict Resolution
- If two traits define the same method, demonstrate how to resolve the conflict.

### 4. Validation
- Unit tests should confirm that `Duck` can both fly and swim, while `Penguin` can only swim.
- Ensure that method conflicts are resolved correctly.
