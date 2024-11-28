###### 1. What is the difference between `TRUNCATE`, `DELETE`, and `DROP` commands in SQL?

1. **TRUNCATE**:
    
    - Removes all rows from a table, but the table's structure and schema remain intact.
    - It is faster than `DELETE` as it doesn't log individual row deletions.
    - Cannot be rolled back (unless inside a transaction in some databases).
    - Resets any auto-increment counters.
2. **DELETE**:
    
    - Removes specific rows based on a `WHERE` condition. If no condition is provided, all rows can be deleted.
    - Logs each row deletion, making it slower than `TRUNCATE`.
    - Can be rolled back if used within a transaction.
3. **DROP**:
    
    - Deletes the entire table (or database), including its structure and schema.
    - Irreversible and permanently removes the object.

**Example:**

- `TRUNCATE TABLE customers;` – Deletes all data but keeps the `customers` table.
- `DELETE FROM customers WHERE id = 1;` – Deletes the row where `id = 1`.
- `DROP TABLE customers;` – Deletes the `customers` table entirely.

