# Day 2: Advanced SQL & Database Schema Design - Exercises

This document contains exercises designed to reinforce the concepts learned in **Advanced SQL Queries, Transactions & ACID, Database Schema Design, Normalization, and Indexing**. Completing these assignments will help you develop a deeper understanding of database management.
`
---

## Table of Contents

1. [Advanced SQL Queries](#advanced-sql-queries)
   - [Joins](#joins)
     - INNER JOIN
     - LEFT JOIN
     - RIGHT JOIN
   - [Grouping and Aggregation](#grouping-and-aggregation)
   - [Aggregate Functions](#aggregate-functions)
2. [Transactions and ACID Properties](#transactions-and-acid-properties)
   - [ACID Explained](#acid-explained)
   - [Transaction Commands: BEGIN, COMMIT, ROLLBACK](#transaction-commands)
3. [Database Schema Design and Normalization](#database-schema-design-and-normalization)
   - [Normalization Basics](#normalization-basics)
     - First Normal Form (1NF)
     - Second Normal Form (2NF)
     - Third Normal Form (3NF)
   - [Handling Relationships](#handling-relationships)
     - One-to-Many Relationships
     - Many-to-Many Relationships
4. [Indexing](#indexing)
5. [Additional Resources](#additional-resources)

---

## Advanced SQL Queries

### Joins

#### Assignment 1: Using INNER JOIN
- Create two tables: `students(student_id, name, age)` and `courses(course_id, course_name, student_id)`.
- Write an **INNER JOIN** query to fetch students along with the courses they are enrolled in.
- Modify the query to return only students enrolled in the "Mathematics" course.

#### Assignment 2: Using LEFT JOIN
- Extend the previous example by ensuring all students appear in the result, even those not enrolled in any course.

#### Assignment 3: Using RIGHT JOIN
- Write a **RIGHT JOIN** query to list all courses along with the students enrolled. Ensure courses with no students also appear.

---

### Grouping and Aggregation

#### Assignment 4: Employee Analysis
- Create a table `employees(employee_id, name, department, salary)`.
- Write a **GROUP BY** query to find the total number of employees per department.
- Modify the query to only show departments where the employee count is more than 5 (**HAVING** clause).

#### Assignment 5: Sales Summary
- Create a table `sales(sale_id, customer_id, amount, sale_date)`.
- Write a query to calculate:
  - The total sales per month.
  - The average sale amount per customer.

---

### Aggregate Functions

#### Assignment 6: Product Data Analysis
- Create a table `products(product_id, category, price, stock_quantity)`.
- Write queries to:
  - Find the most expensive product.
  - Calculate the total stock value (SUM of price * stock_quantity).
  - Find the average product price per category.

---

## Transactions and ACID Properties

### ACID Explained

#### Assignment 7: Banking Transactions
- Create a `bank_accounts(account_id, customer_name, balance)` table.
- Simulate a money transfer between two accounts:
  1. Deduct $100 from one account.
  2. Add $100 to another.
  3. Ensure both updates occur inside a transaction.

#### Assignment 8: Handling Failures with Transactions
- Modify the previous assignment to introduce an intentional error in step 2.
- Use **ROLLBACK** to ensure data consistency.

---

## Database Schema Design and Normalization

### Normalization Basics

#### Assignment 9: Fixing a Poorly Designed Database
- Given the following unnormalized table:

  | OrderID | CustomerName | Products           |
  |---------|--------------|--------------------|
  | 1       | Alice        | Apples, Oranges    |
  | 2       | Bob          | Bananas            |

- Transform this into **First Normal Form (1NF)**.

#### Assignment 10: Applying Second Normal Form (2NF)
- Given a table:

  | OrderID | ProductID | CustomerName | ProductName |
  |---------|-----------|--------------|-------------|
  | 1       | 101       | Alice        | Apples      |
  | 1       | 102       | Alice        | Oranges     |

- Apply **2NF** by splitting into appropriate tables.

#### Assignment 11: Applying Third Normal Form (3NF)
- Given a table:

  | ProductID | ProductName | SupplierID | SupplierName |
  |-----------|-------------|------------|--------------|
  | 101       | Apples      | 201        | FreshFarms   |

- Apply **3NF** by ensuring no transitive dependencies exist.

---

### Handling Relationships

#### Assignment 12: One-to-Many Relationship
- Create a `customers(customer_id, name, email)` table.
- Create an `orders(order_id, customer_id, order_date)` table.
- Establish a **one-to-many** relationship.
- Write a query to get all orders for a given customer.

#### Assignment 13: Many-to-Many Relationship
- Define a **many-to-many** relationship between students and courses.
- Create a junction table `student_courses(student_id, course_id)`.
- Write a query to find all students taking a specific course.

---

## Indexing

### Assignment 14: Creating and Using Indexes
- Create a table `large_dataset(id, name, value)` with **1 million rows**.
- Run a **SELECT WHERE** query without an index and measure the time taken.
- Create an **index** on the `name` column and run the query again.
- Compare the performance and analyze improvements.

### Assignment 15: Unique Index for Data Integrity
- Create a `users(user_id, username, email)` table.
- Ensure **username** and **email** fields have unique indexes.
- Attempt inserting duplicate usernames and emails.
- Observe how the database enforces uniqueness.

---

## Additional Resources

To deepen your understanding, refer to the following:

- **Joins & Aggregations**: [SQL Joins](https://www.w3schools.com/sql/sql_join.asp)
- **Transactions & ACID**: [ACID Transactions Explained](https://www.mongodb.com/resources/basics/databases/acid-transactions)
- **Normalization**: [Database Normalization Basics](https://www.essentialsql.com/database-normalization/)
- **Indexing**: [SQL Indexing Basics](https://www.sqlshack.com/sql-index-basics/)

---

Happy coding! 🚀
