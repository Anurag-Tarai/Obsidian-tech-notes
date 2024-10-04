```java
			+-----------------+        +-------------------+
			|     Farmer      |        |    Store Owner    |
			+-----------------+        +-------------------+
			| FarmerID (PK)   |        | StoreOwnerID (PK) |
			| Name            |        | Name              |
			| Email           |        | Email             |
			| Phone           |        | Phone             |
			| Location        |        | Location          |
			+-----------------+        +-------------------+
			         |                         |
			         | 1                       | 1
			         |                         |
			         |                         |
			         | *                       | *
			+-----------------+        +-------------------+
			|    Product      |        |      Order        |
			+-----------------+        +-------------------+
			| ProductID (PK)  |        | OrderID (PK)      |
			| Name            |        | ProductID (FK)    |
			| Description     |        | StoreOwnerID (FK) |
			| Price           |        | Quantity          |
			| Quantity        |        | OrderDate         |
			| FarmerID (FK)   |        +-------------------+
			+-----------------+

```
### **Entities Explained**

1. **Farmer**
    - **FarmerID (PK)**: Unique identifier for each farmer.
    - **Name**: Name of the farmer.
    - **Email**: Contact email.
    - **Phone**: Contact number.
    - **Location**: Location of the farmer.
    
1. **Store Owner**
    - **StoreOwnerID (PK)**: Unique identifier for each store owner.
    - **Name**: Name of the store owner.
    - **Email**: Contact email.
    - **Phone**: Contact number.
    - **Location**: Location of the store owner.
    
1. **Product**
    - **ProductID (PK)**: Unique identifier for each product.
    - **Name**: Name of the product.
    - **Description**: Description of the product.
    - **Price**: Selling price of the product.
    - **Quantity**: Available quantity of the product.
    - **FarmerID (FK)**: Foreign key referencing the Farmer entity.
    
1. **Order**
    - **OrderID (PK)**: Unique identifier for each order.
    - **ProductID (FK)**: Foreign key referencing the Product entity.
    - **StoreOwnerID (FK)**: Foreign key referencing the Store Owner entity.
    - **Quantity**: Quantity of the product ordered.
    - **Order_Date**: Date the order was placed.

### **Relationships**

- A **Farmer** can have multiple **Products** (1 to many).
- A **Store Owner** can place multiple **Orders** (1 to many).
- An **Order** is associated with one **Product** and one **Store Owner** (many to 1 for both).