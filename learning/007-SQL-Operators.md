# SQL Operators

> "SQL operators are symbols or keywords used to compare, calculate, and filter data."

---

# 📖 What are SQL Operators?

SQL **Operators** are special symbols or keywords that perform operations on data.

They help us:

- Compare values
- Perform calculations
- Filter records
- Combine conditions
- Search for patterns
- Check ranges
- Check NULL values

Without operators, SQL queries would not be able to search or filter data effectively.

---

# 🤔 Why are SQL Operators Needed?

Imagine an Employee table with 10,000 employees.

You don't want to see all employees.

You only want employees:

- Salary greater than ₹50,000
- Age less than 30
- Working in IT
- Name starts with "A"

How does the database know which records to return?

Using **Operators**.

Example:

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

Here,

`>` tells SQL to return only employees whose salary is greater than ₹50,000.

---

# 🌍 Real-world Example

Imagine you're building an Amazon application.

A customer searches:

> "Show products below ₹1000."

Backend executes:

```sql
SELECT *
FROM Products
WHERE price < 1000;
```

Customer searches:

> "Show products between ₹500 and ₹1000."

```sql
SELECT *
FROM Products
WHERE price BETWEEN 500 AND 1000;
```

Customer searches:

> "Show products whose name starts with 'S'."

```sql
SELECT *
FROM Products
WHERE product_name LIKE 'S%';
```

Operators make these searches possible.

---

# 🧠 Interview Explanation

### What are SQL Operators?

SQL Operators are symbols or keywords used to compare values, perform calculations, and filter data in SQL queries.

They help retrieve exactly the records we need from a database.

---

### Interview Answer (30 Seconds)

> SQL Operators are special symbols or keywords used to perform operations on data. They allow us to compare values, perform calculations, combine conditions, search patterns, check ranges, and filter records. Common operators include =, >, <, >=, <=, <>, AND, OR, LIKE, IN, BETWEEN, and IS NULL.

---

# 📂 Types of SQL Operators

---

## 1️⃣ Comparison Operators

Used to compare values.

| Operator | Meaning               |
| -------- | --------------------- |
| =        | Equal                 |
| >        | Greater than          |
| <        | Less than             |
| >=       | Greater than or equal |
| <=       | Less than or equal    |
| <> or != | Not equal             |

Example:

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

---

## 2️⃣ Logical Operators

Used to combine multiple conditions.

| Operator | Meaning                             |
| -------- | ----------------------------------- |
| AND      | Both conditions must be true        |
| OR       | At least one condition must be true |
| NOT      | Reverses a condition                |

Example:

```sql
SELECT *
FROM Employee
WHERE department = 'IT'
AND salary > 50000;
```

---

## 3️⃣ Arithmetic Operators

Perform mathematical calculations.

| Operator | Meaning        |
| -------- | -------------- |
| +        | Addition       |
| -        | Subtraction    |
| \*       | Multiplication |
| /        | Division       |
| %        | Modulus        |

Example:

```sql
SELECT salary * 12 AS yearly_salary
FROM Employee;
```

---

## 4️⃣ BETWEEN Operator

Checks whether a value falls within a range.

Example:

```sql
SELECT *
FROM Employee
WHERE salary BETWEEN 50000 AND 100000;
```

---

## 5️⃣ IN Operator

Checks if a value matches any value in a list.

Example:

```sql
SELECT *
FROM Employee
WHERE department IN ('IT','HR','Sales');
```

---

## 6️⃣ LIKE Operator

Searches for matching text patterns.

Wildcards:

- `%` → Any number of characters
- `_` → Exactly one character

Example:

```sql
SELECT *
FROM Employee
WHERE name LIKE 'A%';
```

Employees whose names start with "A".

---

## 7️⃣ IS NULL Operator

Checks for NULL values.

Example:

```sql
SELECT *
FROM Employee
WHERE email IS NULL;
```

---

# ✍️ Syntax

## Equal

```sql
SELECT *
FROM Employee
WHERE id = 10;
```

---

## Greater Than

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

---

## BETWEEN

```sql
SELECT *
FROM Employee
WHERE salary BETWEEN 40000 AND 60000;
```

---

## IN

