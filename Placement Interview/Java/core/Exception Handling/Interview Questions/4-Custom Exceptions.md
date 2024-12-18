
16. **How can you create a custom exception in Java?**  
    Extend `Exception` for checked exceptions or `RuntimeException` for unchecked exceptions.  
    Example:
```java
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

```
    
17. **What is the difference between extending `Exception` and `RuntimeException`?**
    
    - Extending `Exception`: Creates a checked exception requiring handling.
    - Extending `RuntimeException`: Creates an unchecked exception, not requiring handling.
