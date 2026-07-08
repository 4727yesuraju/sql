# SQL Keywords

> "SQL keywords are reserved words that tell the database what operation to perform."

---

# 📖 What are SQL Keywords?

SQL **Keywords** are **reserved words** that have a special meaning in SQL.

They are used to perform operations like:

- Creating databases
- Creating tables
- Retrieving data
- Inserting data
- Updating data
- Deleting data
- Filtering records
- Sorting results
- Managing permissions

Think of SQL keywords as **commands** you give to the database.

Examples:

- SELECT
- FROM
- WHERE
- INSERT
- UPDATE
- DELETE
- CREATE
- ALTER
- DROP

---

# 🤔 Why are SQL Keywords Needed?

Imagine you walk into a restaurant.

You tell the waiter:

> "Bring me a pizza."

The waiter understands your request because you're using meaningful words.

Similarly, a database understands your request because you use SQL keywords.

Example:

```sql
SELECT *
FROM Employee;
```

Here,

- **SELECT** → tells the database what to retrieve.
- **FROM** → tells the database where to retrieve it from.

Without keywords, the database wouldn't know what operation you want to perform.

---

# 🌍 Real-world Example

Suppose you're building an Amazon application.

A customer logs in.

The application needs to:

- Show products
- Save orders
- Update inventory
- Delete cancelled orders

The backend sends SQL queries like:

```sql
SELECT *
FROM Products;
```

```sql
INSERT INTO Orders (...);
```

```sql
UPDATE Products
SET stock = stock - 1
WHERE product_id = 101;
```

```sql
DELETE FROM Cart
WHERE customer_id = 5;
```

Every query is built using SQL keywords.

---

# 🧠 Interview Explanation

### What are SQL Keywords?

SQL keywords are reserved words used to perform specific operations on a relational database.

They define what action the database should perform, such as retrieving, inserting, updating, deleting, or modifying data and database objects.

---

### Interview Answer (30 Seconds)

> SQL keywords are predefined reserved words used to communicate with a relational database. They instruct the database to perform operations such as creating tables, retrieving data, inserting records, updating data, deleting records, filtering results, sorting output, and managing database objects. Examples include SELECT, INSERT, UPDATE, DELETE, CREATE, ALTER, and DROP.

---

# 🗂 Categories of SQL Keywords

Instead of memorizing hundreds of keywords, group them by purpose.

---

## 1️⃣ Data Query Keywords (Retrieve Data)

| Keyword  | Purpose                 |
| -------- | ----------------------- |
| SELECT   | Retrieve data           |
| FROM     | Specify table           |
| WHERE    | Filter rows             |
| DISTINCT | Remove duplicates       |
| ORDER BY | Sort results            |
| GROUP BY | Group rows              |
| HAVING   | Filter grouped data     |
| LIMIT    | Restrict number of rows |

Example:

```sql
SELECT name
FROM Employee
WHERE salary > 50000
ORDER BY salary DESC;
```

---

## 2️⃣ Data Manipulation Keywords (DML)

| Keyword | Purpose     |
| ------- | ----------- |
| INSERT  | Add data    |
| UPDATE  | Modify data |
| DELETE  | Remove data |

Example:

```sql
INSERT INTO Employee
VALUES (1,'John',50000);
```

---

## 3️⃣ Data Definition Keywords (DDL)

| Keyword  | Purpose         |
| -------- | --------------- |
| CREATE   | Create objects  |
| ALTER    | Modify objects  |
| DROP     | Delete objects  |
| TRUNCATE | Remove all rows |
| RENAME   | Rename object   |

Example:

```sql
CREATE TABLE Employee(
id INT,
name VARCHAR(100)
);
```

---

## 4️⃣ Constraints Keywords

| Keyword     | Purpose             |
| ----------- | ------------------- |
| PRIMARY KEY | Unique identifier   |
| FOREIGN KEY | Relationship        |
| UNIQUE      | No duplicate values |
| NOT NULL    | Value required      |
| CHECK       | Restrict values     |
| DEFAULT     | Default value       |

---

## 5️⃣ Transaction Keywords

| Keyword   | Purpose           |
| --------- | ----------------- |
| BEGIN     | Start transaction |
| COMMIT    | Save changes      |
| ROLLBACK  | Undo changes      |
| SAVEPOINT | Partial rollback  |

---

## 6️⃣ Join Keywords

| Keyword         | Purpose           |
| --------------- | ----------------- |
| JOIN            | Combine tables    |
| INNER JOIN      | Matching rows     |
| LEFT JOIN       | All left rows     |
| RIGHT JOIN      | All right rows    |
| FULL OUTER JOIN | All rows          |
| CROSS JOIN      | Cartesian product |

