`String` is a class in Java that represents a `sequence of characters`.
1. **String**: Immutable; changes create a new object.
2. **StringBuilder**: Mutable; modifies the same object.
3. **StringBuffer**: Mutable & thread-safe (slower than StringBuilder).

### String Creation
- **Literal**: Stored in the String Pool, reuses memory.
```java
String s1 = "Hello";
String s2 = "Hello"; // Same reference as s1
System.out.println(s1 == s2); // true
```
- **New Keyword**: Stored in the heap, no reuse.
```java
String s1 = new String("Hello");
String s2 = new String("Hello");
System.out.println(s1 == s2); // false
System.out.println(s1.equals(s2)); // true
```
#### **Why Immutable?**

- **Memory Optimization**: Reuses objects in the String Pool.
- **Thread Safety**: No synchronization needed.
- **Hashing**: Ensures stable hash codes in collections.
```java
String s = "Hello";
s = s + " World"; // New object created immutable
System.out.println(s); // Hello World

StringBuilder sb = new StringBuilder("Hello");
sb.append(" World"); // Same object modified
System.out.println(sb); // Hello World
```

Modifying String
```java
String s1 = "Hello";
s1.concat(" World"); 
System.out.println(s1); // Output: Hello (unchanged)
s1 = s1.concat(" World");
System.out.println(s1); // Output: Hello World

String s2 = new String("Hello");
s2.concat(" World");
System.out.println(s2); // Output: Hello (unchanged)
s2 = s2.concat(" World");
System.out.println(s2); // Output: Hello World
```

### Immutable and Mutable In Java
### **Immutable Classes in Java**

- **String**
- **Integer**
- **Float**
- **Double**
- **Character**
- **Boolean**
- **LocalDate** (from Java 8 onwards)
- **LocalTime** (from Java 8 onwards)
- **LocalDateTime** (from Java 8 onwards)
- **BigInteger**
- **BigDecimal**

### **Mutable Classes in Java**

- **StringBuilder**
- **StringBuffer**
- **ArrayList**
- **LinkedList**
- **HashMap**
- **TreeMap**
- **HashSet**
- **LinkedHashSet**
- **LinkedHashMap**
- **Vector**
- **Hashtable**

### **Explanation**

- **Immutable**: Objects cannot be changed after creation. Any modification creates a new object.
- **Mutable**: Objects can be modified after creation, and changes affect the same object.