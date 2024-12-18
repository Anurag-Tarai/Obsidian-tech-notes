
21. **What is a `NullPointerException`, and how can it be avoided?**  
    It occurs when trying to use an object reference that is `null`. Avoid it by:
    
    - Null checks.
    - Initializing objects before use.
    - Using `Optional` in Java 8+.
22. **What is an `OutOfMemoryError`, and what causes it?**  
    It occurs when the JVM runs out of heap memory, usually due to memory leaks or large data loads.
    `Memory leaks `- which occur when a program consumes memory but fails to release it when no longer needed
    `Large data loads` - **handling or processing of large volumes of data** at once.
    
23. **What is the difference between `ClassNotFoundException` and `NoClassDefFoundError`?**
    
    - `ClassNotFoundException`: Class was not found at runtime but was available during compilation.
    - `NoClassDefFoundError`: Class is missing in the runtime environment.
24. **What is an `IOException`, and when does it occur?**  
    It occurs during input-output operations, such as file reading/writing errors.
    
25. **What is a `SQLException`, and where is it commonly used?**  
    It occurs when a database access error happens, like syntax errors in SQL queries.