---

# ✍️ Syntax

## SELECT

```sql
SELECT *
FROM Employee;
```

---

## INSERT

```sql
INSERT INTO Employee
VALUES (1,'John',50000);
```

---

## UPDATE

```sql
UPDATE Employee
SET salary=60000
WHERE id=1;
```

---

## DELETE

```sql
DELETE FROM Employee
WHERE id=1;
```

---

## CREATE

```sql
CREATE TABLE Employee(
id INT,
name VARCHAR(100)
);
```

---

# 💻 Example Queries

## Show all employees

```sql
SELECT *
FROM Employee;
```

---

## Employees earning more than ₹50,000

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

---

## Insert new employee

```sql
INSERT INTO Employee
VALUES (2,'Alice',65000);
```

---

## Update salary

```sql
UPDATE Employee
SET salary=70000
WHERE id=2;
```

---

## Delete employee

```sql
DELETE FROM Employee
WHERE id=2;
```

---

# ❓ Common Interview Questions

### Q1. What are SQL keywords?

Reserved words used to perform database operations.

---

### Q2. Why are SQL keywords called reserved words?

Because they have predefined meanings and are recognized by the SQL parser.

---

### Q3. Are SQL keywords case-sensitive?

Generally, **No**.

These are equivalent:

```sql
SELECT * FROM Employee;
```

```sql
select * from Employee;
```

However, using uppercase for keywords is a common convention because it improves readability.

---

### Q4. Can SQL keywords be used as column names?

Generally, avoid it.

If necessary, they must usually be quoted according to the database system.

Example:

```sql
SELECT "order"
FROM Sales;
```

---

### Q5. Which SQL keywords are used most frequently?

- SELECT
- FROM
- WHERE
- INSERT
- UPDATE
- DELETE
- CREATE
- ALTER
- DROP
- JOIN
- GROUP BY
- ORDER BY

---

# 🧩 Interview Follow-up Questions

### Q1. How many SQL keywords are there?

There is no fixed number.

Different database systems support SQL standards and also add their own keywords.

---

### Q2. What is the most commonly used SQL keyword?

**SELECT**, because retrieving data is one of the most frequent database operations.

---

### Q3. Are SQL keywords the same in PostgreSQL, MySQL, Oracle, and SQL Server?

Most common keywords (SELECT, INSERT, UPDATE, DELETE, CREATE, etc.) are standardized.

However, some advanced features and keywords are database-specific.

---

### Q4. Is LIMIT an SQL standard keyword?

`LIMIT` is supported by PostgreSQL and MySQL.

SQL Server uses `TOP`, while modern SQL standards also define `FETCH FIRST`.

---

### Q5. How can I remember SQL keywords?

Instead of memorizing them alphabetically, group them by purpose:

- Querying
- Manipulating data
- Defining database objects
- Transactions
- Constraints
- Joins

This makes them much easier to learn and use.

---

# 📝 Practice Exercises

### Exercise 1

Write a query using:

- SELECT
- FROM

---

### Exercise 2

Retrieve employees with salary greater than ₹60,000.

---

### Exercise 3

Insert three new employees.

---

### Exercise 4

Update one employee's salary.

---

### Exercise 5

Delete one employee.

---

### Exercise 6

Create a table named `Student`.

---

# ⚠️ Common Mistakes

### ❌ Thinking keywords are functions

Keywords are commands that define SQL statements.

Functions (such as `COUNT()` or `MAX()`) perform calculations or return values.

---

### ❌ Writing UPDATE or DELETE without WHERE

```sql
UPDATE Employee
SET salary = 50000;
```

Updates every row.

---

### ❌ Using reserved words as table or column names

Avoid names like:

- SELECT
- ORDER
- GROUP

They can lead to confusion or require quoting.

---

### ❌ Memorizing keywords without understanding their purpose

Learn what each keyword does instead of memorizing a long list.

---

# 🔁 Revision Summary

✅ SQL keywords are reserved words.

✅ They tell the database what operation to perform.

✅ They are grouped into categories such as:

- Data Query (SELECT)
- Data Manipulation (INSERT, UPDATE, DELETE)
- Data Definition (CREATE, ALTER, DROP)
- Constraints
- Transactions
- Joins

✅ Most SQL keywords are part of the SQL standard.

---

# 💡 Key Takeaways

- SQL keywords are the building blocks of SQL queries.
- Learn keywords by **category**, not by memorizing a list.
- Most SQL databases share the same core keywords.
- Understanding what each keyword does is more important than memorizing every keyword.
- Mastering the core SQL keywords will help you read, write, and explain SQL queries confidently.
