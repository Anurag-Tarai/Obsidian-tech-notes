### **[[1. Basics of SQL and RDBMS]]**

1. What is SQL, and what are its primary uses?
2. Define RDBMS. How does it differ from DBMS?
3. Explain the CRUD operations in SQL.
4. What is the difference between SQL and MySQL?
5. How is data stored in an RDBMS?

---

### **[[2. SQL Data Types]]**

6. What are the different types of SQL data types?
7. What is the difference between `CHAR` and `VARCHAR`?
8. Explain the difference between `TEXT`, `BLOB`, and their variants like `TINYTEXT`, `MEDIUMTEXT`.
9. What is the size hierarchy of integer data types like `TINYINT`, `SMALLINT`, and `BIGINT`?
10. When would you use `ENUM` or `SET` data types?

---

### **[[3. SQL Command Types]]**

11. What are the different types of SQL commands, and what do they do?
12. Explain DDL commands and give examples.
13. What is the difference between `TRUNCATE`, `DELETE`, and `DROP`?
14. What is the purpose of DCL commands like `GRANT` and `REVOKE`?
15. What is the difference between `COMMIT` and `ROLLBACK` in TCL?

---

### **[[4. Database Management]]**

16. How do you create a database in SQL?
17. How do you switch between databases?
18. Explain the purpose of the `SHOW DATABASES` and `SHOW TABLES` commands.
19. Can a database with the same name exist multiple times? Explain with an example.
20. What happens if you execute `DROP DATABASE` without checking its existence?

---

### **[[5. Data Retrieval (DRL or DQL)]]**

21. What is the syntax for the `SELECT` statement?
22. Can we use `SELECT` without specifying a `FROM` clause? Provide examples.
23. Explain the purpose of the `WHERE` clause.
24. What is the difference between `BETWEEN` and `IN` clauses?
25. How are pattern matching operators (`%` and `_`) used with `LIKE`?

---

### **[[6. Advanced Retrieval]]**

26. What is the difference between `DISTINCT` and `GROUP BY`?
27. Explain the difference between `WHERE` and `HAVING` clauses.
28. What is the purpose of the `ORDER BY` clause? How is it different from `GROUP BY`?
29. How can you sort the result of a query in descending order?
30. Explain the use of aggregate functions like `COUNT()`, `SUM()`, `AVG()`, `MIN()`, and `MAX()`.

---

### **[[7. Constraints]]**

31. What is a primary key, and what are its characteristics?
32. Explain the concept of a foreign key.
33. What is the difference between `UNIQUE` and `PRIMARY KEY` constraints?
34. How does the `CHECK` constraint work? Provide an example.
35. What is the purpose of the `DEFAULT` constraint?

---

### **[[8. ALTER Operations]]**

36. How do you add a new column to an existing table?
37. What is the difference between `MODIFY` and `CHANGE` commands?
38. How can you rename a column or table in SQL?
39. How do you delete a column from an existing table?
40. How is the `DROP COLUMN` command different from `ALTER`?

---

### **[[9. Data Manipulation (DML)]]**

41. How do you insert data into a table?
42. Explain the difference between `INSERT` and `REPLACE`.
43. How do you update a specific row in a table?
44. What happens if you execute an `UPDATE` statement without a `WHERE` clause?
45. What is `ON UPDATE CASCADE`, and where is it used?

---

### **[[10. Advanced DML]]**

46. How do you delete rows from a table using the `DELETE` statement?
47. What is the purpose of `ON DELETE CASCADE` and `ON DELETE SET NULL`?
48. How does the `REPLACE INTO` command work as both an `INSERT` and an `UPDATE`?
49. What is the difference between `REPLACE` and `INSERT ON DUPLICATE KEY UPDATE`?
50. How do you manage referential integrity constraints in SQL?

---

### **11. Miscellaneous and Best Practices**

51. What is a dual table, and how is it used?
52. Explain the difference between `UNION` and `UNION ALL`.
53. What is a transaction in SQL, and how do you ensure its atomicity?
54. Why are variable-length data types like `VARCHAR` preferred over fixed-length types?
55. What are the advantages of using indexes in a database?

---

### **12. Query Optimization**

56. How can you optimize queries that retrieve large amounts of data?
57. What is the role of indexing in SQL query performance?
58. When should you use subqueries instead of joins?
59. Explain the use of the `EXPLAIN` keyword in SQL query optimization.
60. How does query execution order affect performance?