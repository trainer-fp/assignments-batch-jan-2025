# Databases and SQL Basics

This document covers essential topics on relational databases and SQL. It’s designed to be beginner-friendly and includes resource links for those who want to learn more in depth.

---

## Database Essentials
Relational Database Structure

A relational database organizes data into tables that consist of rows and columns. This structure helps maintain relationships between different data sets.

* Tables: Collections of data entries about a specific subject (e.g., users, orders).
* Rows: Individual records representing an instance of the entity.
* Columns: Attributes that describe each record (such as name, email, or date).

Key Concepts

Understanding these key elements is essential when working with databases:

* **Primary Key**:
    Uniquely identifies each row in a table (e.g., a user_id in a users table).
* **Foreign Key:**
    Links rows in one table to rows in another, establishing relationships between tables.
* **Indexes:**
    Data structures that improve the speed of data retrieval.
* **Constraints:**
    Rules (like NOT NULL or UNIQUE) that maintain data integrity.

--- 

## SQL Basics

### DDL vs. DML

SQL commands fall into two primary categories:

* **DDL (Data Definition Language):***

    Commands that define or modify the structure of the database objects.
    
    Examples:
        
    `CREATE TABLE`
        
    `ALTER TABLE`
        
    `DROP TABLE`

* **DML (Data Manipulation Language):**

    Commands used to manipulate the data within the tables.
    
    Examples:

    `INSERT INTO`
    
    `UPDATE`
    
    `DELETE`
    
    `SELECT`

### Creating and Dropping Tables

**Creating a Table**

Use the CREATE TABLE command to define a new table. For example:

```sql
CREATE TABLE users (
    user_id SERIAL PRIMARY KEY,  -- (Use AUTO_INCREMENT for MySQL)
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

**Dropping a Table**

Remove a table using:

```sql
DROP TABLE IF EXISTS users;
```

### Inserting, Updating, and Deleting Data
**Inserting Data**

Add new rows with the `INSERT INTO` command:

```sql
INSERT INTO users (username, email)
VALUES ('alice', 'alice@example.com'),
       ('bob', 'bob@example.com');
```

### Updating Data

Modify existing data with the `UPDATE` command:
```sql
UPDATE users
SET email = 'bob.new@example.com'
WHERE username = 'bob';
```

### Deleting Data

Remove data with the `DELETE` command:
```sql
DELETE FROM users
WHERE username = 'bob';
```

---

## Simple Queries

### Selecting Data

Retrieve data from a table with the SELECT statement.
Basic `SELECT` Query
```sql
SELECT * FROM users;
```

**Selecting Specific Columns**

```sql
SELECT username, email FROM users;
```

### Filtering, Sorting, and Limiting Results
Filtering with `WHERE`

Filter data using conditions:

```sql
SELECT * FROM users
WHERE username = 'alice';
```

Sorting with `ORDER BY`

Sort the results by a column:
```
SELECT * FROM users
ORDER BY created_at DESC;
```

Limiting Results

Return a subset of rows:
```sql
SELECT * FROM users
ORDER BY created_at DESC
LIMIT 5;
```

Additional Tips:

* Practice writing queries using interactive platforms such as [SQLZoo](https://sqlzoo.net/wiki/SQL_Tutorial) or [SQLFiddle](https://sqlfiddle.com/).

