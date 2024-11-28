#### **Basic Concepts**

1. What is Exception is Java ?
	![[Pasted image 20241124121927.png]]
```java
java.lang.Object (Class)
    |
    +-- java.lang.Throwable (Class)
         |
         +-- java.lang.Exception (Class - for recoverable issues)
         |      |
         |      +-- java.lang.RuntimeException (Class - unchecked exceptions)
         |      |        |
         |      |        +-- NullPointerException (Class)
         |      |        +-- ArithmeticException (Class)
         |      |        +-- ArrayIndexOutOfBoundsException (Class)
         |      |
         |      +-- (Checked exceptions)
         |            |
         |            +-- IOException (Class)
         |            +-- SQLException (Class)
         |            +-- FileNotFoundException (Class)
         |
         +-- java.lang.Error (Class - serious issues)
                |
                +-- OutOfMemoryError (Class)
                +-- StackOverflowError (Class)


```

1. **What is exception handling in Java?**  
    It is a way to manage runtime errors and keep the program running smoothly.
    
2. **What are the benefits of using exception handling in Java?**
    
    - Ensures program stability.
    - Provides meaningful error messages to users.
    - Simplifies debugging.
    - Improves code maintainability.
3. **What are the types of exceptions in Java?**
	    
    - **Checked Exception**: Checked at compile time (e.g., `IOException`).
    - **Unchecked Exception**: Occur at runtime (e.g., `NullPointerException`).
    - **Error**: Serious issues (e.g., `OutOfMemoryError`).
4. **What is the superclass for all exceptions in Java?**  
    `Throwable`, with two main subclasses: `Exception` and `Error`.
    
5. **What is the difference between a checked exception, an unchecked exception, and an error?**
    
- **Checked Exception**:  
    These are exceptions checked at compile time. The programmer must handle them using a `try-catch` block or declare them with the `throws` keyword.  
    Example: `IOException`, `SQLException`.  
    **Instance of**: `Throwable -> Exception -> (Checked Exception)`.
    
- **Unchecked Exception**:  
    These are exceptions checked at runtime. Handling them is optional since they result from programming errors like invalid inputs.  
    Example: `NullPointerException`, `ArithmeticException`.  
    **Instance of**: `Throwable -> Exception -> RuntimeException`.
    
- **Error**:  
    Errors are serious issues related to the system or environment that the program cannot control or recover from.
    Example: `OutOfMemoryError`, `StackOverflowError`.  
    **Instance of**: `Throwable -> Error`.
6. **What happens if an exception is not handled in Java?**  
    If an exception is not handled in Java, the program will terminate unexpectedly, and the JVM will print a stack trace, showing the exception type, the error message.
    `Stack Trace `: A **stack trace** is a list of method calls that the program made before an exception occurred.