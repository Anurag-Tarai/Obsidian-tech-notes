### **SQL Joins: Questions with Answers**

---

#### **Basic Questions**

1. **What is a SQL Join?**  
    A SQL Join combines rows from two or more tables based on a related column.
    
2. **Explain the differences between Inner Join and Outer Join.**
    
    - **Inner Join:** Returns rows with matching values in both tables.
    - **Outer Join:** Returns all rows from one or both tables, with `NULL` for non-matching rows.
3. **What is the syntax for an Inner Join?**
    
    `SELECT columns   FROM Table1   INNER JOIN Table2   ON Table1.column = Table2.column;`
    
4. **What is the purpose of a Left Join?**  
    To retrieve all rows from the left table and matching rows from the right table. Non-matching rows in the right table are returned as `NULL`.
    
5. **What happens when there are no matches in a Right Join?**  
    Rows from the right table are included, with `NULL` in the columns of the left table for non-matches.
    
6. **Explain Full Outer Join with an example.**  
    A Full Outer Join retrieves all rows from both tables, with `NULL` for non-matching rows.
    
    `SELECT columns   FROM Table1   FULL OUTER JOIN Table2   ON Table1.column = Table2.column;`
    MySql does not support full outer join : emulated using unio - left and right
    
7. **What is a Cross Join?**  
    A Cross Join produces a Cartesian product, combining each row from the first table with every row in the second table.
    
8. **Define Self Join.**  
    A Self Join is when a table is joined with itself using table aliases.
    

