```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");                    // Add elements
        list.add("Banana");
        list.add(1, "Cherry");                // Add at index
        list.remove("Banana");               // Remove by value
        list.remove(0);                      // Remove by index
        System.out.println(list.get(0));    // Get element
        list.set(0, "Berry");               // Update element
        System.out.println(list.size());   // List size
        System.out.println(list.contains("Berry")); // Check existence
        list.clear();                      // Clear list
    }
}
```