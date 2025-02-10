# Using Supabase Postgres for Your Exercises


## What is Supabase?
Supabase is an open-source backend-as-a-service that provides a powerful PostgreSQL database
along with authentication, storage, and real-time capabilities.
## Step 1: Sign Up and Create a New Project
1. Go to the Supabase website (https://supabase.com/) and sign up.
2. Click "New Project" and set a name, password, and region.
3. Wait for the setup to complete.
## Step 2: Accessing Your PostgreSQL Database in Supabase
### Using the Supabase Dashboard
1. Navigate to "SQL Editor" in the Supabase dashboard.
2. Run SQL commands to create tables and manage data.
Example:
```sql
CREATE TABLE users (
user_id SERIAL PRIMARY KEY,
username VARCHAR(50) NOT NULL,
email VARCHAR(100) NOT NULL,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
### Connecting with a PostgreSQL Client (Optional)
1. Find your database connection details under "Settings" > "Database".
2. Use a PostgreSQL client (pgAdmin, DBeaver, or `psql` CLI) to connect.
Example `psql` command:
```bash
psql "postgres://<user>:<password>@<host>:<port>/<database>"
```
## Step 3: Working with Your Supabase PostgreSQL Database
### Inserting Data
```sql
INSERT INTO users (username, email)
VALUES ('alice', 'alice@example.com'),
('bob', 'bob@example.com'),
('charlie', 'charlie@example.com');
```
### Querying Data
- Select All Users:
```sql
SELECT * FROM users;
```
- Select Specific Columns:
```sql
SELECT username, email FROM users;
```
- Filter Data:
```sql
SELECT * FROM users WHERE username = 'alice';
```
- Order and Limit Results:
```sql
SELECT * FROM users ORDER BY created_at DESC LIMIT 2;
```
## Step 4: Next Steps
- Try out different SQL commands in the SQL Editor.
- Read PostgreSQL documentation (https://www.postgresql.org/docs/) for advanced topics.
- Explore Supabase documentation (https://supabase.com/docs) for additional features.
## Helpful Tips for Beginners
- Start Simple: Begin with basic commands and gradually try more complex queries.
- Read Error Messages: Error messages often point you directly to the issue.
- Practice Regularly: The more you use SQL, the more comfortable you'll become.

