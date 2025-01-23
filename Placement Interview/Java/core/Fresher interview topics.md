## 1. Core Java Concepts

- **Introduction to Java**: JVM, JRE, JDK, platform independence
- **Data Types**: Primitive and reference types
- **Operators**: Arithmetic, logical, bitwise, relational, assignment
- **Control Flow Statements**: `if-else`, `switch`, loops (`for`, `while`, `do-while`)
- **Arrays**: Single-dimensional and multi-dimensional arrays

### 2. **Object-Oriented Programming (OOP) Concepts**

- **Class and Object**: Class structure, fields, methods, constructors
- **Encapsulation**: Private fields, getter and setter methods
- **Inheritance**: `extends` keyword, method overriding, `super` keyword
- **Polymorphism**: Compile-time (method overloading) and runtime (method overriding)
- **Abstraction**: Abstract classes, interfaces
- **Access Modifiers**: `private`, `protected`, `public`, default

## 3. Exception Handling

- **Types of Exceptions**: Checked and unchecked exceptions
- **Try-Catch Blocks**: Handling exceptions with `try`, `catch`, `finally`
- **Throw and Throws**: Manually throwing exceptions, method signature
- **Custom Exceptions**: Creating user-defined exceptions

## 4. Collections Framework

- **List Interface**: `ArrayList`, `LinkedList`
- **Set Interface**: `HashSet`, `TreeSet`, `LinkedHashSet`
- **Map Interface**: `HashMap`, `TreeMap`, `LinkedHashMap`
- **Queue Interface**: `PriorityQueue`, `Deque`
- **Iterators**: `Iterator`, `ListIterator`, `for-each` loop
- **Collections Utility Class**: Sorting, searching, and other utilities

## 5. Strings

- **String Class**: Immutability, `equals()` vs `==`, `compareTo()`, `substring()`, `length()`, `charAt()`, `replace()`
- **StringBuilder and StringBuffer**: Mutable strings, performance considerations

### 6. **Java I/O (Input/Output)**

- **File Handling**: `File` class, reading and writing files
- **Streams**: InputStream, OutputStream, Reader, Writer
- **Serialization**: `Serializable` interface, `ObjectOutputStream`, `ObjectInputStream`

### 7. **Multithreading and Concurrency**

- **Thread Lifecycle**: `new`, `runnable`, `blocked`, `waiting`, `terminated`
- **Creating Threads**: Extending `Thread` class, implementing `Runnable` interface
- **Synchronization**: `synchronized` keyword, static synchronization
- **Inter-thread Communication**: `wait()`, `notify()`, `notifyAll()`
- **Executor Framework**: Using `ExecutorService`, `Callable`, `Future`
- **Concurrency Utilities**: `CountDownLatch`, `CyclicBarrier`

### 8. **Java 8 Features**

- **Lambda Expressions**: Syntax, functional interfaces
- **Streams API**: Operations like `filter()`, `map()`, `reduce()`
- **Functional Interfaces**: `Predicate`, `Function`, `Consumer`, `Supplier`
- **Optional Class**: Handling null values in Java
- **Method References**: Reference to static and instance methods

### 9. **Generics**

- **Generic Classes and Methods**: Type parameters, bounded types, wildcards (`?`, `? extends T`, `? super T`)
- **Generic Collections**: Using generics in `List`, `Set`, `Map`

### 10. **Memory Management**

- **Heap and Stack Memory**: How objects and variables are stored
- **Garbage Collection**: How Java manages memory, finalize method
- **Memory Leaks**: Common causes and how to avoid them