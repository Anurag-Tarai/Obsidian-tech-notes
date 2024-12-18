### **1. Basics of SQL**

- Introduction to SQL and RDBMS
- Database, Table, and Schema
- SQL Syntax
- Data Types: Numeric, String, Date/Time

---

### **2. SQL Statements**

#### **Data Definition Language (DDL)**

- `CREATE`: Create databases, tables, views, indexes
- `ALTER`: Modify structure (add, drop, modify columns)
- `DROP`: Delete database or table
- `TRUNCATE`: Delete all rows from a table

#### **Data Manipulation Language (DML)**

- `INSERT`: Insert records into tables
- `UPDATE`: Modify existing records
- `DELETE`: Remove records

#### **Data Query Language (DQL)**

- `SELECT`: Retrieve data
    - `DISTINCT`
    - `WHERE` with conditions
    - Aliases (`AS`)
    - Ordering (`ORDER BY`)
    - Filtering (`LIMIT`, `OFFSET`)

#### **Transaction Control Language (TCL)**

- `COMMIT`: Save changes permanently
- `ROLLBACK`: Undo changes
- `SAVEPOINT`: Partial rollback

#### **Data Control Language (DCL)**

- `GRANT`: Provide access
- `REVOKE`: Remove access

---

### **3. Constraints**

- **Primary Key**
- **Foreign Key**
- **Unique**
- **Not Null**
- **Default**
- **Check**

---

### **4. SQL Joins**

- **Inner Join**
- **Left Join (Outer Join)**
- **Right Join (Outer Join)**
- **Full Outer Join**
- **Cross Join**
- **Self Join**

---

### **5. Subqueries and Nested Queries**

- Single-row subqueries
- Multi-row subqueries
- Correlated subqueries

---

### **6. SQL Functions**

#### **Aggregate Functions**

- `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`

#### **String Functions**

- `CONCAT`, `LENGTH`, `UPPER`, `LOWER`, `SUBSTRING`, `TRIM`

#### **Numeric Functions**

- `ROUND`, `FLOOR`, `CEIL`

#### **Date/Time Functions**

- `NOW`, `CURDATE`, `DATEADD`, `DATEDIFF`

#### **Other Functions**

- `COALESCE`, `NULLIF`

---

### **7. Advanced Queries**

- Grouping (`GROUP BY`, `HAVING`)
- Conditional expressions (`CASE`, `IF`)

---

### **8. Views**

- Creating and managing views
- Updatable views

---

### **9. Indexes**

- Clustered and Non-Clustered
- Creating indexes
- Index performance

---

### **10. Transactions**

- ACID properties (Atomicity, Consistency, Isolation, Durability)
- Isolation levels (Read Uncommitted, Read Committed, Repeatable Read, Serializable)

---

### **11. Triggers**

- BEFORE and AFTER triggers
- Row-level vs. statement-level triggers

---

### **12. Stored Procedures and Functions**

- Creating and calling stored procedures
- User-defined functions (UDF)

---

### **13. Recursive Queries**

- Common Table Expressions (CTEs)
- Recursive CTEs

---

### **14. Optimization**

- Query optimization techniques
- Execution plans (`EXPLAIN`, `EXPLAIN ANALYZE`)
- Indexing for performance

---

### **15. Security**

- Roles and permissions
- Encrypting data
- SQL injection prevention

---

### **16. NoSQL Features in SQL (Optional)**

- JSON support (`JSON_EXTRACT`, `JSON_ARRAY`)
- XML processing

---

### **17. Database Design**

- Normalization (1NF, 2NF, 3NF, BCNF)
- Denormalization
- Entity-Relationship (ER) Modeling

---

### **18. Backup and Restore**

- `BACKUP DATABASE`
- `RESTORE DATABASE`