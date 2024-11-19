### **Basics of SQL**

1. What is SQL, and what are its main uses?
2. What are DDL, DML, DCL, and TCL commands? Give examples of each.
3. What is the difference between `DELETE` and `TRUNCATE` commands?
4. Explain the difference between `WHERE` and `HAVING` clauses.
5. What are constraints in SQL? List the types.
6. What is the difference between `PRIMARY KEY` and `UNIQUE`?

---

### **SQL Queries**

7. Write a query to retrieve all records from a table.
    
    sql
    
    Copy code
    
    `SELECT * FROM table_name;`
    
8. Write a query to fetch only unique values from a column.
    
    sql
    
    Copy code
    
    `SELECT DISTINCT column_name FROM table_name;`
    
9. Write a query to filter records based on a condition.
    
    sql
    
    Copy code
    
    `SELECT * FROM table_name WHERE column_name = 'value';`
    
10. How do you sort data in ascending or descending order?

sql

Copy code

`SELECT * FROM table_name ORDER BY column_name ASC; -- or DESC`

11. Write a query to count the number of rows in a table.

sql

Copy code

`SELECT COUNT(*) FROM table_name;`

---

### **Joins**

12. What are the types of joins in SQL? Explain with examples.
13. Write a query to perform an `INNER JOIN` between two tables.

sql

Copy code

`SELECT a.column1, b.column2 FROM table1 a INNER JOIN table2 b ON a.common_column = b.common_column;`

14. Write a query to fetch unmatched records using `LEFT JOIN`.
15. Explain the difference between `CROSS JOIN` and `SELF JOIN`.

---

### **Aggregate Functions**

16. Explain `COUNT()`, `SUM()`, `AVG()`, `MAX()`, and `MIN()` functions.
17. Write a query to calculate the total salary of employees.

sql

Copy code

`SELECT SUM(salary) FROM employees;`

18. How do you group data in SQL? Use `GROUP BY` with an example.

sql

Copy code

`SELECT department, COUNT(*) FROM employees GROUP BY department;`

---

### **Advanced Topics for Freshers**

19. What is a subquery? Write an example.

sql

Copy code

`SELECT * FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);`

20. What is a view in SQL? How is it created?

sql

Copy code

`CREATE VIEW view_name AS SELECT column1, column2 FROM table_name WHERE condition;`

21. Write a query using the `LIKE` operator to search for names starting with 'A'.

sql

Copy code

`SELECT * FROM table_name WHERE name LIKE 'A%';`

22. What is the difference between `UNION` and `UNION ALL`?
23. What are stored procedures and how are they created?

---

### **Indexes and Optimization**

24. What is an index in SQL? Why is it used?
25. Write a query to create an index on a column.

sql

Copy code

`CREATE INDEX index_name ON table_name(column_name);`

26. How would you find duplicate records in a table?

sql

Copy code

`SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > 1;`

---

### **Miscellaneous**

27. How do you handle NULL values in SQL? Write a query using `IS NULL` and `COALESCE`.
28. What are triggers in SQL? Write a basic example.
29. Explain the difference between `RANK()`, `DENSE_RANK()`, and `ROW_NUMBER()`.
30. What are transactions? Explain `COMMIT`, `ROLLBACK`, and `SAVEPOINT`.