```sql
SELECT *
FROM Employee
WHERE department IN ('IT','HR');
```

---

## LIKE

```sql
SELECT *
FROM Employee
WHERE name LIKE 'J%';
```

---

## IS NULL

```sql
SELECT *
FROM Employee
WHERE email IS NULL;
```

---

# 💻 Example Queries

## Employees earning more than ₹50,000

```sql
SELECT *
FROM Employee
WHERE salary > 50000;
```

---

## Employees in IT department

```sql
SELECT *
FROM Employee
WHERE department = 'IT';
```

---

## Employees in IT or HR

```sql
SELECT *
FROM Employee
WHERE department IN ('IT','HR');
```

---

## Employees whose names start with A

```sql
SELECT *
FROM Employee
WHERE name LIKE 'A%';
```

---

## Employees without email

```sql
SELECT *
FROM Employee
WHERE email IS NULL;
```

---

# ❓ Common Interview Questions

### Q1. What are SQL Operators?

Operators are symbols or keywords used to compare, calculate, and filter data.

---

### Q2. What is the difference between = and LIKE?

- `=` checks for an exact match.
- `LIKE` searches using patterns.

---

### Q3. What is the difference between IN and OR?

These queries are equivalent:

```sql
WHERE department IN ('IT','HR')
```

```sql
WHERE department='IT'
OR department='HR'
```

`IN` is shorter and easier to read.

---

### Q4. What is BETWEEN?

It checks whether a value falls within a specified range (inclusive).

---

### Q5. Why can't we use = NULL?

Because `NULL` means **unknown**, not an actual value.

Use:

```sql
IS NULL
```

instead of:

```sql
= NULL
```

---

# 🧩 Interview Follow-up Questions

### Q1. Which SQL operator is used most often?

The comparison operators (`=`, `>`, `<`) together with logical operators (`AND`, `OR`) are the most commonly used.

---

### Q2. Is BETWEEN inclusive?

Yes.

`BETWEEN 10 AND 20` includes both **10** and **20**.

---

### Q3. Why is LIKE slower than =?

Because pattern matching often requires scanning more data, especially when the pattern starts with `%`.

---

### Q4. Can we combine multiple operators?

Yes.

Example:

```sql
SELECT *
FROM Employee
WHERE salary > 50000
AND department = 'IT';
```

---

### Q5. What is the difference between NULL and 0?

- `NULL` = Unknown or missing value.
- `0` = A valid numeric value.

---

# 📝 Practice Exercises

### Exercise 1

Find employees earning more than ₹60,000.

---

### Exercise 2

Find employees in the HR department.

---

### Exercise 3

Find employees whose names start with "S".

---

### Exercise 4

Find employees whose salary is between ₹40,000 and ₹80,000.

---

### Exercise 5

Find employees whose email is NULL.

---

### Exercise 6

Find employees working in IT or Sales.

---

# ⚠️ Common Mistakes

### ❌ Using = NULL

Wrong:

```sql
WHERE email = NULL;
```

Correct:

```sql
WHERE email IS NULL;
```

---

### ❌ Confusing = with LIKE

`=` → Exact match

```sql
WHERE name = 'John';
```

`LIKE` → Pattern matching

```sql
WHERE name LIKE 'J%';
```

---

### ❌ Forgetting parentheses with AND and OR

Wrong logic can return unexpected results.

Use parentheses when combining conditions.

---

### ❌ Forgetting BETWEEN is inclusive

`BETWEEN 10 AND 20`

Includes:

- 10 ✅
- 20 ✅

---

# 🔁 Revision Summary

✅ SQL Operators compare, calculate, and filter data.

✅ Types of operators:

- Comparison Operators
- Logical Operators
- Arithmetic Operators
- BETWEEN
- IN
- LIKE
- IS NULL

✅ Operators are mainly used inside the `WHERE` clause.

✅ They help retrieve exactly the records you need.

---

# 💡 Key Takeaways

- Operators are the heart of filtering data in SQL.
- Learn operators by category instead of memorizing them randomly.
- `=` is for exact matches, while `LIKE` is for pattern matching.
- Always use `IS NULL` to check for NULL values.
- Mastering operators makes writing SQL queries much easier.
