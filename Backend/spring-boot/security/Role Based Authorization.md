`Engineering Digest` [Lecture 20](https://youtu.be/LndqWC4yIU4?si=DqyR1uob4N5tzzUf)

#### Assign role to users
```java
private List<String> roles;

// set role during signup and then save to data base
user.setRoles(List.of("USER"));
```

#### Role based Authorization
```java
/* this is the filter chain bean in config class. 
*/
.requestMatchers("/admin/**").hasRole("ADMIN")
```
