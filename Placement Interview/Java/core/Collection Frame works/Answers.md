1. **What is a Collection in Java, and why is it used?** A Collection is a framework that provides an architecture to store and manipulate a group of objects. It is used to perform data operations such as searching, sorting, insertion, deletion, and manipulation of data.
    
2. **What is the difference between** `**ArrayList**` **and** `**LinkedList**`**?**
    
    - `ArrayList` is based on a dynamic array that allows random access, but inserting or deleting elements is slow as elements need to be shifted.
        
    - `LinkedList` is based on a doubly linked list, allowing faster insertion and deletion at the cost of slower access.
        
3. **What is the difference between** `**Set**` **and** `**List**` **in Java?**
    
    - `List` allows duplicate elements and maintains insertion order.
        
    - `Set` does not allow duplicates and does not guarantee order.
        
4. **What is a** `**HashMap**`**, and how is it different from a** `**Hashtable**`**?**
    
    - `HashMap` allows one null key and multiple null values, is non-synchronized, and faster than `Hashtable`.
        
    - `Hashtable` is synchronized and does not allow null keys or values.
        
5. **What is a** `**HashSet**`**, and how does it ensure unique elements?**
    
    - `HashSet` uses a `HashMap` internally to store elements. It does not allow duplicate elements because it uses hashing to check if an element is already present.
        
6. **What is the purpose of an** `**Iterator**` **in Java?**
    
    - `Iterator` is used to traverse through a collection, one element at a time. It can be used to remove elements from the collection during iteration.
        
7. **What is the difference between** `**HashMap**` **and** `**TreeMap**`**?**
    
    - `HashMap` stores key-value pairs in random order, whereas `TreeMap` stores them in sorted order (based on natural order or a custom comparator).
        
8. **What happens if you try to insert a duplicate key into a** `**HashMap**`**?**
    
    - In a `HashMap`, if a duplicate key is inserted, the old value associated with that key will be replaced by the new value.
        
9. **What is the difference between** `**Stack**` **and** `**Queue**`**?**
    
    - `Stack` is based on the LIFO (Last In First Out) principle, whereas `Queue` follows the FIFO (First In First Out) principle.
        
10. **How do you remove an element from a** `**Set**` **in Java?**
    
    - You can use the `remove(Object o)` method of the `Set` interface to remove a specific element. It returns `true` if the element was removed, and `false` if it was not present.