Here are the types of SQL commands with examples:

1. **Data Definition Language (DDL)**  
    Used to define or modify database structure.
        
```sql
CREATE TABLE Students (
    ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT
);
ALTER TABLE Students ADD Gender VARCHAR(10);
DROP TABLE Students;

```
      
2. **Data Manipulation Language (DML)**  
    Used to manipulate data in the database.
    
```sql
INSERT INTO Students (ID, Name, Age, Gender) VALUES (1, 'Alice', 20, 'Female');
UPDATE Students SET Age = 21 WHERE ID = 1;
DELETE FROM Students WHERE ID = 1;
```
        
3. **Data Query Language (DQL)**  
    Used to retrieve data from the database.
    
```sql
SELECT * FROM Students WHERE Age > 18;

```
        
4. **Data Control Language (DCL)**  
    Used to control access to data in the database.
    
```sql
GRANT SELECT ON Students TO User1;
REVOKE SELECT ON Students FROM User1;

```
        
5. **Transaction Control Language (TCL)**  
    Used to manage transactions in the database.
    
```sql
BEGIN TRANSACTION;
INSERT INTO Students (ID, Name, Age, Gender) VALUES (2, 'Bob', 22, 'Male');
COMMIT;
-- or ROLLBACK if needed

```