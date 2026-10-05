# 📚 SQL Commands and SQL vs NoSQL

This section covers the five major types of SQL commands and the basic differences between SQL and NoSQL databases.

## 🧩 Types of SQL Commands

SQL commands are commonly categorized into five types:

* **DDL** – Data Definition Language
* **DML** – Data Manipulation Language
* **TCL** – Transaction Control Language
* **DCL** – Data Control Language
* **DQL** – Data Query Language

---

## 1. 🏗️ DDL – Data Definition Language

DDL commands are used to define, modify, and manage database objects such as tables, schemas, and indexes.

| Command    | Description                                  | Example                                       |
| ---------- | -------------------------------------------- | --------------------------------------------- |
| `CREATE`   | Creates a new database object                | `CREATE TABLE employees (id INT, name TEXT);` |
| `ALTER`    | Modifies the structure of an existing object | `ALTER TABLE employees ADD COLUMN age INT;`   |
| `DROP`     | Deletes database objects                     | `DROP TABLE employees;`                       |
| `TRUNCATE` | Removes all records from a table             | `TRUNCATE TABLE employees;`                   |

---

## 2. 📝 DML – Data Manipulation Language

DML commands are used to manage data stored inside tables.

| Command  | Description               | Example                                                         |
| -------- | ------------------------- | --------------------------------------------------------------- |
| `INSERT` | Adds new records          | `INSERT INTO employees (id, name, age) VALUES (1, 'John', 30);` |
| `UPDATE` | Modifies existing records | `UPDATE employees SET age = 31 WHERE id = 1;`                   |
| `DELETE` | Removes specific records  | `DELETE FROM employees WHERE id = 1;`                           |

---

## 3. 🔄 TCL – Transaction Control Language

TCL commands are used to manage transactions and maintain data consistency and integrity.

| Command     | Description                                                     | Example          |
| ----------- | --------------------------------------------------------------- | ---------------- |
| `BEGIN`     | Starts a transaction                                            | `BEGIN;`         |
| `COMMIT`    | Saves changes made in a transaction                             | `COMMIT;`        |
| `ROLLBACK`  | Reverts changes made in a transaction                           | `ROLLBACK;`      |
| `SAVEPOINT` | Creates a point within a transaction to which you can roll back | `SAVEPOINT sp1;` |

---

## 4. 🔐 DCL – Data Control Language

DCL commands are used to control user access and permissions on database objects.

| Command  | Description                    | Example                                       |
| -------- | ------------------------------ | --------------------------------------------- |
| `GRANT`  | Gives permissions to users     | `GRANT SELECT, INSERT ON employees TO user1;` |
| `REVOKE` | Removes permissions from users | `REVOKE INSERT ON employees FROM user1;`      |

---

## 5. 🔍 DQL – Data Query Language

DQL is used to retrieve data from one or more tables.

The main DQL command is:

### `SELECT`

```sql
SELECT name, age
FROM employees
WHERE age > 25;
```

> DQL is often treated separately from DML to emphasize data retrieval, although `SELECT` is sometimes considered part of DML.

---

# 🗄️ SQL vs NoSQL

SQL and NoSQL are two different approaches to storing and managing data.

| Aspect              | SQL Databases                                     | NoSQL Databases                                   |
| ------------------- | ------------------------------------------------- | ------------------------------------------------- |
| **Data Model**      | Relational and table-based                        | Non-relational                                    |
| **Structure**       | Rows and columns                                  | Documents, key-value, graph, or wide-column       |
| **Schema**          | Fixed / predefined schema                         | Flexible / dynamic schema                         |
| **Query Language**  | Uses SQL                                          | Uses different query methods                      |
| **Scalability**     | Mainly vertically scalable                        | Mainly horizontally scalable                      |
| **ACID Compliance** | Strong ACID compliance                            | Varies by database                                |
| **Use Cases**       | Complex queries and transactional systems         | Large-scale and real-time applications            |
| **Relationships**   | Supports relationships using keys                 | Usually does not require predefined relationships |
| **Data Integrity**  | Strong data integrity and consistency             | Often prioritizes scalability and availability    |
| **Transactions**    | Strong transaction support                        | Support varies by database                        |
| **Performance**     | Optimized for structured data and complex queries | Optimized for large volumes and fast reads/writes |

## 📊 Data Storage

### SQL

SQL databases store structured data using **tables with rows and columns**.

Examples:

* PostgreSQL
* MySQL
* Oracle
* SQL Server

### NoSQL

NoSQL databases can store data using different models such as:

* Document
* Key-Value
* Wide-Column
* Graph

Examples:

* MongoDB
* Cassandra
* Redis
* Couchbase

## 🎯 SQL Databases Are Best Suited For

* Banking systems
* ERP systems
* Transactional applications
* Applications requiring complex queries
* Applications requiring strong data consistency

## 🚀 NoSQL Databases Are Best Suited For

* Social media platforms
* IoT applications
* Real-time analytics
* Big data applications
* Large-scale applications
