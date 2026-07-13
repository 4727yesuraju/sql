# Data Types in SQL

> "A data type tells the database what kind of data a column can store."

---

# 📖 What are Data Types?

A **Data Type** defines the **type of value** that can be stored in a table column.

It tells the database:

- What kind of data is allowed
- How much storage is needed
- How the data should be processed

For example:

- Age → Number
- Name → Text
- Salary → Decimal Number
- Date of Birth → Date
- Is Active → True/False

Every column in a table must have a data type.

---

# 🤔 Why are Data Types Needed?

Imagine you're creating an **Employee** table.

```
Employee

Name
Age
Salary
Joining Date
Email
```

Should the database allow:

```
Age = "Hello"

Salary = "ABC"

Joining Date = "Tomorrow"
```

❌ No.

These values are invalid.

That's why we use **Data Types**.

They ensure that only valid data is stored.

For example:

```
Age → INTEGER

Salary → DECIMAL

Joining Date → DATE
```

Now the database can reject incorrect values and maintain data quality.

---

# 🌍 Real-world Example

Imagine you're building an **Amazon** application.

Customer Table:

| Column          | Data Type     |
| --------------- | ------------- |
| customer_id     | INTEGER       |
| name            | VARCHAR(100)  |
| email           | VARCHAR(255)  |
| age             | INTEGER       |
| balance         | DECIMAL(10,2) |
| created_at      | DATE          |
| is_prime_member | BOOLEAN       |

Each column stores a different type of information.

Choosing the correct data type makes the database faster, more reliable, and easier to manage.

---

# 🧠 Interview Explanation

### What are Data Types?

Data Types define the type of values that can be stored in a database column.

They help ensure data accuracy, improve storage efficiency, and prevent invalid data from being inserted.

---

### Interview Answer (30 Seconds)

> Data Types specify what kind of data a column can store, such as numbers, text, dates, or boolean values. They help maintain data integrity, optimize storage, and improve query performance. Common SQL data types include INTEGER, VARCHAR, DECIMAL, DATE, TIMESTAMP, and BOOLEAN.

---

# 📂 Common SQL Data Types

## 1️⃣ Numeric Data Types

Used for numbers.

| Data Type     | Example    |
| ------------- | ---------- |
| INT / INTEGER | 10         |
| SMALLINT      | 100        |
| BIGINT        | 9999999999 |
| DECIMAL(10,2) | 5999.99    |
| NUMERIC       | 100.50     |
| REAL / FLOAT  | 3.14       |

Example:

```sql
salary DECIMAL(10,2)
```

---

## 2️⃣ Character (String) Data Types

Used for text.

| Data Type    | Example          |
| ------------ | ---------------- |
| CHAR(5)      | "ABCDE"          |
| VARCHAR(100) | "John"           |
| TEXT         | Long description |

Example:

```sql
name VARCHAR(100)
```

---

## 3️⃣ Date & Time Data Types

Used for dates and times.

| Data Type | Example             |
| --------- | ------------------- |
| DATE      | 2026-07-13          |
| TIME      | 10:30:45            |
| TIMESTAMP | 2026-07-13 10:30:45 |

Example:

```sql
created_at TIMESTAMP
```

---

## 4️⃣ Boolean Data Type

Stores only two values.

```text
TRUE
FALSE
```

Example:

```sql
is_active BOOLEAN
```

---

# ✍️ Syntax

## Create Table

```sql
CREATE TABLE Employee (
    id INT,
    name VARCHAR(100),
    salary DECIMAL(10,2),
    joining_date DATE,
    is_active BOOLEAN
);
```

---

# 💻 Example Queries

## Create Employee Table

```sql
CREATE TABLE Employee (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    salary DECIMAL(10,2),
    joining_date DATE,
    is_active BOOLEAN
);
```

---

## Insert Data

```sql
INSERT INTO Employee
VALUES (
    1,
    'John',
    25,
    50000.50,
    '2026-07-13',
    TRUE
);
```

