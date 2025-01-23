- **List Interface**:
    
    - **`ArrayList`**: Resizable array implementation of the `List` interface. Allows random access and provides fast read operations but slower insertions and deletions.
    - **`LinkedList`**: Doubly linked list implementation of the `List` interface. Suitable for frequent insertions and deletions but provides slower access compared to `ArrayList`.
- **Set Interface**:
    
    - **`HashSet`**: Implements the `Set` interface and uses a hash table for storage. It does not allow duplicates and does not maintain order.
    - **`TreeSet`**: Implements the `Set` interface and stores elements in a sorted, ascending order (natural order or custom comparator).
    - **`LinkedHashSet`**: Maintains insertion order, unlike `HashSet`. It uses a linked list along with a hash table.
- **Map Interface**:
    
    - **`HashMap`**: Implements the `Map` interface. Stores key-value pairs, allows one null key, and multiple null values. Does not maintain any order.
    - **`TreeMap`**: Implements the `Map` interface and stores entries in sorted order based on keys.
    - **`LinkedHashMap`**: Extends `HashMap` but maintains insertion order.
- **Queue Interface**:
    
    - **`PriorityQueue`**: Implements the `Queue` interface and orders elements based on their natural order or a custom comparator.
    - **`Deque`**: Double-ended queue allowing insertion and removal of elements from both ends (supports `Queue` and `Stack` operations).
- **Iterators**:
    
    - **`Iterator`**: Used to traverse a collection in a forward direction. Allows removing elements during iteration.
    - **`ListIterator`**: Extends `Iterator` and allows bidirectional traversal, as well as element modification during iteration.
    - **`for-each` loop**: A simplified way to iterate over collections without the need for an explicit iterator.
- **Collections Utility Class**:
    
    - Provides static methods for sorting, searching, and manipulating collections. Includes methods like `sort()`, `binarySearch()`, `reverse()`, and `shuffle()`.