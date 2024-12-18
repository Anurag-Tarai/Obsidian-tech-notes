### **Challenge 1: RESTful CRUD with React and Spring Boot**

**Task:**  
Build a basic **Task Manager** application.

1. Create a Spring Boot backend with endpoints for creating, reading, updating, and deleting tasks.
    - Each task should have a title, description, and status (Pending/Completed).
2. Use React to create a simple frontend with the following:
    - A form to add new tasks.
    - A table to display tasks.
    - Buttons to edit or delete tasks.

**Bonus:**

- Implement filtering tasks by their status.

---

### **Challenge 2: Authentication System**

**Task:**  
Implement a basic **JWT Authentication System**.

1. Backend:
    - Create endpoints for user registration and login.
    - Secure an endpoint (`/dashboard`) to return "Welcome to Dashboard" only for authenticated users.
2. Frontend:
    - Create a simple login page.
    - Store and use the JWT token to access the `/dashboard` endpoint.

**Bonus:**

- Show an error message if the login fails.

---

### **Challenge 3: Real-Time Chat**

**Task:**  
Develop a basic **Chat Application** with mock users.

1. Backend:
    - Use Spring Boot with WebSocket to handle real-time chat messages.
2. Frontend:
    - Create a chat interface in React.
    - Display messages in real-time.

**Bonus:**

- Add a dropdown to select a user and display user-specific chat threads.

---

### **Challenge 4: File Upload System**

**Task:**  
Create a **File Upload System**.

1. Backend:
    - Create an endpoint to upload files and store them in the local file system or an in-memory database.
    - Return the file URL in the response.
2. Frontend:
    - Build a React form to upload files.
    - Show the uploaded file's name and provide a link to download it.

**Bonus:**

- Add a file type and size validation on the frontend.

---

### **Challenge 5: E-Commerce Cart System**

**Task:**  
Create a basic **E-Commerce Cart System**.

1. Backend:
    - Add endpoints to add/remove products and fetch all products in the cart.
2. Frontend:
    - Display a list of products fetched from a mock API.
    - Allow users to add/remove products from their cart.

**Bonus:**

- Display the total price of items in the cart.

---

### **Challenge 6: Auction System**

**Task:**  
Build a simple **Auction Feature**.

1. Backend:
    - Add an endpoint to create an auction with a product, starting price, and end time.
    - Another endpoint to place bids.
2. Frontend:
    - Create a form to create auctions.
    - Display active auctions and allow users to place bids.

**Bonus:**

- Display the current highest bid.

---

### **Challenge 7: Dashboard with Charts**

**Task:**  
Build a **Dashboard** displaying statistics.

1. Backend:
    - Create an endpoint to return mock statistics data (e.g., user count, product count, sales).
2. Frontend:
    - Use a chart library (like Chart.js or Recharts) to visualize the statistics.

**Bonus:**

- Add live updates to the statistics every 10 seconds.