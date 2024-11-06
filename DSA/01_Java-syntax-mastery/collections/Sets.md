- Interface and part of Java collection frame work.
- A `Set` in Java is a **collection** that **does not allow duplicate elements**.
- Unordered, does not have indexing have to use advance for loop.
- `HashSet`, `LinkedSet`, `TreeSet`
### HashSet
```java
Set<Integer> hashSet = new HashSet<>();
```
##### Operations
```java
set.add(1); // Adds 1 to the set

set.remove(1); // Removes 1 from the set

boolean exists = set.contains(2);

int size = set.size();

boolean empty = set.isEmpty();

set.clear(); // Clear the set

set.addAll(anotherSet); // Adds all elements from anotherSet to set

set.removeAll(anotherSet); // Removes all common elements between set and anotherSet

set.retainAll(anotherSet);  // Keeps only common elements between set and anotherSet

boolean isEqual = set.equals(anotherSet);  // Checks if two sets are equal


for (int num : set) {
System.out.println(num); // Iterate over the set elements 
}
```
