```java
import java.util.ArrayDeque;
import java.util.Deque;

public class Main {
    public static void main(String[] args) {
        Deque<Integer> deque = new ArrayDeque<>();

        // Add elements
        deque.addFirst(10); // Add to front
        deque.addLast(20);  // Add to rear

        // Access elements
        System.out.println("First: " + deque.peekFirst()); // 10
        System.out.println("Last: " + deque.peekLast());   // 20

        // Remove elements
        deque.pollFirst(); // Remove front
        deque.pollLast();  // Remove rear

        // Use as Stack
        deque.push(30); // Push to front
        System.out.println("Popped: " + deque.pop()); // Remove front (LIFO)
    }
}
```