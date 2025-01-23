1. **User**:
    
    - `id`
    - `name` (attributes: `first_name`, `middle_name`, `last_name`)
    - `email_id`
    - `pan_no`
    - `adhar_no`
    - `registered_date`
    - `password`
    - `profile_status`
2. **Admin** (separate entity, not related to **User**):
    
    - `admin_id`
    - `admin_level`
    - `permissions`
    - `activity_logs`
    - `address`
    - **Monitors** user activities (one-to-many relationship with users)
3. **Farmer** (extends **User**):
    
    - `farmer_id` (foreign key from User)
    - `farm_location`
    - `crops_types`
    - `farm_size`
    - `harvest_date`
    - `rating`
    - `is_verified`
    - **Adds** products (one-to-many relationship with products)
4. **Buyer** (extends **User**):
    
    - `buyer_id` (foreign key from User)
    - `contact_number`
    - **Has** a **Cart** (one-to-many relationship with products)
5. **Product**:
    
    - `product_id`
    - `farmer_id` (foreign key to Farmer)
    - `product_name`
    - `category`
    - `description`
    - `product_type`
    - `available_types`
    - `availability_status`
    - `quantity_available`
6. **Address**:
    
    - `address_id`
    - `farmer_id` (foreign key to Farmer)
    - `street`
    - `city`
    - `village`
    - `postalCode`
    - `country`
    - `geolocation` (`latitude`, `longitude`)
7. **ContactDetails**:
    
    - `contact_id`
    - `farmer_id` (foreign key to Farmer)
    - `email`
    - `phone_number`
8. **Cart**:
    
    - `cart_id`
    - `buyer_id` (foreign key to Buyer)
    - `products` (relation to Product)
    - `item_count`
9. **Chat**:
    
    - `chat_id`
    - `farmer_id` (foreign key to Farmer)
    - `buyer_id` (foreign key to Buyer)
10. **Message**:
    
    - `message_id`
    - `chat_id` (foreign key to Chat)
    - `sender_id`
    - `product_id` (foreign key to Product)
    - `content`
    - `timestamp`
11. **Review**:
    
    - `review_id`
    - `buyer_id` (foreign key to Buyer)
    - `farmer_id` (foreign key to Farmer)
    - `rating`
    - `comment`
    - `timestamp`

### Updated Relationships:

1. **Admin**:
    - **Monitors** users' activities (one-to-many with **User**, **Farmer**, and **Buyer** entities).
2. **User**:
    - **User** entity is generalized and relates to **Farmer** and **Buyer** through "is a" relationships.
3. **Buyer**:
    - Can **search** for farmers or products.
    - **Has** a **Cart** (one-to-many relationship with products).
    - Can **reach out** to farmers via **Chat**.
4. **Farmer**:
    - **Adds** products (one-to-many relationship with **Product**).
    - Has **ContactDetails** (one-to-many relationship).
    - Has **Address** (one-to-one relationship).
5. **Product**:
    - Is linked to **Farmer**.
    - Can be added to **Cart** by **Buyer**.
    - Can be discussed in **Chat** with **Buyer**.
6. **Chat**:
    - Occurs between a **Farmer** and **Buyer**.
    - Contains multiple **Messages** (one-to-many).
7. **Review**:
    - **Buyer** can **give** a **Review** to **Farmer**.
    - Includes **rating** and **comment**.