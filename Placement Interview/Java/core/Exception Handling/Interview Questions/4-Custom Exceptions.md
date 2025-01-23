
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

Example :
```java
// Custom checked exception by extending Exception class
public class InsufficientBalanceException extends Exception {
    // Constructor with custom error message
    public InsufficientBalanceException(String message) {
        super(message);
    }
    
    // Constructor with custom error message and cause
    public InsufficientBalanceException(String message, Throwable cause) {
        super(message, cause);
    }
}
```

```java
public class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance = balance;
    }

    // Method to withdraw money, throws custom exception
    public void withdraw(double amount) throws InsufficientBalanceException {
        if (amount > balance) {
            throw new InsufficientBalanceException("Insufficient balance for withdrawal.");
        }
        balance -= amount;
    }

    public static void main(String[] args) {
        BankAccount account = new BankAccount(500.00);
        try {
            account.withdraw(600.00);  // This will throw the custom exception
        } catch (InsufficientBalanceException e) {
            System.out.println(e.getMessage());
        }
    }
}

```