
26. **Can you have multiple `catch` blocks for a single `try` block?**  
    Yes, you can have multiple `catch` blocks to handle different exceptions separately.
```java
try {
    int result = 10 / 0;  // ArithmeticException
    String str = null;
    str.length();  // NullPointerException
} catch (ArithmeticException e) {
    System.out.println("Arithmetic error: " + e.getMessage());
} catch (NullPointerException e) {
    System.out.println("Null pointer error: " + e.getMessage());
}

```
    
27. **Can a `catch` block handle both checked and unchecked exceptions?**  
    Yes, as long as the exception type matches or the parent class (`Throwable`) is used.
```java
try {
    int[] arr = new int[2];
    arr[5] = 10;  // ArrayIndexOutOfBoundsException (unchecked)
} catch (Exception e) {  // Catches both checked and unchecked exceptions
    System.out.println("Exception caught: " + e.getMessage());
}

```
    
28. **Why is it not recommended to catch `Throwable` directly?**  
    It can catch critical errors (e.g., `OutOfMemoryError`) that the program cannot or should not handle.
```java
try {
    // Simulating error
    throw new OutOfMemoryError("Out of memory error");
} catch (Throwable e) {
    // This catches critical errors like OutOfMemoryError
    System.out.println("Caught error: " + e.getMessage());
}

```
    
29. **What is the purpose of the `throws` clause in method declarations?**  
    The `throws` clause informs the caller of the method that the method may throw specific exceptions, so the caller can handle them appropriately.