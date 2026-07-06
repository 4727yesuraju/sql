## ❓ Doubt: What does "SQL is a standard language" mean?

### Answer

A **standard language** is a language that follows a **common set of rules** accepted by different database systems.

Because of this, the same basic SQL commands work across most relational databases.

### Example

The following query works (or works very similarly) in databases like MySQL, PostgreSQL, SQL Server, Oracle, and SQLite:

```sql
SELECT * FROM employees;
```

### Interview Answer

> "A standard language is a language that follows a common set of rules accepted by different database systems. Because of this, the same basic SQL commands work across most relational databases."

---

## ❓ Doubt: What does "Control Permissions" mean in SQL?

### Answer

**Control permissions** means managing **who can access the database and what actions they are allowed to perform**.

A database administrator (DBA) can grant or revoke permissions for different users.

### Common Permissions

- `SELECT` → Read/View data
- `INSERT` → Add new data
- `UPDATE` → Modify existing data
- `DELETE` → Remove data
- `CREATE` → Create databases or tables
- `ALTER` → Modify table structure
- `DROP` → Delete databases or tables

### SQL Example

```sql
-- Give a user permission to read data
GRANT SELECT ON employees TO user_name;

-- Remove permission to delete data
REVOKE DELETE ON employees FROM user_name;
```

### Real-World Example

Suppose an `employees` table has two users:

- **Manager** → Can read, insert, update, and delete data.
- **Intern** → Can only read data.

This is an example of **controlling permissions**.

### Interview Answer

> **"Control permissions means managing user access to the database by deciding what actions each user is allowed to perform, such as reading, inserting, updating, or deleting data."**
