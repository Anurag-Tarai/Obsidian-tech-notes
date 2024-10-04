## After 50 Min -->

##### MySQL Dependencies : jpa and sql driver
and in application.properties add mySql driver class
```sql
#MySql driver class  
spring.jpa.hibernate.ddl-auto=update  
spring.datasource.url=jdbc:mysql://localhost:3306/crypto_trading  
spring.datasource.username=root  
spring.datasource.password=Root@123  
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

##### JWT dependencies : imp, api, jackson : used 0.11.5 because in 12 a lot deprecated what he used
`More Details`- [[3-JWT Auth]]
```xml
<dependency>  
    <groupId>io.jsonwebtoken</groupId>  
    <artifactId>jjwt-impl</artifactId>  
    <version>0.12.6</version>  
    <scope>runtime</scope>  
</dependency>  
<dependency>  
    <groupId>io.jsonwebtoken</groupId>  
    <artifactId>jjwt-jackson</artifactId>  
    <version>0.12.6</version>  
    <scope>runtime</scope>  
</dependency>  
<dependency>  
    <groupId>io.jsonwebtoken</groupId>  
    <artifactId>jjwt-api</artifactId>  
    <version>0.12.6</version>  
</dependency>
```
### Why does the default password stop appearing when a custom `UserDetailsService` is added?
###### Default Behavior
**Before Adding `CustomeUserDetailsService`**: Spring Boot creates a default user and prints the generated password in the console.
###### Custom Behavior
**After Adding `CustomeUserDetailsService`**: Spring Boot recognizes your custom authentication setup and **no longer creates a default user or prints a password**.
##### Additional Notes
 **No Need to Manually Disable the Default User**: You don't need to set properties in `application.properties` to disable the default user; providing a custom `UserDetailsService` is sufficient.
**Ensure Proper Security Configuration**: Make sure your security configuration (if any) aligns with your custom `UserDetailsService` to avoid any authentication issues.