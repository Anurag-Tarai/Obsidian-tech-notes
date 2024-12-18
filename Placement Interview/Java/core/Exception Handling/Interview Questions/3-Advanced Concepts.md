
12. **What is exception propagation in Java?**  
    Exception propagation is the process where an exception moves up the call stack, looking for a `catch` block to handle it. If it doesn't find one, the program terminates.
```java
public class ExceptionPropagationExample {
    
    public static void main(String[] args) {
        try {
            method1();
        } catch (ArithmeticException e) {
            System.out.println("Caught exception in main: " + e.getMessage());
        }
    }
    
    public static void method1() {
        method2();
    }
    
    public static void method2() {
        int result = 10 / 0;  // This will throw ArithmeticException
    }
}

```
### Explanation:

- When `method2()` tries to divide by 0, an `ArithmeticException` is thrown.
- The exception is **not caught in `method2()`**, so it propagates (moves) to `method1()`.
- Since `method1()` doesn’t have a `catch` block either, the exception keeps moving up to the `main()` method.
- In `main()`, the exception is **caught** by the `catch` block and handled, printing the message "Caught exception in main: / by zero."

If no `catch` block existed in `main()`, the program would terminate.
    
13. **What is a multi-catch block in Java?**  
    A multi-catch block allows handling multiple exceptions in a single `catch` block using the `|` operator.
    
14. **What is `try-with-resources`, and why is it used?**  
    Introduced in Java 7, `try-with-resources` automatically closes resources like files or streams after use.  
```java
try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
    System.out.println(br.readLine());
}

```
    
15. **What happens if an exception is thrown in the `finally` block?**  
    If an exception is thrown in the `finally` block, it overrides any exception thrown earlier in the `try` or `catch` block, potentially hiding the original exception.