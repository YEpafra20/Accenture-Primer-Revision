# Mastering Relational Databases with MySQL — Revision Notes

**Category:** Electives · **Focus Area:** Database Management · **Level:** Intermediate

---

## Table of Contents

1. [RDBMS Concepts](#1-rdbms-concepts)
2. [ER and Normalization](#2-er-and-normalization)
3. [Data Definition Language (DDL)](#3-data-definition-language-ddl)
4. [Data Manipulation Language (DML)](#4-data-manipulation-language-dml)
5. [SQL Select Statement](#5-sql-select-statement)
6. [Function — Scalar & Aggregate](#6-function--scalar--aggregate)
7. [Joins & Subquery](#7-joins--subquery)
8. [DCL & Database Objects](#8-dcl--database-objects)

---

## 1. RDBMS Concepts

> Placeholder — the source notepad listed "RDBMS Introduction" as a section header, then moved directly into the ER Model & Normalization content. Add core RDBMS concepts here (what a Relational Database Management System is, tables/rows/columns, ACID properties, RDBMS vs DBMS, popular RDBMS engines) once available.

---

## 2. ER and Normalization

### 2.1 Entities & Attributes

**Entities:**
Specific objects or things in the real world that are represented in the database.
Example: the EMPLOYEE "John Doe", the DEPARTMENT of "Sales".

**Attributes:**
Properties used to describe any entity.
Example: an EMPLOYEE entity may have a Name, ID, Address, Sex, BirthDate.

### 2.2 Composite Key

A key attribute may be **composite** — a combination of multiple attributes, such that together they are unique.

**Example:** `EmployeeID` is a key of the EMPLOYEE entity type, composed of `(DepartmentNumber, EmployeeNumber)`.

### 2.3 Normalization

**Normalization** is the process of minimizing data redundancy by decomposing relations in a database.

**Goals:**
- Allows data to be processed more efficiently, and queries to be processed faster
- Achieves a highly flexible design
- Ensures the design is free from update, insertion, and deletion anomalies

### 2.4 First Normal Form (1NF)

- Remove repeating groups
- Repeating groups become new entities, linked together by a one-to-many relationship
- Relationships are created by including a primary key from one entity as a foreign key in another entity

### 2.5 Second Normal Form (2NF)

- Identify functionally dependent and partially dependent attributes

### 2.6 Third Normal Form (3NF)

- Remove all transitive dependencies to a new entity

### 2.7 Denormalization

**De-normalization** is a technique to move from higher to lower normal forms of database modeling, in order to speed up database access.

---

## 3. Data Definition Language (DDL)

### 3.1 What is DDL?

**Data Definition Language** defines the structure of a table.

**Core commands:** `CREATE` · `ALTER` · `RENAME` · `TRUNCATE` · `DROP`

### 3.2 Data Types

MySQL data types are classified into three main categories:

| Category | Types |
|---|---|
| **Numeric** | INT, FLOAT, DOUBLE (or REAL), DECIMAL (or DEC or FIXED) |
| **Date and Time** | DATE, TIME, DATETIME, TIMESTAMP |
| **String** | CHAR, VARCHAR, ENUM, BINARY |

### 3.3 Constraints

**Constraints** are rules enforced on data columns in a table. They limit the type of data that can go into a table, ensuring the accuracy and reliability of the data.

**Types of Constraints:**

| Constraint | Description |
|---|---|
| **Primary Key** | Unique + Not Null |
| **Foreign Key** | References the primary key of another table |
| **Unique** | Values must be unique |
| **Not Null** | Value cannot be null |
| **Check** | Validates values against a condition |

> A table can have **one** primary key, but it can have **'N' number** of foreign keys, unique, not null, and check constraints.
>
> Two columns joined together can be made into a single (composite) primary key.

### 3.4 Foreign Key

- Used to enforce the link between tables
- The referenced table is called the **parent table**; the table with the foreign key is called the **child table**
- The primary or unique column of the parent table can be created as the foreign key column in the child table

### 3.5 ALTER

The `ALTER` command is used to change the structure of a table:

- Add a new column/constraint
- Remove an existing column/constraint
- Rename an existing column
- Increase or decrease the column size
- Change the column data type

**Examples:**

```sql
-- Add a column age into table
ALTER TABLE customer ADD age INT(2);

-- Increase the column size of email to 30
ALTER TABLE customer MODIFY email VARCHAR(30);

-- Rename the column name from email to emailid
ALTER TABLE customer CHANGE email emailid VARCHAR(25);

-- Change the datatype of a particular column
ALTER TABLE customer MODIFY emailid VARCHAR(35);

-- Remove a column from the table
ALTER TABLE customers DROP COLUMN emailid;

-- Remove a constraint
ALTER TABLE customers DROP FOREIGN KEY ck;
```

> **Note:** Constraints can be applied at the column level or table level. Column-level constraints apply only to one column, whereas table-level constraints apply to the whole table.

### 3.6 Rename a Table

```sql
RENAME TABLE Policy TO Policy_Details;
```

### 3.7 Truncate

- Removes all rows from the table
- **Restriction:** You cannot truncate the table if it is linked with another table

```sql
TRUNCATE TABLE <Table_name>;
-- Example:
TRUNCATE TABLE Customer;
```

### 3.8 Truncate vs Drop

| Command | Effect |
|---|---|
| **TRUNCATE** | Only data is removed |
| **DROP** | Entire structure is removed |

---

## 4. Data Manipulation Language (DML)

### 4.1 What is DML?

DML defines the **data** of a table.

| Command | Example |
|---|---|
| **INSERT** | `INSERT INTO customer VALUES(1, 'Tom', 9876523190, 'Tom@gmail.com', 'Mumbai');` |
| **UPDATE** | Modifies existing rows |
| **DELETE** | `DELETE FROM Customer WHERE CidRDB = 2;` |
| **SELECT** | Retrieves data |

### 4.2 Delete vs Truncate

| DELETE | TRUNCATE |
|---|---|
| Deletes all rows or a specific row from the table | Removes all rows from the table |
| Can be reverted to its previous state | Cannot be reverted |
| Rows referred to in a child table cannot be removed | Will not work if the truncated table is referenced |

### 4.3 Database Transaction

- A **transaction** is a logical unit of work
- MySQL ensures data consistency based on transactions
- A transaction performs a consistent data change
- A transaction begins when a DML statement is executed
- A transaction should end with either **COMMIT** or **ROLLBACK**
- DDL commands are, by default, **auto-commit**

| Command | Description |
|---|---|
| **COMMIT** | Ends the current transaction by making all pending data changes permanent |
| **SAVEPOINT name** | Marks a save point within the current transaction |
| **ROLLBACK TO SAVEPOINT name** | Rolls back the current transaction to the specified savepoint, discarding any changes or savepoints created after that point |
| **ROLLBACK** | Ends the current transaction by discarding all pending data changes |

---

## 5. SQL Select Statement

### 5.1 SELECT Statement

The SQL `SELECT` statement is used to fetch data from a database table. SELECT can be used for retrieving data.

### 5.2 Logical Operators

| Operator | Description |
|---|---|
| **AND** | Returns true if both conditions are true |
| **OR** | Returns true if either condition is true |
| **NOT** | Returns true if the condition is false |

### 5.3 ORDER BY Clause

Used to retrieve, for example, customer names in ascending order.

---

## 6. Function — Scalar & Aggregate

### 6.1 What is a Function?

A **function** is a block of code that returns a single value.

### 6.2 SQL Function Hierarchy

```
SQL Functions
│
├── Built-In / SQL Functions
│   │
│   ├── Single Row Functions
│   │   ├── Character Functions
│   │   ├── Number Functions
│   │   ├── Date Functions
│   │   └── Conversion Functions
│   │
│   └── Multiple Row Functions (Group of Rows)
│       ├── AVG
│       ├── MAX
│       ├── MIN
│       └── SUM
│
└── User Defined Functions
    └── Custom Functions
```

### 6.3 Function Types

| Function Type | Description |
|---|---|
| **Character Function** | Single-row character functions accept character data as input and can return both character and numeric values |
| **Number Function** | Accepts numeric input and returns numeric values |
| **Date Function** | E.g., to get the current system date |
| **Nesting Functions** | Single-row functions can be nested to any level |
| **Cast Function** | The MySQL CAST function converts a value of any type to a specified data type (ANSI-SQL specification) |
| **General Function** | Works with any data type and pertains to handling null values |
| **NULLIF and IFNULL** | Usable data types include date, character, varchar, and integer — data types must match |

### 6.4 Aggregate Functions

**Example question:** "What is the max and min penalty amount paid for late payment?"

```sql
SELECT MAX(penalty) AS maximum, MIN(penalty) AS minimum FROM policyenrollment;
```

### 6.5 GROUP BY

Used to group records based on a column (e.g., customer ID), then apply an aggregate function.

```sql
SELECT CID, MAX(penalty) AS max, MIN(penalty) AS min
FROM policyenrollment
GROUP BY CID;
```

### 6.6 HAVING Clause

**Example question:** "Who has paid a total premium amount greater than Rs. 2000?"

```sql
SELECT CID, SUM(amount) AS total
FROM policyenrollment
GROUP BY CID
HAVING SUM(amount) > 2000;
```

---

## 7. Joins & Subquery

### 7.1 JOINS

The `JOIN` keyword is used to combine records from two or more tables, based on a common field between them. To produce a report, we often need to link more than one table and access data from both.

### 7.2 Join Syntax

```sql
-- WHERE clause style
SELECT table1.column, table2.column
FROM table1, table2
WHERE table1.column1 = table2.column2;

-- JOIN...ON style
SELECT table1.column, table2.column
FROM table1
JOIN table2 ON table1.column1 = table2.column2;
```

> The join condition can be written in either the `WHERE` clause or the `ON` clause.

### 7.3 Equijoin

**EQUI joins** (also called simple joins or inner joins) — when two tables are joined using the `=` operator in the join condition, it's called an equi join.

### 7.4 Outer Join

- Left and Right Outer Joins
- **Note:** Full join is not natively supported in MySQL — the effect of a full join is achieved through `LEFT JOIN`, `RIGHT JOIN`, and the `UNION` operator

### 7.5 Self Join

A **self join** joins a table to itself. It is done by creating alias names for the same table.

### 7.6 Natural Join

A **Natural Join** is a type of EQUI JOIN that compares the common columns of both tables with each other. The columns must have the same data type.

### 7.7 Joins with the USING Clause

The `USING` clause specifies which columns to test for equality when two tables are joined — it can be used instead of an `ON` or `WHERE` clause.

### 7.8 Subquery

A **subquery** is a query nested inside a `SELECT`, `INSERT`, `UPDATE`, or `DELETE` statement, or inside another subquery.

**Types of Subquery:**

| Type | Operators |
|---|---|
| **Single Row Subquery** | `=`, `<`, `<=`, `>`, `>=`, `<>` |
| **Multiple Row Subquery** | `IN`, `ALL`, `ANY` |

### 7.9 SQL Joins — Summary

| Join Type | Result |
|---|---|
| **INNER / EQUI** | Matching rows from both tables |
| **FULL [OUTER]** | Matching and unmatched rows from both tables |
| **LEFT [OUTER]** | All rows from the left, matching rows from the right |
| **RIGHT [OUTER]** | All rows from the right, matching rows from the left |

---

## 8. DCL & Database Objects

### 8.1 Data Control Language (DCL)

Used to create privileges that allow users to access and manipulate the database. Two main commands:

| Command | Description |
|---|---|
| **GRANT** | Grants a privilege to a user |
| **REVOKE** | Revokes (removes) a privilege from a user |

### 8.2 VIEW

A **view** is a virtual table that provides a window through which one can see data (stored in a base relation).

### 8.3 AUTO_INCREMENT

Generates unique numbers automatically. A shared object, typically used to create data for a primary key column.

### 8.4 INDEX

A performance-tuning method that allows faster retrieval of records. Can reduce disk I/O by using a rapid path access method to locate data quickly.

---

## Quick Revision Checklist

- [ ] Can differentiate Entity vs Attribute, with examples
- [ ] Can explain what a Composite Key is
- [ ] Can state the goal of Normalization
- [ ] Can describe what 1NF, 2NF, and 3NF each require
- [ ] Can explain Denormalization and why it's used
- [ ] Can list the 3 MySQL data type categories with examples
- [ ] Can list all 5 constraint types
- [ ] Can explain Parent table vs Child table in a Foreign Key relationship
- [ ] Can write ALTER TABLE statements to add, modify, rename, and drop a column
- [ ] Can differentiate TRUNCATE vs DROP
- [ ] Can differentiate DELETE vs TRUNCATE
- [ ] Can explain COMMIT, SAVEPOINT, ROLLBACK, and ROLLBACK TO SAVEPOINT
- [ ] Can list the 3 logical operators (AND, OR, NOT)
- [ ] Can differentiate Single-row vs Multiple-row (aggregate) SQL functions
- [ ] Can write a query using GROUP BY and HAVING correctly
- [ ] Can differentiate Equijoin, Outer Join, Self Join, and Natural Join
- [ ] Can differentiate Single-row vs Multiple-row subqueries and their operators
- [ ] Can explain GRANT vs REVOKE
- [ ] Can explain what a VIEW, AUTO_INCREMENT, and INDEX are used for