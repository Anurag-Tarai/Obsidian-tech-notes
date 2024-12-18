### **Core Concepts**

1. **Database vs. DBMS**
    
    - **Database**: Organized collection of data (e.g., a library).
    - **DBMS (Database Management System)**: Software to manage databases (e.g., MySQL, PostgreSQL).
2. **Data Models**
    
    - Define the logical structure of data.
        - **Relational Model**: Tables (most widely used).
        - **Hierarchical Model**: Tree-like structure.
        - **Network Model**: Complex relationships using graphs.
3. **Keys**
    
    - **Primary Key**: Uniquely identifies each record in a table.
    - **Foreign Key**: Links two tables by referencing the primary key in another table.
    - **Candidate Key**: Possible unique identifiers (but only one can be the primary key).
    - **Composite Key**: Combination of two or more attributes to uniquely identify a record.
4. **Normalization**
    
    - Process to reduce redundancy and improve database structure.
        - **1NF**: Eliminate duplicate columns.
        - **2NF**: Remove partial dependencies.
        - **3NF**: Remove transitive dependencies.
        - **BCNF**: Special case of 3NF for better optimization.
5. **Entity-Relationship (ER) Model**
    
    - **Entity**: Real-world objects (e.g., Student).
    - **Attribute**: Properties of an entity (e.g., Name, Age).
    - **Relationship**: Association between entities (e.g., Student enrolls in a Course).

---

### **SQL Basics**

6. **SQL Commands**
    
    - **DDL (Data Definition Language)**: Create/modify tables (e.g., `CREATE`, `ALTER`).
    - **DML (Data Manipulation Language)**: Modify data (e.g., `INSERT`, `UPDATE`).
    - **DQL (Data Query Language)**: Retrieve data (e.g., `SELECT`).
    - **DCL (Data Control Language)**: Permissions (e.g., `GRANT`, `REVOKE`).
    - **TCL (Transaction Control Language)**: Manage transactions (e.g., `COMMIT`, `ROLLBACK`).
7. **Joins**
    
    - Combine data from multiple tables:
        - **INNER JOIN**: Matching rows only.
        - **LEFT JOIN**: All rows from the left table, matching rows from the right.
        - **RIGHT JOIN**: All rows from the right table, matching rows from the left.
        - **FULL JOIN**: All rows from both tables.
8. **Subqueries**
    
    - **Correlated**: Uses data from the outer query.
    - **Non-Correlated**: Independent query inside another query.
9. **Views**
    
    - Virtual tables created using SQL queries. Useful for security and simplicity.
10. **Constraints**
    

- Rules applied to columns:
    - **NOT NULL**: Prevents null values.
    - **UNIQUE**: Ensures no duplicate values.
    - **CHECK**: Enforces a condition.
    - **DEFAULT**: Sets a default value for a column.

---

### **Advanced Topics**

11. **Indexing**

- Improves query performance by creating a data structure for quick lookups.
    - **Clustered Index**: Physically sorts the table data.
    - **Non-Clustered Index**: Logical pointer to table data.

12. **Transactions**

- Group of operations treated as a single unit. Follow **ACID properties**:
    - **Atomicity**: All or nothing.
    - **Consistency**: Keeps data valid.
    - **Isolation**: Prevents conflicts between transactions.
    - **Durability**: Changes persist even after a failure.

13. **Triggers**

- Automated actions triggered by specific events on a table (e.g., `AFTER INSERT`).

14. **Stored Procedures and Functions**

- **Stored Procedure**: Precompiled SQL statements to execute logic.
- **Function**: Returns a value and can be used in queries.

15. **Database Locking**

- Mechanism to control access to the database.
    - **Shared Lock**: Multiple reads but no writes.
    - **Exclusive Lock**: No other reads or writes allowed.

---

### **Other Essentials**

16. **Denormalization**

- Adding redundancy to improve read performance, often used in NoSQL databases.

17. **SQL vs. NoSQL**

- **SQL**: Relational, structured schema (e.g., MySQL).
- **NoSQL**: Flexible, document-based (e.g., MongoDB).

18. **Data Integrity**

- Maintains accuracy and consistency of data. Types: Entity, Referential, and Domain Integrity.

19. **Database Backup and Recovery**

- Strategies to prevent data loss (e.g., full, incremental backups).

20. **Deadlocks**

- Occur when two transactions wait indefinitely for each other to release locks. Use **timeouts** or **deadlock prevention** to avoid.