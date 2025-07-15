Sure, Muazam! Here's the complete **SQL Learning Notes** in clean, single-file GitHub markdown format, without any Apna College branding. This is ready to paste into a `.md` file for your GitHub repository.

---

### ✅ Final GitHub Markdown Format (Ready to Paste)

```markdown
# 🧠 SQL Full Course Notes

Welcome to my complete SQL learning notes. This markdown file contains all concepts, commands, syntax, and examples to help revise SQL quickly and efficiently.

---

## 📂 What is a Database?

- A **Database** is a collection of structured data, stored digitally, that can be easily accessed, managed, and updated.
- The software that interacts with databases is called a **DBMS** (Database Management System).

---

## 📑 Types of Databases

1. **Relational Databases**
   - Data is stored in **tables** (rows and columns).
   - We use **SQL** to interact with relational DBMS like MySQL, PostgreSQL, etc.

2. **Non-relational (NoSQL) Databases**
   - Data is stored in other formats like key-value, document, graph, etc.
   - Examples: MongoDB, Redis, Cassandra.

---

## 💻 What is SQL?

**SQL (Structured Query Language)** is used to perform operations like:

- `CREATE` — Create new databases or tables
- `READ` — Read or query data
- `UPDATE` — Modify existing data
- `DELETE` — Remove data

---

## 🧱 Database Structure

```

Database
├── Table 1
│    └── Data (Rows)
└── Table 2
└── Data (Rows)

````

---

## 🧾 Creating a Database

```sql
CREATE DATABASE db_name;
DROP DATABASE db_name;
CREATE DATABASE IF NOT EXISTS db_name;
DROP DATABASE IF EXISTS db_name;
SHOW DATABASES;
````

---

## 📋 Creating a Table

```sql
USE db_name;

CREATE TABLE table_name (
  column1 datatype constraint,
  column2 datatype constraint,
  ...
);
```

---

## 🧮 SQL Data Types

* `INT`, `TINYINT`, `BIGINT`
* `VARCHAR(n)`, `TEXT`
* `DATE`, `DATETIME`
* `FLOAT`, `DOUBLE`
* `BOOLEAN`

**Signed vs Unsigned:**

* `TINYINT` → `-128 to 127`
* `TINYINT UNSIGNED` → `0 to 255`

---

## 🧰 SQL Commands Categories

| Category               | Description         | Examples                              |
| ---------------------- | ------------------- | ------------------------------------- |
| **DDL** (Definition)   | Schema operations   | `CREATE`, `DROP`, `ALTER`, `TRUNCATE` |
| **DQL** (Query)        | Read data           | `SELECT`                              |
| **DML** (Manipulation) | Modify data         | `INSERT`, `UPDATE`, `DELETE`          |
| **DCL** (Control)      | Access control      | `GRANT`, `REVOKE`                     |
| **TCL** (Transaction)  | Handle transactions | `COMMIT`, `ROLLBACK`                  |

---

## 🔑 Keys in SQL

* **Primary Key (PK)**: Uniquely identifies each record (Only 1 allowed, NOT NULL).
* **Foreign Key (FK)**: Refers to a PK in another table (Can be multiple, can be NULL).

---

## 📎 SQL Constraints

| Constraint    | Description                 |
| ------------- | --------------------------- |
| `NOT NULL`    | Value must be provided      |
| `UNIQUE`      | No duplicate values allowed |
| `PRIMARY KEY` | Unique + Not Null           |
| `FOREIGN KEY` | Links two tables            |
| `DEFAULT`     | Sets default value          |
| `CHECK`       | Restricts range of values   |

---

## 📄 Table Queries

### Create Table

```sql
CREATE TABLE students (
  id INT PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  age INT,
  city VARCHAR(100)
);
```

### Insert Records

```sql
INSERT INTO students (id, name, age, city)
VALUES 
(1, 'Ali', 20, 'Lahore'),
(2, 'Sara', 22, 'Karachi');
```

### Select Data

```sql
SELECT * FROM students;
SELECT name, city FROM students;
```

### WHERE Clause

```sql
SELECT * FROM students WHERE age > 20;
```

**Operators:**

* Arithmetic: `+`, `-`, `*`, `/`, `%`
* Comparison: `=`, `!=`, `<`, `>`, `<=`, `>=`
* Logical: `AND`, `OR`, `NOT`, `IN`, `BETWEEN`, `LIKE`

---

## 🔄 Modify Table

```sql
ALTER TABLE students ADD COLUMN email VARCHAR(100);
ALTER TABLE students DROP COLUMN email;
ALTER TABLE students RENAME TO learners;

ALTER TABLE students
CHANGE COLUMN old_name new_name datatype;
MODIFY COLUMN age TINYINT NOT NULL;
```

---

## ❌ Delete/Truncate/Update

```sql
-- Delete specific row
DELETE FROM students WHERE id = 1;

-- Delete all rows but keep structure
TRUNCATE TABLE students;

-- Update data
UPDATE students SET age = 23 WHERE name = 'Sara';
```

---

## 🔗 Joins in SQL

### Types of Joins

| Join Type  | Description                        |
| ---------- | ---------------------------------- |
| INNER JOIN | Returns rows with matching values  |
| LEFT JOIN  | All from left + matched from right |
| RIGHT JOIN | All from right + matched from left |
| FULL JOIN  | All from both sides (via `UNION`)  |
| SELF JOIN  | Table joins with itself            |

```sql
SELECT s.name, c.course_name
FROM student s
INNER JOIN course c
ON s.id = c.student_id;
```

---

## 📊 Aggregate Functions

```sql
SELECT COUNT(*) FROM students;
SELECT MAX(age) FROM students;
SELECT MIN(age) FROM students;
SELECT AVG(age) FROM students;
SELECT SUM(age) FROM students;
```

---

## 📚 GROUP BY & HAVING

```sql
-- Count students per city
SELECT city, COUNT(*) FROM students GROUP BY city;

-- Cities with more than 5 students
SELECT city, COUNT(*) as total FROM students
GROUP BY city
HAVING total > 5;
```

---
