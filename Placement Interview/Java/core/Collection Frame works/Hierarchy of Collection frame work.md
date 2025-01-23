```mathematica
            Iterable
               |
          Collection
         /    |     \
       List  Set   Queue
       |      |      |
  ArrayList HashSet PriorityQueue
 LinkedList TreeSet ArrayDeque
    Stack LinkedHashSet
        \
       Map
     /   |   \
 HashMap TreeMap LinkedHashMap

```
### 1. **Core Interfaces**

The Collection Framework provides several core interfaces that define the essential types of collections:

#### a. **Collection Interface**

- It is the root interface of the Collection Framework and is extended by other sub-interfaces like `List`, `Set`, and `Queue`. It provides basic methods like `add()`, `remove()`, `size()`, and `iterator()`.

#### b. **List Interface** (extends `Collection`)

- A `List` is an ordered collection (sequence) that allows duplicate elements. It provides positional access and insertion of elements.
    - **Implementations**:
        - `ArrayList`: Resizable array implementation of `List`.
        - `LinkedList`: Doubly linked list implementation.
        - `Vector`: Synchronized `ArrayList`.
        - `Stack`: Extends `Vector` to provide a LIFO stack.

#### c. **Set Interface** (extends `Collection`)

- A `Set` is a collection that does not allow duplicates. It is used when uniqueness is required.
    - **Implementations**:
        - `HashSet`: Hash table-based implementation; no order maintained.
        - `LinkedHashSet`: Hash table-based, maintains insertion order.
        - `TreeSet`: Tree-based, elements are sorted in natural order or via a comparator.

#### d. **Queue Interface** (extends `Collection`)

- A `Queue` is used to hold elements before processing and typically follows a FIFO (First In First Out) order, though some queues like `PriorityQueue` can follow different orders.
    - **Implementations**:
        - `PriorityQueue`: Orders elements based on their priority or a comparator.
        - `Deque`: Double-ended queue; allows insertion and removal from both ends.
        - `ArrayDeque`: Resizable array-based implementation of `Deque`.

#### e. **Map Interface**

- A `Map` is not part of the `Collection` interface but is an essential part of the Collection Framework. It represents a key-value pair mapping and does not allow duplicate keys.
    - **Implementations**:
        - `HashMap`: Hash table-based; no order maintained.
        - `LinkedHashMap`: Hash table-based; maintains insertion order.
        - `TreeMap`: Sorted map implementation.
        - `Hashtable`: Synchronized `HashMap`.

#### f. **SortedSet Interface** (extends `Set`)

- A `SortedSet` is a specialized `Set` that maintains elements in ascending order.
    - **Implementation**:
        - `TreeSet`: Implements `SortedSet`.

#### g. **SortedMap Interface** (extends `Map`)

- A `SortedMap` is a `Map` that maintains its mappings in ascending key order.
    - **Implementation**:
        - `TreeMap`: Implements `SortedMap`.

### 2. **Iterators**

- **Iterator Interface**: Provides methods to traverse a collection (like `hasNext()`, `next()`, and `remove()`).
- **ListIterator Interface**: Extends `Iterator` and allows bidirectional traversal of lists.

### 3. **Utility Classes**

- **Collections**: Provides static methods to perform common operations like sorting, searching, and shuffling.
- **Arrays**: Provides utility methods for array operations, such as sorting and converting arrays to `List`.