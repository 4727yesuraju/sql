# Data Types

## 🤔 Why it's needed

Every application stores different kinds of data, such as:

- User name
- Age
- Email
- Price
- Date
- Images
- Videos
- True/False values

A **Data Type** tells the computer **what kind of data is being stored** and **what operations can be performed on it**.

Using the correct data type helps:

- Save memory
- Improve performance
- Validate data correctly
- Prevent errors
- Maintain data consistency

---

## 🌍 Real-world example

Imagine you're filling out a **bank account application**.

Each field expects a specific type of data:

| Field             | Data Type            |
| ----------------- | -------------------- |
| Name              | Text (String)        |
| Age               | Number (Integer)     |
| Balance           | Decimal Number       |
| Is Account Active | Boolean (True/False) |
| Date of Birth     | Date                 |
| Profile Photo     | Image/Binary         |

Just like a form expects the correct kind of input, programs and databases use **Data Types** to store data correctly.

---

## 🧠 Interview explanation

### Definition

A **Data Type** defines **the type of value a variable, field, or database column can store**.

It also determines:

- How much memory is used.
- What operations are allowed.
- How the data is processed.

---

## Common Data Types

### 1. String

Stores text.

Examples:

```text
"Yesu Raju"

"Hello"

"user@gmail.com"
```

Used for:

- Names
- Addresses
- Emails
- Messages

---

### 2. Integer

Stores whole numbers.

Examples:

```text
10

100

-50
```

Used for:

- Age
- Quantity
- Count

---

### 3. Float / Decimal

Stores numbers with decimal points.

Examples:

```text
99.99

3.14

5000.75
```

Used for:

- Prices
- Salary
- Weight

---

### 4. Boolean

Stores only two values.

```text
true

false
```

Used for:

- Login status
- Email verified
- Payment completed

---

### 5. Date / Time

Stores dates and times.

Examples:

```text
2026-07-13

10:30 AM

2026-07-13 10:30:45
```

Used for:

- Birthdays
- Order dates
- Login time

---

### 6. Array / List

Stores multiple values of the same type.

Example:

```text
["Apple", "Mango", "Orange"]
```

Used for:

- Tags
- Product names
- Skills

---

### 7. Object / Record

Stores related data using key-value pairs.

Example:

```text
{
  Name: "Rahul",
  Age: 25
}
```

Used for:

- User details
- Product information
- Orders

---

### 8. Binary (BLOB)

Stores binary files.

Examples:

- Images
- Videos
- PDFs
- Audio files

---

## Data Types in Databases

| Data Type | Example       |
| --------- | ------------- |
| VARCHAR   | Name          |
| INT       | Age           |
| DECIMAL   | Salary        |
| BOOLEAN   | IsActive      |
| DATE      | Birthday      |
| TIMESTAMP | CreatedAt     |
| BLOB      | Profile Photo |

---

## Data Types in Programming

| Data Type              | Example         |
| ---------------------- | --------------- |
| String                 | `"Hello"`       |
| Number                 | `25`            |
| Boolean                | `true`          |
| Array                  | `[1,2,3]`       |
| Object                 | `{name:"John"}` |
| Null                   | `null`          |
| Undefined (JavaScript) | `undefined`     |

---

## ✍️ Syntax

### JavaScript

```javascript
let name = "Yesu Raju"; // String

let age = 25; // Number

let salary = 45000.5; // Decimal

let isActive = true; // Boolean

let skills = ["Node.js", "React"]; // Array

let user = {
  name: "Yesu Raju",
  age: 25,
}; // Object
```

---

### SQL

```sql
CREATE TABLE Users (
    id INT,
    name VARCHAR(100),
    age INT,
    salary DECIMAL(10,2),
    is_active BOOLEAN,
    created_at TIMESTAMP
);
```

---

## 💻 Example queries

- What are Data Types?
- Why are Data Types important?
- What is the difference between Integer and Float?
- What is a Boolean?
- What is VARCHAR in SQL?
- What is BLOB?
- What is the difference between Array and Object?

---

## ❓ Common interview questions

1. What are Data Types?
2. Why do we use Data Types?
3. What is the difference between Integer and Float?
4. What is Boolean?
5. What is VARCHAR?
6. What is TIMESTAMP?
7. What is BLOB?
8. What is the difference between Array and Object?
9. What is Null?
10. What is Undefined? (JavaScript)

---

## 📝 Practice exercises

1. Identify the data type of each value:
   - `"Hello"`
   - `100`
   - `99.95`
   - `true`
   - `["Java", "Node"]`

2. Design a **Student** table with appropriate SQL data types.

3. Create a JavaScript object representing a user.

4. Explain when to use:
   - String
   - Integer
   - Boolean
   - Date

5. Compare SQL data types with JavaScript data types.

---

## ⚠️ Common mistakes

- Storing numbers as strings.
- Using an Integer for decimal values.
- Choosing the wrong data type for dates.
- Storing large files directly in the database without considering storage needs.
- Confusing `null` with `undefined` in JavaScript.
- Using overly large data types when a smaller one is sufficient.

---

## 🔁 Revision summary

### Data Types

- Define the kind of data that can be stored.
- Improve performance and data integrity.
- Ensure correct operations on data.

### Common Data Types

- **String** → Text
- **Integer** → Whole Numbers
- **Float / Decimal** → Decimal Numbers
- **Boolean** → True/False
- **Date** → Date & Time
- **Array** → Multiple Values
- **Object** → Key-Value Data
- **Binary** → Images, Videos, Files

### Easy Revision Formula

```text
Text

↓

String

Number

↓

Integer / Float

True or False

↓

Boolean

Date

↓

Date/Time

Many Values

↓

Array

Related Data

↓

Object
```

### Memory Trick

```text
String

↓

Words

Integer

↓

Whole Numbers

Float

↓

Decimal Numbers

Boolean

↓

Yes / No

Date

↓

Time Information

Array

↓

Many Items

Object

↓

Complete Information
```

> **Remember:**
>
> A **Data Type** tells the computer **what kind of data is stored** and **how it should be handled**. Choosing the correct data type makes applications more efficient, reliable, and easier to maintain.
