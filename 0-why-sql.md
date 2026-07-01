# Why SQL?

> "Database stores data, SQL communicates with the database."

---

# 📖 What is SQL?

**SQL (Structured Query Language)** is a standard language used to communicate with **Relational Databases (RDBMS)**.

It is used to:

- Create databases
- Create tables
- Insert data
- Retrieve data
- Update data
- Delete data
- Manage relationships
- Control user permissions

Popular SQL Databases:

- PostgreSQL
- MySQL
- Oracle
- SQL Server
- SQLite

---

# 🤔 Why is SQL Needed?

Imagine you're building an application like **Amazon**.

Millions of users:

- Create accounts
- Place orders
- Make payments
- Track deliveries

Where should all this information be stored?

Not in variables.

Variables disappear when the application stops.

We need permanent storage.

That's why we use a **Database**.

But simply storing data isn't enough.

We also need a way to:

- Save data
- Read data
- Update data
- Delete data
- Search data quickly

SQL is the language that allows us to perform all these operations.

Without SQL, communicating with a relational database would be extremely difficult.

---

# 🌍 Real-world Example

Suppose a customer places an order on Amazon.

The application performs several SQL operations:

- Save customer details
- Save order details
- Reduce product stock
- Generate invoice
- Show order history

Example:

Customer clicks:

> "Show My Orders"

Backend executes:

```sql
SELECT *
FROM Orders
WHERE customer_id = 101;
```

Without SQL, applications like Amazon, Netflix, Flipkart, Swiggy, Banking Systems, Hospital Management Systems, and Railway Reservation Systems wouldn't be able to manage data efficiently.

---

# 🧠 Interview Explanation

### What is SQL?

SQL (Structured Query Language) is a standard language used to communicate with relational databases.

It allows us to:

- Create databases
- Create tables
- Insert data
- Retrieve data
- Update data
- Delete data
- Manage relationships
- Control permissions

**Interview Answer (30 seconds):**

> SQL stands for Structured Query Language. It is a standard language used to communicate with relational databases. Using SQL, we can create databases and tables, insert, retrieve, update, and delete data, define relationships between tables, and manage user permissions. It is supported by databases such as PostgreSQL, MySQL, Oracle, SQL Server, and SQLite.

---

# ✍️ Basic Syntax

## Create Table

```sql
CREATE TABLE Employee (
    id INT,
    name VARCHAR(100),
    salary INT
);
```

---

## Insert Data

```sql
INSERT INTO Employee
VALUES (1, 'John', 50000);
```

---

## Read Data

```sql
SELECT *
FROM Employee;
```

---

## Update Data

```sql
UPDATE Employee
SET salary = 60000
WHERE id = 1;
```

---

## Delete Data

```sql
DELETE FROM Employee
WHERE id = 1;
```

---

# 💻 Example Queries

## Find all employees

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

## Count employees

```sql
SELECT COUNT(*)
FROM Employee;
```

---

## Highest salary

```sql
SELECT MAX(salary)
FROM Employee;
```

---

# ❓ Common Interview Questions

### Q1. What is SQL?

SQL is a standard language used to interact with relational databases.

---

### Q2. Why do we use SQL?

To perform CRUD operations (Create, Read, Update, Delete) and manage relational data efficiently.

---

### Q3. Is SQL a programming language?

No.

SQL is a **query language**, not a general-purpose programming language.

---

### Q4. Can SQL create databases?

Yes.

Example:

```sql
CREATE DATABASE CompanyDB;
```

---

### Q5. Which databases use SQL?

- PostgreSQL
- MySQL
- Oracle
- SQL Server
- SQLite

---

# 📝 Practice Exercises

### Exercise 1

Create a table named **Student** with the following columns:

- id
- name
- age

---

### Exercise 2

Insert five student records.

---

### Exercise 3

Display all student records.

---

### Exercise 4

Display students older than 20 years.

---

### Exercise 5

Delete one student record.

---

### Exercise 6

Update one student's age.

---

# ⚠️ Common Mistakes

### ❌ Forgetting WHERE in UPDATE

```sql
UPDATE Employee
SET salary = 50000;
```

**Result:** Updates every employee's salary.

---

### ❌ Forgetting WHERE in DELETE

```sql
DELETE FROM Employee;
```

**Result:** Deletes all rows from the table.

---

### ❌ Confusing SQL with Database

❌ Database = SQL

✅ Database → Stores data

✅ SQL → Communicates with the database

---

### ❌ Thinking SQL is only for SELECT

SQL is also used for:

- CREATE
- INSERT
- UPDATE
- DELETE
- ALTER
- DROP
- TRUNCATE

---

# 🔁 Revision Summary

✅ SQL stands for Structured Query Language.

✅ Used to communicate with relational databases.

✅ Performs CRUD operations.

✅ Creates databases and tables.

✅ Retrieves, inserts, updates, and deletes data.

✅ Manages relationships between tables.

✅ Controls user permissions.

✅ Supported by PostgreSQL, MySQL, Oracle, SQL Server, and SQLite.

---

# 📝 Key Takeaways

- Database stores data.
- SQL communicates with the database.
- SQL is a query language, not a programming language.
- SQL is the foundation of most backend applications.
- Mastering SQL is essential for backend development and technical interviews.



# 🧩 Interview Follow-up Questions

### Q1. What if SQL didn't exist?

Without SQL, there would be no standard language to communicate with relational databases. Every database would require its own custom commands, making development much more difficult.

---

### Q2. Can SQL work without a database?

No.

SQL requires a Database Management System (DBMS/RDBMS) such as PostgreSQL, MySQL, Oracle, or SQL Server to execute its commands.

---

### Q3. Is SQL case-sensitive?

SQL keywords are generally **not case-sensitive**.

These are equivalent:

```sql
SELECT * FROM Employee;
```

```sql
select * from Employee;
```

However, table names and string comparisons may behave differently depending on the database.

---

### Q4. Is SQL a programming language?

No.

SQL is a **declarative query language**. You tell the database **what** you want, not **how** to retrieve it.

---

### Q5. Can SQL be used without a backend language?

Yes.

You can execute SQL directly using database tools such as pgAdmin, MySQL Workbench, or the PostgreSQL terminal.

However, in real applications, backend languages like JavaScript (Node.js), Java, Python, or C# send SQL queries to the database.

---

### Q6. Which companies use SQL?

Almost every company that works with structured data uses SQL, including:

- Google
- Amazon
- Microsoft
- Netflix
- Uber
- Airbnb
- Swiggy
- Flipkart

---

### Q7. Can SQL handle millions of records?

Yes.

Modern databases like PostgreSQL, MySQL, Oracle, and SQL Server are designed to efficiently manage millions or even billions of records using indexes, query optimization, and transactions.

---

### Q8. What is the difference between SQL and a Database?

A **Database** stores data.

**SQL** is the language used to communicate with the database.

Think of it like this:

- 🏦 Database = Bank
- 🗣️ SQL = Language you use to talk to the bank

---

### Q9. Why should a backend developer learn SQL?

Backend developers constantly interact with databases to:

- Store user information
- Authenticate users
- Process orders
- Generate reports
- Manage relationships between data
- Optimize application performance

SQL is one of the core skills for backend development.

---

### Q10. What is one limitation of SQL?

SQL works best with **structured, relational data**.

For highly flexible or schema-less data (such as social media feeds or logs), NoSQL databases like MongoDB may be a better choice.