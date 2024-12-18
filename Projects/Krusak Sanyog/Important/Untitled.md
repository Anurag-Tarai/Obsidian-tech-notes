Here are the recommended SQL data types for the entities and their attributes in lowercase:

### **Entities and Attributes with Recommended SQL Data Types:**

1. **user**:
    
    - `id`: **int** (primary key)
    - `first_name`, `middle_name`, `last_name`: **varchar(255)**
    - `email_id`: **varchar(255)**
    - `pan_no`: **char(10)** (assuming pan is a fixed-length alphanumeric code)
    - `adhar_no`: **char(12)** (fixed length for aadhaar number)
    - `password`: **varchar(255)** (to store hashed passwords)
    - `profile_status`: **varchar(50)**
    - `registered_date`: **datetime** (for date and time of registration)
2. **farmer**:
    
    - `id`: **int** (primary key, foreign key to user)
    - `farm_location`: **varchar(255)**
    - `farm_size`: **decimal(10,2)** (for area, to store numerical values with decimals)
    - `crops_type`: **varchar(255)**
    - `is_verified`: **boolean** (true/false)
    - `rating`: **decimal(3,2)** (for average rating, range 0-10)
    - `harvest_date`: **date** (for harvest date)
3. **product**:
    
    - `id`: **int** (primary key)
    - `product_name`: **varchar(255)**
    - `description`: **text** (for product description)
    - `category`: **varchar(100)**
    - `availability_status`: **varchar(50)**
    - `quantity_available`: **int** (quantity of product available)
4. **address**:
    
    - `id`: **int** (primary key)
    - `street`: **varchar(255)**
    - `village`: **varchar(100)**
    - `postalCode`: **char(6)** (assuming postal code length in india)
    - `latitude`: **decimal(9,6)** (for geographic coordinates)
    - `longitude`: **decimal(9,6)** (for geographic coordinates)
5. **buyer**:
    
    - `id`: **int** (primary key, foreign key to user)
    - `contact_number`: **varchar(15)** (for phone number with country code)
6. **cart**:
    
    - `id`: **int** (primary key)
    - `item`: **varchar(255)**
    - `item_count`: **int**
    - `price`: **decimal(10,2)** (price of the item)
7. **chat**:
    
    - `id`: **int** (primary key)
    - `messages`: **text** (for chat messages)
8. **contactdetails**:
    
    - `id`: **int** (primary key)
    - `email`: **varchar(255)**
    - `phone_number`: **varchar(15)**
9. **admin**:
    
    - `id`: **int** (primary key, foreign key to user)
    - `admin_level`: **varchar(50)**
    - `permissions`: **varchar(255)**
    - `activity_logs`: **text** (for storing logs)

---

### **Relationship Tables:**

1. **farmer_buyer (m:m)** (for `reach out farmer`):
    
    - `farmer_id`: **int** (foreign key to farmer)
    - `buyer_id`: **int** (foreign key to buyer)
2. **product_cart (m:m)** (for storing products in cart):
    
    - `product_id`: **int** (foreign key to product)
    - `cart_id`: **int** (foreign key to cart)
3. **product_chat (1:m)** (for chat associated with product):
    
    - `product_id`: **int** (foreign key to product)
    - `chat_id`: **int** (foreign key to chat)
4. **buyer_contactdetails (1:1)**:
    
    - `buyer_id`: **int** (foreign key to buyer)
    - `contact_id`: **int** (foreign key to contactdetails)
5. **admin_user (1:m)** (for admin monitoring user activities):
    
    - `admin_id`: **int** (foreign key to admin)
    - `user_id`: **int** (foreign key to user)