# JUnit - Java Unit
- Testing framework for java
###### Testing 
	1.Unit testing 
	1.Integration testing

### Dependencies
```java
<dependency>  
    <groupId>org.springframework.boot</groupId>  
    <artifactId>spring-boot-starter-test</artifactId>  
    <scope>test</scope>  
</dependency>

// inside this you will ger JUnit as below
<dependency>  
  <groupId>org.junit.jupiter</groupId>  
  <artifactId>junit-jupiter</artifactId>  
  <version>5.10.2</version>  
  <scope>compile</scope>  
</dependency>
```
This is only for testing remove in the production.

## Use
To test different components during development of API's.
- this is known as `Test driven development`

##### Example
```java
package com.anurag.journalapp.serviceTests;  
  
import com.anurag.journalapp.repository.UserRepository;  
import org.junit.jupiter.api.Test;  
import static org.junit.jupiter.api.Assertions.assertEquals;  
import static org.junit.jupiter.api.Assertions.assertNotNull;  
  
import org.springframework.beans.factory.annotation.Autowired;  
import org.springframework.boot.test.context.SpringBootTest;  
  
@SpringBootTest // to start application context  
public class UserServiceTests {  
  
    @Autowired  
    private UserRepository userRepository;  
    @Test  
    public void findByUserNameTest(){  
        assertEquals(2, 1+1);  
        assertNotNull(userRepository.findByUserName("sujit"));  
    }  
}
```
##### Parameterized Test
```java
@ParameterizedTest  
@ValueSource(strings={  
        "anurag",  
        "sujit",  
        "admin"  
})  
public void findByUserNameTest(String name){  
    assertNotNull(userRepository.findByUserName(name));  
}

@ParameterizedTest  
@CsvSource({  
        "1,2,3",  
        "4,2,6",  
        "5,6,3"  
})  
public void test(int a, int b, int expected){  
    assertEquals(expected, a+b);  
}
```