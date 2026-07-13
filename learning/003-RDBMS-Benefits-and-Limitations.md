# RDBMS Benefits & Limitations

> "Every technology has strengths and weaknesses. Understanding both helps you choose the right database for the right problem."

---

# 📖 What are the Benefits & Limitations of RDBMS?

An **RDBMS (Relational Database Management System)** stores data in **tables (rows and columns)** and maintains relationships between those tables using **Primary Keys** and **Foreign Keys**.

Like every technology, RDBMS has both **advantages** and **limitations**.

Understanding these helps developers choose the most suitable database for different applications.

Popular RDBMS:

- PostgreSQL
- MySQL
- Oracle
- Microsoft SQL Server
- SQLite

---

# 🤔 Why is it Needed?

Imagine you're building different applications.

### 🏦 Banking Application

Requirements:

- Money transfers
- Account balance
- Transaction history
- High security
- No data loss

An RDBMS is the perfect choice because it guarantees:

- Data consistency
- Transactions
- Security
- Relationships

---

### 📱 Social Media Application

Requirements:

- Billions of posts
- Likes
- Comments
- Messages
- Notifications
- Constantly changing data structure

Here, an RDBMS alone may not always be the best fit. Many companies combine it with NoSQL databases to handle highly flexible and large-scale data efficiently.

**Lesson:**

There is no "best" database.

Choose the database according to your application's requirements.

---

# 🌍 Real-world Example

Imagine Amazon.

It stores:

- Customers
- Products
- Orders
- Payments
- Addresses

Each table is related to another.

When a customer places an order:

1. Customer information is retrieved.
2. Product stock is checked.
3. Payment is processed.
4. Order is created.
5. Inventory is updated.

All of these operations happen inside transactions to maintain data consistency.

This is why RDBMS is widely used in banking, e-commerce, hospitals, and airline reservation systems.

---

# 🧠 Interview Explanation

### What are the benefits of an RDBMS?

An RDBMS provides:

- Structured data storage
- Data integrity
- Relationships between tables
- SQL support
- ACID transactions
- Security
- Reduced data duplication

### What are the limitations?

Some limitations include:

- Fixed schema
- More difficult horizontal scaling
- Less suitable for unstructured data
- Complex JOINs can affect performance
- Schema changes require planning

---

### Interview Answer (60 Seconds)

> An RDBMS stores structured data in related tables using Primary Keys and Foreign Keys. It offers several advantages, including reduced data duplication, strong data integrity, SQL support, ACID transactions, security, and efficient querying. However, it also has limitations such as a fixed schema, more challenging horizontal scaling, and reduced flexibility for handling unstructured data. That's why transactional systems like banking commonly use RDBMS, while applications handling large volumes of flexible data often combine RDBMS with NoSQL databases.

---

# ✅ Benefits of RDBMS

## 1. Reduces Data Duplication

Instead of storing the same customer details repeatedly, RDBMS stores them once and creates relationships.

### Example

Customers

| Customer ID | Name |
| ----------- | ---- |
| 1           | John |

Orders

| Order ID | Customer ID |
| -------- | ----------- |
| 101      | 1           |
| 102      | 1           |

Customer information is stored only once.

---

## 2. Maintains Data Integrity

RDBMS ensures data remains accurate and consistent.

Using:

- Primary Key
- Foreign Key
- NOT NULL
- UNIQUE
- CHECK

Example:

An order cannot reference a customer who doesn't exist.

---

## 3. Supports ACID Transactions

Transactions guarantee that database operations are completed safely.

Example:

During money transfer,

- Money is deducted.
- Money is credited.

If one operation fails,

everything is rolled back.

This prevents inconsistent data.

---

## 4. Supports Relationships

Tables can be connected.

Example:

```
Customers
    │
    │
Orders
    │
    │
Payments
```

Relationships reduce duplicate data and simplify data retrieval.

---

## 5. Powerful SQL Queries

Retrieve exactly the data you need.

Example

```sql
SELECT *
FROM Orders
WHERE price > 5000;
```

---

## 6. Better Security

RDBMS supports:

- User authentication
- Roles
- Permissions
- Access control

Example:

An employee may view customer information but cannot delete it.

---

## 7. Easy Maintenance

Customer information is stored once.

Updating it automatically benefits all related records.

---

## 8. Industry Standard

RDBMS is widely used in:

- Banking
- E-commerce
- Hospital Management
- Airline Reservation
- ERP Systems
- Government Systems

---

# ❌ Limitations of RDBMS

## 1. Fixed Schema

Before storing data, tables must be designed.

Example

Adding a new column:

```sql
ALTER TABLE Employee
ADD email VARCHAR(100);
```

