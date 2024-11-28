```js
const categories = [

{ name: "Vegetables", value: "vegetables" },

{ name: "Fruits", value: "fruits" },

{ name: "Dairy Products", value: "dairyProducts" },

{ name: "Herbs and Spices", value: "herbsAndSpices" },

];
```
**Create a class diagram for a Farmer-to-Store application. The system includes the following entities and relationships:**

1. **User**:  
    **Attributes**: id, firstName, middleName, lastName, email, password, phone, registeredDate, panNo, adharNo.  
    **Relationships**:
    
    - A User can act as a Farmer or Vendor (inheritance).
    - Admins verify Farmers and Vendors based on PAN and Aadhar.
2. **Admin**:  
    **Attributes**: id, adminLevel, permissions, activityLogs.  
    **Responsibilities**:
    
    - Verifies Farmers, Vendors, Products, and Current Harvests.
    - Manages auction configurations like the minimum bid increment.
3. **Farmer** (inherits from User):  
    **Attributes**: experienceLevel, farmLocation, farmSize, cropsType, address.  
    **Relationships**:
    
    - A Farmer can add multiple Products.
    - A Farmer can list multiple Auctions for their Products.
    - A Farmer reports Current Harvests.
4. **Vendor** (inherits from User):  
    **Attributes**: storeName, storeLocation, address, rating, operationHour.  
    **Relationships**:
    
    - A Vendor can bid on Auctions.
    - A Vendor can place Orders and manage a Cart.
5. **Product**:  
    **Attributes**: id, farmerId, productName, category, price, quantityAvailable, description, isVerified, expireDate.  
    **Relationships**:
    
    - Products are added by Farmers.
    - Products can be verified by Admins.
    - Products are included in Auctions.
6. **CurrentHarvest**:  
    **Attributes**: id, farmerId, quantity, availableDate, category, description, isVerified.  
    **Relationships**:
    
    - Linked to Farmers who report their harvests.
    - Verified by Admins.
7. **Auction**:  
    **Attributes**: id, farmerId, productId, startTime, endTime, startingPrice, minimumBidIncrement, highestBidderId, status.  
    **Relationships**:
    
    - A Farmer can create multiple Auctions for their Products.
    - Vendors place Bids on Auctions.
8. **Bid**:  
    **Attributes**: id, auctionId, vendorId, bidAmount, bidTime, isWinningBid, minimumBidIncrement.  
    **Relationships**:
    
    - Linked to Auctions.
    - Submitted by Vendors.
9. **Order**:  
    **Attributes**: id, vendorId, productId, orderDate, status.  
    **Relationships**:
    
    - Vendors place Orders for Products.
    - Orders are linked to a ShippingAddress.
10. **Cart**:  
    **Attributes**: id, vendorId, item, itemCount, price.  
    **Relationships**:
    
    - Vendors manage their Carts to prepare Orders.
11. **ShippingAddress**:  
    **Attributes**: id, addressLine, city, state, country, postalCode.  
    **Relationships**:
    
    - Linked to Orders for delivery information.