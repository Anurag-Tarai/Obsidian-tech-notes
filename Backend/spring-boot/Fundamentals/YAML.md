##### class path 
- Locations where the Java runtime (JVM) and your application will look for classes, libraries, and resources at runtime and compile-time.
# YAML
- YAML Ain't Markup Language.
- YAML uses **indentation** to define structure and hierarchy.
### application.properties Vs yaml
```java
//application.properties
spring.application.name=JournalAppPractice  
spring.devtools.restart.enabled=true  
spring.data.mongodb.auto-index-creation = true  
spring.data.mongodb.uri=mongodb+srv://sdflkjsldf:6MzvqqxfWqX9UFdJ@cluster0.lt8gotz.mongodb.net/journal_db?retryWrites=true&w=majority


// application.yaml
spring:  
  devtools:  
    restart:  
      enabled: true  
  application:  
    name: JournalAppPractice  
  data:  
    mongodb:  
      uri: mongodb+srv://sdflkjsldf:6MzvqqxfWqX9UFdJ@cluster0.lt8gotz.mongodb.net/journal_db?retryWrites=true&w=majority  
      auto-index-creation: true  
server:  
  port: 8081
```

## How to pass command line arguments in spring boot application ?
```java
./mvnw clean
./mvnw package
JournalApplication/target$ java -jar JournalAppPractice-0.0.1-SNAPSHOT.jar

```