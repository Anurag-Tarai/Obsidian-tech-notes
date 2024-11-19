## Key
A **key** in SQL is a column or a set of columns in a table used to uniquely identify rows or establish relationships between tables. Keys ensure data integrity and consistency in databases.

### Types of Keys in SQL:

1. **Primary Key**:
    
    - Uniquely identifies each row in a table.
    - Does not allow `NULL` values.
    - Example:
        
        sql
        
        Copy code
        
        `CREATE TABLE Students (     StudentID INT PRIMARY KEY,     Name VARCHAR(50) );`
        
2. **Foreign Key**:
    
    - Links two tables by referencing the primary key in another table.
    - Maintains referential integrity.
    - Example:
        
        sql
        
        Copy code
        
        `CREATE TABLE Orders (     OrderID INT PRIMARY KEY,     StudentID INT,     FOREIGN KEY (StudentID) REFERENCES Students(StudentID) );`
        
3. **Unique Key**:
    
    - Ensures all values in the column are unique, but allows one `NULL`.
    - Example:
        
        sql
        
        Copy code
        
        `CREATE TABLE Employees (     EmployeeID INT UNIQUE,     Name VARCHAR(50) );`
        
4. **Candidate Key**:
    
    - Any column(s) that can serve as a primary key (uniquely identifies rows).
5. **Composite Key**:
    
    - A combination of two or more columns to uniquely identify rows in a table.
    - Example:
        
        sql
        
        Copy code
        
        `CREATE TABLE Enrollment (     StudentID INT,     CourseID INT,     PRIMARY KEY (StudentID, CourseID) );`
        
6. **Alternate Key**:
    
    - Candidate keys that are not chosen as the primary key.

7. Super key - A **Super Key** is a column or a combination of columns that uniquely identifies each row in a table.