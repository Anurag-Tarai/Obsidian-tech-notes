### **1. Servlets**

- What are Servlets and their role in web applications.
- Servlet lifecycle (`init`, `service`, `destroy`).
- Handling HTTP requests (`GET`, `POST`) with `HttpServlet`.
- Session management techniques:
    - Cookies
    - URL Rewriting
    - HttpSession

---

### **2. JSP (JavaServer Pages)**

- Purpose of JSP and how it complements Servlets.
- JSP lifecycle (Translation, Compilation, Initialization, Execution, Cleanup).
- JSP directives (`<%@ page %>`, `<%@ include %>`, `<%@ taglib %>`).
- Scriptlets, Expressions, and Declarations.
- Using JSTL (JavaServer Pages Standard Tag Library).

---

### **3. JDBC (Java Database Connectivity)**

- Basics of connecting Java applications to databases.
- Key interfaces: `DriverManager`, `Connection`, `Statement`, `PreparedStatement`, `ResultSet`.
- Steps for database interaction:
    1. Load the driver.
    2. Establish a connection.
    3. Execute SQL queries.
    4. Process the result.
    5. Close the connection.
- Advantages of `PreparedStatement` over `Statement`.

---

### **4. Java Web Application Basics**

- Directory structure of a Java web application (`WEB-INF`, `web.xml`).
- Deployment of WAR (Web Application Archive) files in a server (e.g., Apache Tomcat).
- `web.xml` configuration and annotations for Servlets.

---

### **5. Core Concepts in Advanced Java**

- Filters in Servlets (e.g., Authentication filters).
- Listeners in Java EE (e.g., `HttpSessionListener`, `ServletContextListener`).
- Forwarding and redirecting requests (`RequestDispatcher` vs `sendRedirect`).

---

### **6. RESTful Web Services Basics**

- What is REST and its principles.
- Differences between REST and SOAP.
- Basics of using Java to create REST APIs (using `JAX-RS` or Spring Boot).
- Understanding HTTP methods (`GET`, `POST`, `PUT`, `DELETE`).

---

### **7. Annotations**

- Common annotations used in Java EE:
    - `@WebServlet`
    - `@WebFilter`
    - `@Path` (for REST endpoints)

---

### **8. Threads in Web Applications**

- Basics of thread safety in Servlets and JSP.
- Handling multi-threading issues in web applications.

---

### **9. Build Tools**

- **Maven:**
    - Managing dependencies.
    - Writing a simple `pom.xml`.
    - Maven build lifecycle (clean, compile, package).
- **Gradle (Optional):**
    - Basics of task management.

---

### **10. Deployment Basics**

- What is a Web/Application Server (e.g., Tomcat, GlassFish).
- Deployment of WAR files in Tomcat.
- Configuring server ports and context paths.

---

### **11. Basic Security**

- Securing Servlets and JSP with basic authentication.
- SQL injection prevention using `PreparedStatement`.
- Introduction to HTTPS and SSL certificates.

---

### **12. Popular Frameworks Overview (Optional)**

- **Spring Basics**:
    - Dependency Injection
    - Introduction to Spring Boot
- **Hibernate Basics**:
    - Object-Relational Mapping (ORM)
    - Mapping an entity to a table using annotations.