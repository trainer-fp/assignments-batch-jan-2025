# SQL Database Assignment - E-Commerce Data Model

**Duration:** 3-4 hours  
**Tools Required:** [SQL Fiddle](http://sqlfiddle.com/) or any SQL playground  
**Topics Covered:** DDL, DML, Joins, Aggregation, Constraints, Indexes  

---

## Assignment Overview

You’ll design a small e-commerce database schema, populate it with data, and write queries to analyze sales and customer behavior.  
Submit your solutions as:  
1. A GitHub repository with `.sql` files **OR**  
2. SQL Fiddle links for each section.

---

## Database Schema Setup (DDL)

### Tables to Create:
1. **Customers**
   - `customer_id` (Primary Key)
   - `name` (Non-null string)
   - `email` (Unique, non-null string)
   - `join_date` (Date with default = current date)
2. **Products**
   - `product_id` (Primary Key)
   - `product_name` (Non-null string)
   - `price` (Decimal > 0)
3. **Orders**
   - `order_id` (Primary Key)
   - `customer_id` (Foreign Key to Customers)
   - `order_date` (Date with default = current date)
4. **Order_Items**
   - `order_item_id` (Primary Key)
   - `order_id` (Foreign Key to Orders)
   - `product_id` (Foreign Key to Products)
   - `quantity` (Integer ≥ 1)

**Your Tasks:**
1. Write the SQL DDL to create these tables with proper constraints.
2. Create a SQL Fiddle with this schema and share the link.

---

## Data Insertion (DML)

Insert the sample data below using `INSERT` statements:

**Customers:**
| name      | email               |
|-----------|---------------------|
| John Doe  | john@example.com    |
| Jane Smith| jane@example.com    |

**Products:**
| product_name | price |
|--------------|-------|
| Laptop       | 999.99|
| Smartphone   | 499.99|

**Orders & Order_Items:**
- John Doe placed 1 order on 2023-01-01:  
  - 1 Laptop, 2 Smartphones  
- Jane Smith placed 1 order on 2023-01-02:  
  - 3 Laptops  

**Your Tasks:**
1. Write `INSERT` statements for all tables.
2. Add your SQL Fiddle link with the populated data.

---

## Query Exercises

### Part 1: Basic Queries
1. List all customers sorted by `join_date` (newest first).
2. Find all orders placed in January 2023.
3. Calculate the total revenue from all orders.

### Part 2: Joins and Relationships
4. Show all orders with customer names and order dates.
5. List products that have never been ordered.
6. Find the top-spending customer (total spent across all orders).

### Part 3: Data Manipulation
7. Update the price of "Laptop" to `899.99`.
8. Delete all orders placed before 2023-01-02.
9. Add a new product "Headphones" priced at `149.99`.

### Part 4: Advanced Challenges
10. Calculate the average order value per customer.
11. Find products ordered more than 2 times in total.
12. **Bonus:** Create an index to optimize querying orders by `customer_id`.

---

## Submission Guidelines

1. Organize your SQL scripts into sections (e.g., `schema.sql`, `inserts.sql`, `queries.sql`).
2. Test all queries in SQL Fiddle and include working links.
3. Push your work to a GitHub repository or share SQL Fiddle links in a text file.

---

## Resources
- [SQL Fiddle Demo](http://sqlfiddle.com/#!15/212e4/1)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

**Good luck!** 🔍🚀