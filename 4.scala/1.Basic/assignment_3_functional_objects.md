
# Assignment 3: Functional Objects

## Objective
Learn about immutable objects and how to implement functional programming principles in Scala.

## Learning Outcomes
- Create immutable classes.
- Understand the benefits of immutability.
- Implement methods that return new instances rather than modifying existing ones.

## Tasks

### 1. Immutable Point Class
- Create a case class `Point(x: Int, y: Int)`.
- Implement a method `move(dx: Int, dy: Int): Point` that returns a new `Point` with updated coordinates.

### 2. Testing Immutability
- Attempt to modify the properties of a `Point` instance and observe the compiler error.

### 3. Validation
- Unit tests should confirm that `move` returns a new `Point` instance.
- Verify that properties of a case class are immutable.
