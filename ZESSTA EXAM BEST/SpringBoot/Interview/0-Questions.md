### **1. Basics of Spring and Spring Boot**

1. What is Spring Boot, and how is it different from the Spring Framework?
2. What are the main advantages of using Spring Boot?
3. What are starters in Spring Boot? Name a few commonly used starters.
4. Explain the concept of auto-configuration in Spring Boot.
5. What is the role of the `@SpringBootApplication` annotation?
6. How do you create a Spring Boot application from scratch?

---

### **2. Dependency Injection and Annotations**

1. What is dependency injection in Spring Boot?
2. What is the difference between `@Component`, `@Service`, `@Repository`, and `@Controller`?
3. What is the use of `@Autowired`, and how does it work in Spring Boot?
4. What is the difference between field injection, setter injection, and constructor injection?
5. What is `@Qualifier`, and when do you use it?

---

### **3. Configuration and Properties**

1. How do you externalize configuration in Spring Boot?
2. What is the purpose of the `application.properties` or `application.yml` file?
3. How do you access application properties in a Spring Boot application?
4. What is the difference between `@Value` and `@ConfigurationProperties`?
5. How do you profile-specific configurations in Spring Boot?

---

### **4. REST APIs and Controllers**

1. How do you create a REST API in Spring Boot?
2. What is the difference between `@RestController` and `@Controller`?
3. Explain the role of `@RequestMapping`, `@GetMapping`, `@PostMapping`, etc.
4. What are `@PathVariable` and `@RequestParam`, and how do they differ?
5. How do you handle exceptions in a Spring Boot REST API?

---

### **5. Data Access with Spring Boot**

1. What is Spring Data JPA, and how is it used in Spring Boot?
2. How do you configure a database connection in Spring Boot?
3. What is the difference between `JpaRepository` and `CrudRepository`?
4. Explain the purpose of the `@Entity`, `@Id`, and `@Table` annotations.
5. What is the role of `@Transactional` in Spring Boot?
6. How do you write custom queries using Spring Data JPA?

---

### **6. Security**

1. What is Spring Security, and how do you implement it in a Spring Boot application?
2. What is the difference between Basic Authentication and JWT in Spring Boot?
3. How do you secure REST APIs in Spring Boot?
4. What is the role of `@EnableWebSecurity`?
5. How do you implement role-based authorization in Spring Boot?

---

### **7. Testing in Spring Boot**

1. What are the testing features provided by Spring Boot?
2. How do you test a Spring Boot application using JUnit and Mockito?
3. What is the purpose of `@SpringBootTest`?
4. What is the use of `MockMvc` in testing REST APIs?
5. How do you test a Spring Data JPA repository?

---

### **8. Actuator and Monitoring**

1. What is Spring Boot Actuator, and why is it used?
2. How do you enable and customize actuator endpoints?
3. How do you secure Spring Boot Actuator endpoints?
4. Explain the `/health` and `/metrics` endpoints provided by Spring Boot Actuator.

---

### **9. Spring Boot DevTools**

1. What is Spring Boot DevTools, and how does it enhance development productivity?
2. How do you enable and configure Spring Boot DevTools?

---

### **10. Logging**

1. How do you implement logging in Spring Boot?
2. What is the default logging framework in Spring Boot?
3. How do you change the logging level for a specific package in Spring Boot?

---

### **11. Deployment**

1. How do you package a Spring Boot application into a JAR or WAR file?
2. How do you deploy a Spring Boot application to a server like Tomcat?
3. What is the purpose of the `application.properties` in a production environment?

---

### **12. Advanced Concepts**

1. What are Spring Boot filters, and how do you implement them?
2. Explain the role of `@Async` and asynchronous processing in Spring Boot.
3. What are interceptors in Spring Boot?
4. How do you configure CORS in Spring Boot?
5. What is the purpose of the `@EnableScheduling` annotation?

---

### **13. Messaging and Events**

1. How do you implement event handling in Spring Boot using `ApplicationEvent`?
2. What is Spring Boot's support for messaging platforms like RabbitMQ and Kafka?
3. How do you send and receive messages using Spring Boot?

---

### **14. Microservices with Spring Boot**

1. How do you build microservices using Spring Boot?
2. What is Spring Cloud, and how does it relate to Spring Boot?
3. How do you implement service discovery with Spring Boot (e.g., using Eureka)?
4. What is API Gateway, and how do you use it with Spring Boot?
5. How do you implement distributed tracing in a Spring Boot microservice?