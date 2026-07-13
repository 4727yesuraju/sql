# What are Relational Databases?

> "A Relational Database stores data in tables and connects those tables using relationships."

---

# 📖 What is a Relational Database?

A **Relational Database (RDBMS)** is a type of database that stores data in the form of **tables (rows and columns)**.

The word **"Relational"** means that **multiple tables are connected (related) to each other** using common fields such as **Primary Keys** and **Foreign Keys**.

Instead of storing everything in one large table, related data is divided into multiple tables, making it easier to organize, manage, and retrieve.

Popular Relational Databases include:

- PostgreSQL
- MySQL
- Oracle
- Microsoft SQL Server
- SQLite

---

# 🤔 Why are Relational Databases Needed?

Imagine you're building an **E-commerce application**.

You have customers placing orders.

Should you store everything in one table?

❌ No.

Example:

| Order ID | Customer Name | Customer Phone | Product | Price |
| -------- | ------------- | -------------- | ------- | ----- |
| 101      | John          | 9876543210     | Laptop  | 70000 |
| 102      | John          | 9876543210     | Mouse   | 800   |

Notice how John's information is repeated multiple times.

Problems:

- Duplicate data
- Wasted storage
- Difficult to update information
- Higher chance of inconsistent data

Instead, divide the data into related tables.

**Customers**

| Customer ID | Name | Phone      |
| ----------- | ---- | ---------- |
| 1           | John | 9876543210 |

**Orders**

| Order ID | Customer ID | Product | Price |
| -------- | ----------- | ------- | ----- |
| 101      | 1           | Laptop  | 70000 |
| 102      | 1           | Mouse   | 800   |

Now the tables are connected using **Customer ID**.

This relationship removes duplicate data and keeps the database organized.

---

# 🌍 Real-world Example

Think about **Amazon**.

Amazon doesn't store customer details with every order.

Instead, it has separate tables like:

- Customers
- Orders
- Products
- Payments
- Addresses

When you open **"My Orders"**, the application combines data from these tables using relationships.

Example:

```
Customers
----------
1  John

Orders
----------
101   Customer_ID = 1

Products
----------
501   Laptop
```

The backend uses SQL JOINs to combine these tables and display complete order information.

Without relationships, managing millions of records would become slow, repetitive, and error-prone.

---

# 🧠 Interview Explanation

### What is a Relational Database?

A Relational Database is a database that stores data in tables consisting of rows and columns.

These tables are connected using relationships, typically through **Primary Keys** and **Foreign Keys**.

This design helps reduce duplicate data, maintain consistency, and retrieve related information efficiently.

---

### Interview Answer (30 seconds)

> A Relational Database stores data in tables made up of rows and columns. The tables are connected using relationships, usually through Primary Keys and Foreign Keys. This approach minimizes data duplication, maintains data integrity, and allows efficient querying using SQL. Popular relational databases include PostgreSQL, MySQL, Oracle, SQL Server, and SQLite.

---

# ✍️ Syntax

## Create Customers Table

```sql
CREATE TABLE Customers (
    customer_id INT PRIMARY KEY,
    name VARCHAR(100),
    phone VARCHAR(15)
);
```

---

## Create Orders Table

```sql
CREATE TABLE Orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    product_name VARCHAR(100),
    price DECIMAL(10,2),
    FOREIGN KEY (customer_id)
    REFERENCES Customers(customer_id)
);
```

---

## Retrieve Customer Orders

```sql
SELECT *
FROM Customers
JOIN Orders
ON Customers.customer_id = Orders.customer_id;
```

---

# 💻 Example Queries

## Show all customers

```sql
SELECT *
FROM Customers;
```

---

## Show all orders

```sql
SELECT *
FROM Orders;
```

---

## Show customer names with their orders

```sql
SELECT Customers.name,
       Orders.product_name
FROM Customers
JOIN Orders
ON Customers.customer_id = Orders.customer_id;
```

---

## Count total orders

```sql
SELECT COUNT(*)
FROM Orders;
```

---

# ❓ Common Interview Questions

### Q1. What is a Relational Database?

A database that stores data in tables and connects those tables using relationships.

---

### Q2. Why is it called a "Relational" database?

Because different tables are related to each other using Primary Keys and Foreign Keys.

---

### Q3. What is a table?

A table is a collection of related data organized into rows and columns.

---

### Q4. What creates the relationship between tables?

Primary Keys and Foreign Keys.

---

### Q5. Which databases are Relational Databases?

- PostgreSQL
- MySQL
- Oracle
- SQL Server
- SQLite

---

# 🧩 Interview Follow-up Questions

### Q1. Why not store everything in one table?

Because it causes:

- Duplicate data
- More storage usage
- Difficult updates
- Poor data consistency

Using multiple related tables keeps data organized and reduces redundancy.

---

### Q2. What is the biggest advantage of Relational Databases?

They reduce duplicate data through relationships and maintain data integrity.

---

### Q3. Can Relational Databases handle millions of records?

Yes.

Databases like PostgreSQL and MySQL are designed to efficiently manage millions or even billions of records using indexes, query optimization, and transactions.

---

### Q4. What is the difference between a Database and a Relational Database?

A **Database** is any system that stores data.

A **Relational Database** stores data in related tables and uses SQL for managing it.

---

### Q5. Are Excel sheets Relational Databases?

No.

Excel stores data in sheets but does not enforce relationships, Primary Keys, Foreign Keys, or SQL-based querying like an RDBMS.

---

# 📝 Practice Exercises

### Exercise 1

Create a `Customers` table.

---

### Exercise 2

Create an `Orders` table with a Foreign Key.

---

### Exercise 3

Insert three customers.

---

### Exercise 4

Insert five orders.

---

### Exercise 5

Retrieve customer names along with their orders using a JOIN.

---

### Exercise 6

Find the customer who placed the most orders.

---

# ⚠️ Common Mistakes

### ❌ Thinking a Relational Database is just a collection of tables.

A Relational Database is **more than tables**—the key idea is the **relationships** between those tables.

---

### ❌ Storing duplicate information

Avoid repeating the same customer or product details in multiple rows.

Instead, create separate tables and relate them.

---

### ❌ Forgetting Primary Keys

Every table should ideally have a Primary Key to uniquely identify each row.

---

### ❌ Confusing Primary Key and Foreign Key

- **Primary Key** → Uniquely identifies a row in its own table.
- **Foreign Key** → References the Primary Key of another table to create a relationship.

---

# 🔁 Revision Summary

✅ A Relational Database stores data in tables.

✅ Tables are connected using relationships.

✅ Relationships are created using Primary Keys and Foreign Keys.

✅ Reduces duplicate data.

✅ Maintains data consistency and integrity.

✅ Makes querying related data efficient using SQL.

✅ Common Relational Databases include PostgreSQL, MySQL, Oracle, SQL Server, and SQLite.

---

# 📝 Key Takeaways

- Tables store the data.
- Relationships connect the tables.
- Primary Keys uniquely identify rows.
- Foreign Keys create relationships.
- SQL is used to query and manage Relational Databases.
- Relational Databases are the foundation of most backend applications.
