A **constraint** in SQL is a rule that controls what kind of data can be added to a table to keep it correct and organized.
### 1. **NOT NULL**

Ensures that a column cannot have a `NULL` value.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Students (     ID INT NOT NULL,     Name VARCHAR(50) NOT NULL );`
    

### 2. **UNIQUE**

Ensures that all values in a column are distinct.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Employees (     EmployeeID INT UNIQUE,     Email VARCHAR(100) UNIQUE );`
    

### 3. **PRIMARY KEY**

Combines `NOT NULL` and `UNIQUE`. Each table can have only one primary key.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Orders (     OrderID INT PRIMARY KEY,     OrderDate DATE );`
    

### 4. **FOREIGN KEY**

Establishes a relationship between two tables.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Orders (     OrderID INT PRIMARY KEY,     CustomerID INT,     FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID) );`
    

### 5. **CHECK**

Ensures that all values in a column satisfy a specific condition.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Products (     ProductID INT,     Price DECIMAL(10, 2),     CHECK (Price > 0) );`
    

### 6. **DEFAULT**

Sets a default value for a column if no value is provided.

- Example:
    
    sql
    
    Copy code
    
    `CREATE TABLE Users (     UserID INT,     RegistrationDate DATE DEFAULT GETDATE() );`
    

### 7. **INDEX** (Constraint-like)

Improves query performance by indexing one or more columns.

- Example:
    
    sql
    
    Copy code
    
    `CREATE INDEX idx_name ON Students(Name);`
    

These constraints help maintain the quality and consistency of the data in a database.