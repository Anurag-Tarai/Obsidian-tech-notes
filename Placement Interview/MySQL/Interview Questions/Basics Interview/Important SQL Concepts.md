1. Date Difference : DATEDIFF( )
```sql
SELECT * FROM orders WHERE DATEDIFF(current_date, placed_date) > 30;
```
you can use following to find the current date
	- **MySQL**: `NOW()` or `CURDATE()`
    - **PostgreSQL**: `CURRENT_DATE`
    - **Oracle**: `SYSDATE`
    - **SQL Server**: `GETDATE()`
```sql
SELECT * FROM orders WHERE DATEDIFF(NOW(), placed_date) > 30;
```

2. Aggregate function
**Find the total number of employees and their average salary from the `employees` table**:
```sql
SELECT COUNT(*) AS total_employees, AVG(salary) AS average_salary
FROM employees;
```
**Calculate the maximum price of products in the `products` table**:
```sql
SELECT MAX(price) AS max_price
FROM products;
```