---

## Retrieve Employees

```sql
SELECT *
FROM Employee;
```

---

# ❓ Common Interview Questions

### Q1. What is a Data Type?

A Data Type defines what kind of value can be stored in a database column.

---

### Q2. Why do we use Data Types?

To:

- Store correct data
- Prevent invalid values
- Improve storage efficiency
- Improve performance

---

### Q3. What is the difference between CHAR and VARCHAR?

**CHAR**

- Fixed length
- Always uses the defined size

Example:

```text
CHAR(10)

"John"

Stored as:

John______
```

---

**VARCHAR**

- Variable length
- Uses only the required storage

Example:

```text
VARCHAR(10)

John
```

VARCHAR is more commonly used.

---

### Q4. Difference between INT and BIGINT?

- INT → Smaller range of numbers
- BIGINT → Much larger range

Use BIGINT when very large numbers are expected.

---

### Q5. When should we use DECIMAL instead of FLOAT?

Use **DECIMAL** for money because it stores exact values.

Use **FLOAT** for approximate values such as scientific calculations.

---

# 🧩 Interview Follow-up Questions

### Q1. Which Data Types are used most often?

The most commonly used are:

- INT
- VARCHAR
- DECIMAL
- DATE
- TIMESTAMP
- BOOLEAN
- TEXT

---

### Q2. Why shouldn't we store numbers as VARCHAR?

Because:

- Calculations become difficult
- Sorting may be incorrect
- Performance can decrease

Always use numeric data types for numbers.

---

### Q3. Can we change a column's Data Type later?

Yes.

Example:

```sql
ALTER TABLE Employee
ALTER COLUMN salary TYPE DECIMAL(12,2);
```

---

### Q4. Which Data Type should be used for phone numbers?

Usually **VARCHAR**, not INT.

Reason:

- Phone numbers are identifiers, not values for calculation.
- They may contain leading zeros or symbols like `+`.

---

### Q5. Which Data Type should be used for money?

Use **DECIMAL**, not FLOAT.

DECIMAL stores exact values, making it suitable for financial data.

---

# 📝 Practice Exercises

### Exercise 1

Create a `Student` table with:

- id
- name
- age
- email

Choose appropriate data types.

---

### Exercise 2

Create a `Product` table.

Columns:

- id
- name
- price
- stock
- created_at

---

### Exercise 3

Insert five employee records.

---

### Exercise 4

Create a table with a BOOLEAN column.

---

### Exercise 5

Explain why `VARCHAR` is used for email addresses.

---

# ⚠️ Common Mistakes

### ❌ Using VARCHAR for numbers

Wrong:

```sql
salary VARCHAR(20)
```

Correct:

```sql
salary DECIMAL(10,2)
```

---

### ❌ Using INT for phone numbers

Phone numbers are identifiers.

Use:

```sql
phone VARCHAR(15)
```

---

### ❌ Using FLOAT for money

Use:

```sql
DECIMAL(10,2)
```

Money requires exact precision.

---

### ❌ Choosing very large VARCHAR sizes unnecessarily

Example:

```sql
name VARCHAR(5000)
```

Use a realistic size, such as:

```sql
name VARCHAR(100)
```

---

# 🔁 Revision Summary

✅ Data Types define what kind of data a column can store.

✅ They improve data integrity.

✅ They optimize storage and performance.

✅ Common Data Types:

- INT
- VARCHAR
- DECIMAL
- DATE
- TIMESTAMP
- BOOLEAN
- TEXT

✅ Every table column should have an appropriate data type.

---

# 💡 Key Takeaways

- A Data Type tells the database what kind of data a column can store.
- Choosing the correct Data Type improves accuracy, storage efficiency, and performance.
- Use `VARCHAR` for text, `INT` for whole numbers, `DECIMAL` for money, `DATE`/`TIMESTAMP` for dates, and `BOOLEAN` for true/false values.
- Don't memorize every SQL data type—master the commonly used ones first.