Schema changes may require application updates.

---

## 2. Difficult Horizontal Scaling

As data grows, distributing it across multiple servers is generally more complex than with many NoSQL databases.

---

## 3. Not Ideal for Unstructured Data

RDBMS works best with structured data.

Examples of unstructured data:

- Chat messages
- Images
- Videos
- Social media feeds
- IoT sensor logs

---

## 4. Complex JOIN Queries

Joining many large tables can reduce performance if queries or indexes are not optimized.

---

## 5. Schema Changes Can Be Expensive

Changing production database structures often requires:

- Planning
- Testing
- Data migration
- Downtime (in some cases)

---

## 6. Less Flexible

Frequently changing application requirements may be easier to support with document-based databases.

---

# ✍️ Syntax

## Create Table

```sql
CREATE TABLE Employee (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    salary DECIMAL(10,2)
);
```

---

## Add New Column

```sql
ALTER TABLE Employee
ADD email VARCHAR(100);
```

---

## Retrieve Data

```sql
SELECT *
FROM Employee;
```

---

# 💻 Example Queries

## Show all employees

```sql
SELECT *
FROM Employee;
```

---

## Count employees

```sql
SELECT COUNT(*)
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

## Highest salary

```sql
SELECT MAX(salary)
FROM Employee;
```

---

# ❓ Common Interview Questions

### Q1. What are the benefits of an RDBMS?

- Data integrity
- Reduced duplication
- ACID transactions
- Security
- SQL support
- Relationships

---

### Q2. What are the limitations of an RDBMS?

- Fixed schema
- Difficult horizontal scaling
- Less suitable for unstructured data
- Complex JOINs
- Schema changes

---

### Q3. Why do banks use RDBMS?

Because banks require:

- Consistency
- Transactions
- Security
- Reliability
- ACID compliance

---

### Q4. Why don't social media applications rely only on RDBMS?

Because they handle massive amounts of flexible and rapidly changing data, where NoSQL databases can complement RDBMS.

---

### Q5. Is RDBMS still relevant today?

Yes.

Most enterprise applications continue to rely on RDBMS for structured, transactional data.

---

# 🧩 Interview Follow-up Questions

### Q1. Can RDBMS handle millions of records?

Yes.

With indexing, partitioning, caching, and query optimization, modern RDBMS systems can efficiently manage millions or billions of records.

---

### Q2. Can we use SQL and NoSQL together?

Yes.

Many companies use both.

Example:

- PostgreSQL → Users, Orders, Payments
- MongoDB → Logs, Notifications, Analytics

This is called **Polyglot Persistence**.

---

### Q3. Why isn't NoSQL used everywhere?

Because many applications require:

- Transactions
- Relationships
- Data consistency

These are strengths of an RDBMS.

---

### Q4. Which is better: SQL or NoSQL?

Neither.

The right choice depends on the application's requirements.

---

### Q5. What is the biggest strength of an RDBMS?

Its ability to maintain **data consistency and integrity** while efficiently managing relationships between tables.

---

# 📝 Practice Exercises

### Exercise 1

List five benefits of an RDBMS.

---

### Exercise 2

List five limitations of an RDBMS.

---

### Exercise 3

Explain why a banking system uses an RDBMS.

---

### Exercise 4

Explain why a social media platform may combine RDBMS and NoSQL.

---

### Exercise 5

Create a comparison table between SQL and NoSQL databases.

---

# ⚠️ Common Mistakes

### ❌ Thinking RDBMS is always the best choice

Different applications have different requirements.

---

### ❌ Confusing SQL with RDBMS

- **RDBMS** → Software that stores and manages relational data.
- **SQL** → Language used to interact with the RDBMS.

---

### ❌ Assuming RDBMS cannot scale

Modern RDBMS systems can scale effectively with proper architecture and optimization.

---

### ❌ Believing NoSQL replaces RDBMS

Many real-world systems use both together.

---

# 🔁 Revision Summary

✅ Stores structured data in related tables.

✅ Reduces data duplication.

✅ Maintains data integrity.

✅ Supports SQL queries.

✅ Provides ACID transactions.

✅ Ensures security and access control.

✅ Best for structured and transactional applications.

✅ Less flexible for rapidly changing or unstructured data.

---

# 💡 Key Takeaways

- RDBMS is ideal for structured, relational, and transactional data.
- Its biggest strengths are consistency, integrity, and relationships.
- Its main limitations are fixed schemas and less flexibility for unstructured data.
- Many modern applications combine RDBMS and NoSQL to leverage the strengths of both.
- Always choose a database based on your application's requirements, not popularity.
