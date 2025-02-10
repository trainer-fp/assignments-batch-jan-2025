# Day 2: Advanced SQL & Database Schema Design

Welcome to Day 2 of our DBMS journey! Today, we dive into advanced SQL query techniques, the fundamentals of transactions with ACID properties, and key concepts in database schema design—including normalization and indexing. These topics are critical for building efficient, reliable, and scalable databases.

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

Joins are essential for combining data from multiple tables based on related columns. They help you answer complex queries by linking tables together.

#### INNER JOIN
- **What it Does:** Returns only the records where there is a match in both tables.
- **Example:**
  ```sql
  SELECT employees.name, departments.department_name
  FROM employees
  INNER JOIN departments 
    ON employees.department_id = departments.department_id;
  ```
  *This query retrieves the names of employees along with their department names, but only for employees that belong to a department.*

#### LEFT JOIN (LEFT OUTER JOIN)
- **What it Does:** Returns all records from the left table and the matching records from the right table. If there is no match, the result is NULL on the right side.
- **Example:**
  ```sql
  SELECT employees.name, orders.order_id
  FROM employees
  LEFT JOIN orders 
    ON employees.employee_id = orders.employee_id;
  ```
  *This query shows all employees, including those who may not have any orders.*

#### RIGHT JOIN (RIGHT OUTER JOIN)
- **What it Does:** Returns all records from the right table and the matching records from the left table. If there is no match, the result is NULL on the left side.
- **Example:**
  ```sql
  SELECT employees.name, orders.order_id
  FROM employees
  RIGHT JOIN orders 
    ON employees.employee_id = orders.employee_id;
  ```
  *This query returns all orders, even if some orders are not linked to an employee.*

---

### Grouping and Aggregation

Grouping allows you to summarize data, which is useful for generating reports and insights.

#### GROUP BY
- **What it Does:** Groups rows that have the same values in specified columns so aggregate functions can be applied to each group.
- **Example:**
  ```sql
  SELECT department_id, COUNT(employee_id) AS num_employees
  FROM employees
  GROUP BY department_id;
  ```
  *This query counts the number of employees in each department.*

#### HAVING
- **What it Does:** Filters groups after the aggregation has been applied. It works like the WHERE clause but for groups.
- **Example:**
  ```sql
  SELECT department_id, COUNT(employee_id) AS num_employees
  FROM employees
  GROUP BY department_id
  HAVING COUNT(employee_id) > 10;
  ```
  *This query returns only those departments that have more than 10 employees.*

---

### Aggregate Functions

Aggregate functions perform calculations on sets of rows and return a single value. They are critical for summarizing data.

- **COUNT()**: Returns the number of rows.
  ```sql
  SELECT COUNT(*) AS total_orders FROM orders;
  ```
- **SUM()**: Returns the total sum of a numeric column.
  ```sql
  SELECT SUM(amount) AS total_sales FROM sales;
  ```
- **AVG()**: Returns the average of a numeric column.
  ```sql
  SELECT AVG(salary) AS average_salary FROM employees;
  ```
- **MIN() / MAX()**: Returns the minimum or maximum value.
  ```sql
  SELECT MIN(price) AS lowest_price, MAX(price) AS highest_price FROM products;
  ```

---

## Transactions and ACID Properties

Transactions ensure that a series of operations are executed reliably and maintain data integrity.

### ACID Explained

ACID stands for:
- **Atomicity:** All operations in a transaction are treated as a single unit. If any part fails, the entire transaction fails.
- **Consistency:** A transaction must leave the database in a consistent state, following all rules and constraints.
- **Isolation:** Transactions are executed independently without interference from concurrent operations.
- **Durability:** Once a transaction is committed, its changes are permanent, even in the case of a system failure.

### Transaction Commands: BEGIN, COMMIT, ROLLBACK

- **BEGIN**: Starts a new transaction.
  ```sql
  BEGIN;
  ```
- **COMMIT**: Saves all changes made during the transaction.
  ```sql
  COMMIT;
  ```
- **ROLLBACK**: Reverts all changes if an error occurs during the transaction.
  ```sql
  ROLLBACK;
  ```

---

## Database Schema Design and Normalization

Normalization is the process of structuring a database to minimize redundancy and improve integrity.

### Normalization Basics

#### First Normal Form (1NF)
- **Goal:** Ensure each column contains atomic, indivisible values.

#### Second Normal Form (2NF)
- **Goal:** Remove partial dependencies so that non-key attributes depend on the entire primary key.

#### Third Normal Form (3NF)
- **Goal:** Remove transitive dependencies, ensuring non-key attributes depend solely on the primary key.

---

## Indexing

Indexes improve the speed of data retrieval.

### When to Use Indexes
- **Frequent Query Filtering**
- **High Read Frequency**
- **Sorting Performance Improvements**

---

## Additional Resources

- **[SQL Joins](https://www.w3schools.com/sql/sql_join.asp)**
- **[ACID Transactions Explained](https://www.mongodb.com/resources/basics/databases/acid-transactions)**
- **[Database Normalization Basics](https://www.essentialsql.com/database-normalization/)**
