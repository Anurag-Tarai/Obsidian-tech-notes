```java
Scanner sc = new Scanner(System.in);

int n = sc.nextInt();
int s = sc.nextLine(); // it will take " " because empty string left by input of nextInt() is consumed by this 

// solution
int n = sc.nextInt();
sc.nextLine(); // it will consume the empty string
int s = sc.nextLine(); 
```