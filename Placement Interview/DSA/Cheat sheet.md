### **Step 1: Core Java Syntax Overview (15 minutes)**

- **Data Types**: `int`, `double`, `float`, `char`, `boolean`, `String`.
- **Control Structures**:
    
    java
    
    Copy code
    
    `if (condition) {...} else {...} for (int i = 0; i < n; i++) {...} while (condition) {...} do {...} while (condition); switch (variable) {...}`
    
- **Operators**: `+`, `-`, `*`, `/`, `%`, `==`, `!=`, `&&`, `||`, `!`.
- **Arrays**:
    
    java
    
    Copy code
    
    `int[] arr = {1, 2, 3}; int[] arr = new int[size]; Arrays.sort(arr);`
    

---

### **Step 2: Java Methods Quick Reference (20 minutes)**

#### **String Methods**:

java

Copy code

`str.length(); str.charAt(index); str.substring(start, end); str.equals(anotherStr); str.contains("text"); str.indexOf('a'); str.toUpperCase(); str.toLowerCase(); str.split("regex");`

#### **Math Class**:

java

Copy code

`Math.max(a, b); Math.min(a, b); Math.sqrt(num); Math.pow(base, exp); Math.abs(num); Math.random();`

#### **Collections Framework**:

- **List**:
    
    java
    
    Copy code
    
    `List<Integer> list = new ArrayList<>(); list.add(value); list.remove(index); list.get(index); list.size(); Collections.sort(list);`
    
- **Set**:
    
    java
    
    Copy code
    
    `Set<Integer> set = new HashSet<>(); set.add(value); set.contains(value); set.remove(value);`
    
- **Map**:
    
    java
    
    Copy code
    
    `Map<Integer, String> map = new HashMap<>(); map.put(key, value); map.get(key); map.remove(key); map.containsKey(key); map.containsValue(value);`
    

#### **Stream API**:

java

Copy code

`list.stream().filter(x -> x > 10).collect(Collectors.toList()); list.stream().map(x -> x * 2).collect(Collectors.toList());`

---

### **Step 3: Practice Common Code Patterns (15 minutes)**

- **Sorting an Array**:
    
    java
    
    Copy code
    
    `Arrays.sort(arr);`
    
- **Reverse a String**:
    
    java
    
    Copy code
    
    `new StringBuilder(str).reverse().toString();`
    
- **Binary Search**:
    
    java
    
    Copy code
    
    `Arrays.binarySearch(arr, key);`
    
- **Fibonacci Sequence**:
    
    java
    
    Copy code
    
    `int a = 0, b = 1, c; for (int i = 0; i < n; i++) {     System.out.print(a + " ");     c = a + b;     a = b;     b = c; }`
    
- **Factorial**:
    
    java
    
    Copy code
    
    `int factorial(int n) {     return (n == 1 || n == 0) ? 1 : n * factorial(n - 1); }`
    

---

### **Step 4: Focus on Object-Oriented Concepts (10 minutes)**

- **Class and Object**:
    
    java
    
    Copy code
    
    `class Person {     String name;     int age;      Person(String name, int age) {         this.name = name;         this.age = age;     }      void display() {         System.out.println(name + " " + age);     } }  Person p = new Person("John", 25); p.display();`
    
- **Inheritance**:
    
    java
    
    Copy code
    
    `class Animal {...} class Dog extends Animal {...}`
    
- **Polymorphism**:
    
    java
    
    Copy code
    
    `Animal a = new Dog();`
    
- **Interfaces**:
    
    java
    
    Copy code
    
    `interface Animal {...} class Dog implements Animal {...}`
    

---

### **Step 5: Mock Coding Problems (10 minutes)**

Pick **3 easy problems** from LeetCode, HackerRank, or write sample code snippets:

1. Find the sum of an array.
2. Reverse a linked list.
3. Merge two sorted arrays