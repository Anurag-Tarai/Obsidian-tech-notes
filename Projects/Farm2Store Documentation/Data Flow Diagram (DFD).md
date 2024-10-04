### **Data Flow Diagram (DFD) Level 0**
```java
+-----------------------------------+
|          Farmer-to-Store          |
|          Web Application          |
+-----------------------------------+
             |   ^
             |   |
             v   |
+-----------------------+             +----------------------+
|       Farmer          |             |    Store Owner       |
|                       |             |                      |
| 1. Register/Login     | -------->   | 1. Register/Login    |
| 2. Post Products      |             | 2. Search Products   |
| 3. View Orders        |             | 3. Buy Products      |
|                       |             | 3. Search Product    |
+-----------------------+             +----------------------+
             |                                
             |                                
             v                                
+-----------------------------------+    
|             Database              |   
|                                   |    
|  - Farmer Details                 |   
|  - Store Owner Details            |                  
|  - Product Listings               |                                   
|  - Orders                         |                                   
|                                   |    
+-----------------------------------+   

```
### **Data Flow Diagram (DFD) Level 1**

#### **Farmer Process**
```java
				+---------------------------------------+
				|                Farmer                 |
				+---------------------------------------+
				| 1. Register/Login                     |
				|    - Input: Name, Email, Phone,      |
				|      Location                         |
				|    - Output: Success/Failure Message  |
				|                                       |
				| 2. Post Products                      |
				|    - Input: Product Details           |
				|    - Output: Confirmation Message     |
				|                                       |
				| 3. View Orders                        |
				|    - Input: FarmerID                  |
				|    - Output: List of Orders           |
				+---------------------------------------+
				             |
				             v
				+---------------------------------------+
				|               Database                |
				|                                       |
				| - Store Farmer Details                |
				| - Store Product Listings              |
				| - Store Orders                        |
				+---------------------------------------+

```

Store Owner Process
```java
				+---------------------------------------+
				|             Store Owner              |
				+---------------------------------------+
				| 1. Register/Login                     |
				|    - Input: Name, Email, Phone,      |
				|      Location                         |
				|    - Output: Success/Failure Message  |
				|                                       |
				| 2. Search Products                    |
				|    - Input: Search Criteria           |
				|    - Output: List of Products         |
				|                                       |
				| 3. Buy Products                      |
				|    - Input: Order Details             |
				|    - Output: Order Confirmation       |
				+---------------------------------------+
				             |
				             v
				+---------------------------------------+
				|               Database                |
				|                                       |
				| - Store Store Owner Details           |
				| - Store Product Listings              |
				| - Store Orders                        |
				+---------------------------------------+

```