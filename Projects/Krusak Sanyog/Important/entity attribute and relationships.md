### **Entities and Their Attributes:**

1. **User**:
    
    - **Attributes**:
        - `id`
        - `first_name`
        - `middle_name`
        - `last_name`
        - `email_id`
        - `pan_no`
        - `adhar_no`
        - `password`
        - `profile_status`
        - `registered_date`
    - **Relationships**:
        - Is a `Farmer` or `Buyer` (1:1)
2. **Farmer**:
    
    - **Attributes**:
        - `id`
        - `farm_location`
        - `farm_size`
        - `crops_type`
        - `is_verified`
        - `rating`
        - `harvest_date`
    - **Relationships**:
        - Can add `Products` (1:M with Product)
        - Has a `Reach Out Farmer` (M:M with Buyer)
3. **Product**:
    
    - **Attributes**:
        - `id`
        - `product_name`
        - `description`
        - `category`
        - `availability_status`
        - `quantity_available`
    - **Relationships**:
        - Belongs to a `Farmer` (M:1 with Farmer)
        - Has `Address` (1:1 with Address)
        - Can be in `Cart` (M:M with Cart)
        - Associated with `Chat` (1:M with Chat)
4. **Address**:
    
    - **Attributes**:
        - `id`
        - `street`
        - `village`
        - `postalCode`
        - `latitude`
        - `longitude`
    - **Relationships**:
        - Belongs to a `Product` (1:1 with Product)
5. **Buyer**:
    
    - **Attributes**:
        - `id`
        - `contact_number`
    - **Relationships**:
        - Has `Cart` (1:M with Cart)
        - Can `Reach Out Farmer` (M:M with Farmer)
        - Associated with `ContactDetails` (1:1 with ContactDetails)
6. **Cart**:
    
    - **Attributes**:
        - `id`
        - `item`
        - `item_count`
        - `price`
    - **Relationships**:
        - Belongs to a `Buyer` (M:1 with Buyer)
        - Contains `Product` (M:1 with Product)
7. **Chat**:
    
    - **Attributes**:
        - `id`
        - `messages`
    - **Relationships**:
        - Belongs to `Product` (1:M with Product)
        - Belongs to `Farmer` (M:1 with Farmer)
        - Belongs to `Buyer` (M:1 with Buyer)
8. **ContactDetails**:
    
    - **Attributes**:
        - `id`
        - `email`
        - `phone_number`
    - **Relationships**:
        - Belongs to `Farmer` (M:1 with Farmer)
9. **Admin**:
    
    - **Attributes**:
        - `id`
        - `admin_level`
        - `permissions`
        - `activity_logs`
    - **Relationships**:
        - Monitors `User` (1:M with User)

### **Relationships Between Entities:**

1. **User**:
    
    - A `User` can be either a `Farmer` or a `Buyer` (1:1 relationship with either).
2. **Farmer**:
    
    - A `Farmer` can have multiple `Products` (1:M relationship with Product).
    - A `Farmer` can have multiple `Buyers` reaching out to them (M:M relationship with Buyer via `Reach Out Farmer`).
3. **Product**:
    
    - A `Product` is created by a `Farmer` (M:1 with Farmer).
    - A `Product` can be stored in a `Cart` (M:M relationship with Cart).
    - A `Product` can have multiple `Chat` messages (1:M relationship with Chat).
    - A `Product` has a single `Address` (1:1 relationship with Address).
4. **Cart**:
    
    - A `Cart` belongs to a `Buyer` (M:1 with Buyer).
    - A `Cart` can contain multiple `Products` (M:1 relationship with Product).
5. **Chat**:
    
    - A `Chat` is associated with both a `Product` (1:M relationship) and a `Buyer` (M:1 relationship), and also with a `Farmer` (M:1 relationship).
6. **Buyer**:
    
    - A `Buyer` can have multiple items in a `Cart` (1:M relationship with Cart).
    - A `Buyer` can reach out to multiple `Farmers` (M:M relationship via `Reach Out Farmer`).
    - A `Buyer` has associated `ContactDetails` (1:1 relationship with ContactDetails).
7. **ContactDetails**:
    
    - `ContactDetails` stores contact information for a `Farmer` (M:1 relationship).
8. **Admin**:
    
    - An `Admin` has permission to monitor `User` activity (1:M relationship with User).