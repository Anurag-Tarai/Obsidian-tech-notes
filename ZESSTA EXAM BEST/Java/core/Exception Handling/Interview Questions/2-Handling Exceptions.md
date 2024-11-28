
7. **What is a `try-catch` block, and how is it used in Java?**  
    A `try` block encloses code that might throw exceptions, while `catch` handles those exceptions.
    
8. **Can a `try` block exist without a `catch` block?**  
    Yes, if a `finally` block is used for cleanup actions. "Cleanup actions" refer to tasks that should be performed after the main logic of the program
    
9. **What is the purpose of the `finally` block?**  
    It ensures that essential code (like resource release) is executed regardless of exceptions.
```java
import java.io.*;

public class FileExample {
    public static void main(String[] args) {
        FileReader reader = null;
        try {
            reader = new FileReader("file.txt");
            int data = reader.read();  // Some operation that might throw an exception
        } catch (IOException e) {
            System.out.println("An error occurred while reading the file.");
        } finally {
            try {
                if (reader != null) {
                    reader.close();  // Ensure the file is closed
                    System.out.println("File closed.");
                }
            } catch (IOException e) {
                System.out.println("Error closing the file.");
            }
        }
    }
}

```
10. **What is the difference between `throw` and `throws`?**
    
    - `throw`: Used to explicitly throw an exception.
    - `throws`: Declares exceptions a method might throw.
11. **How can multiple exceptions be handled in a single `try` block?**
    
    - Use multiple `catch` blocks.
    - Use multi-catch (`|` operator) for related exceptions.