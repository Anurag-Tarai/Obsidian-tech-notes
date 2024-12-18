### 1. **Reusability**: Reuse existing code

- **Explanation**: Reusability means that once a class or module is created, it can be used again in different parts of the program or even in other projects. Instead of writing the same code repeatedly, you can simply reuse existing code, saving time and reducing redundancy.
- **Example**: If you have a `User` class that manages user data, you can reuse this class across multiple projects without rewriting the logic for managing users.
[[3. Constructors]]
### 2. **Modularity**: Code is divided into independent objects or classes, making it easier to manage, maintain, and scale.

- **Explanation**: Modularity refers to breaking down the system into smaller, self-contained units (objects or classes). Each module handles a specific functionality and can be developed, tested, and maintained independently. This separation makes it easier to manage the code, troubleshoot issues, and scale the application as new features are added.
- **Example**: In a shopping application, you can have separate classes for `Product`, `Cart`, `Order`, and `Payment`. Each class handles its own functionality and can be independently updated or extended.

### 3. **Scalability**: Adapt systems as needs grow.

- **Explanation**: Scalability is the ability of a system to handle increasing loads or to be easily expanded as requirements change over time. OOP makes it easier to add new features or accommodate growing demands without significantly affecting existing code. As new needs arise, new classes or modules can be added to support additional functionality.
- **Example**: If your application needs to support more user types (e.g., adding an "Admin" user in addition to regular users), you can extend existing classes or add new ones without changing the entire system.

### 4. **Maintainability**: Organize code for easy updates.

- **Explanation**: Maintainability refers to how easy it is to modify, update, or fix a system. OOP promotes maintainability by organizing code into classes and objects, each with a specific responsibility. Changes to one part of the system can be made independently of other parts, making it easier to track down issues, fix bugs, or update functionality without affecting the whole system.
- **Example**: If you need to change how user authentication works, you can modify the `Auth` class without affecting other parts of the system, such as the `Profile` class or `User` class. This isolated approach makes updates easier and less risky.