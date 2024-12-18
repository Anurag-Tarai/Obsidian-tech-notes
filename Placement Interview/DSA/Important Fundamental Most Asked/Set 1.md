### 1. Write a code to reverse a number
```java
//Loop
    int sum = 0 
    while(n>0){
        sum = sum*10 + n%10;
        n/=10;
    }
    System.out.println(sum);

// Recursion
  public static int reverse(int n, int sum){
      if(n<=0) return sum;
      sum = sum*10 + n%10;
      return reverse(n/10, sum);
  }
```

### 2. Write the code to find the Fibonacci series upto the nth term.
```java

//to find nth term
// Loop
	int n = 7;
    int pre1 = 1;
    int pre2 = 0; 
    int ans = 0;
    
    if(n==1) ans = 0;
    else if(n==2) ans = 1;
    else {
        while(n>2){
        ans = pre1 + pre2;
        pre2 = pre1;
        pre1 = ans;
         n--;
     }
    }
    System.out.println(ans);

// Recursion 
      static int f(int n){
      if(n==1) return 0;
      if(n==2) return 1;
      return f(n-1)+f(n-2);
  }
  
  
// Whole series 
    int pre2 = 0;
    int pre1 = 1; 
    int n = 7;

    int ans = 0;
    
    System.out.print(pre2+" "+pre1+" ");
        while(n>2){
        ans = pre1 + pre2;
        System.out.print(ans +" ");
        pre2 = pre1;
        pre1 = ans;
         n--;
    }
```

### 3. Write code of Greatest Common Divisor
GCD - Greatest common factor : Greatest number that divide both the number
- **Using Division Method:**
    
    - Divide the larger number by the smaller number.
    - Take the remainder.
    - Replace the larger number with the smaller number and the smaller number with the remainder.
    - Repeat until the remainder is zero. The last non-zero remainder is the GCD.
- **Using Prime Factorization:**
    
    - Find the prime factorization of both numbers.
    - Identify common factors and multiply them.
LCM - Least common Multiplier : The smallest positive number that is divisible by both numbers.
1. **Using the Formula:**
    
    - LCM=Product of the numbersGCD\text{LCM} = \frac{\text{Product of the numbers}}{\text{GCD}}LCM=GCDProduct of the numbers​
2. **Using Listing Multiples:**
    
    - List the multiples of both numbers.
    - Identify the smallest common multiple.

```java
// Brute Force
    for(int i=2; i<=Math.min(a,b); i++){
        if(a%i==0 && b%i==0) gcd  = i;
    }
// GCD // Euclidean’s theorem
    public static int gcd(int a, int b) {
        if(a%b==0) return b;
        return gcd(b, a%b);
    }
// LCM
    lcm = (a * b) / gcd;
```

### 4. Write code of  Perfect number
A **perfect number** is a positive integer that is equal to the sum of its proper divisors, excluding the number itself.

For example:

- **6** is a perfect number because its proper divisors are **1, 2, and 3**, and **1 + 2 + 3 = 6**.
- **28** is another example because its proper divisors are **1, 2, 4, 7, 14**, and **1 + 2 + 4 + 7 + 14 = 28**.

```java
static boolean perfect(int a){
    int sum = 0;
    for(int i=1; i<=a/2; i++){
      if(a%i==0) sum = sum+i;
    }
    if(sum == a) return true;
    return false;
  }
  
  
// Recursion
static boolean perf(int a, int sum, int i){
    if(i>a/2){
      return sum==a;
    }
    return perf(a, a%i==0? sum+i: sum , i+1);
  }
```
### 5. Write code to Check if two strings are Anagram or not
An **anagram** is a word or phrase formed by rearranging the letters of another word or phrase, using all the original letters exactly once. For example:

- **"listen"** is an anagram of **"silent"**.
- **"evil"** is an anagram of **"vile"**.
```java
// Using String Builder

// Intitution : iterate each char of 2nd string and remove that char if appear in first and remove, in the end the first string should be empty and both string size should same

	  String s1 = "silent";
      String s2 = "listent";
      
      StringBuilder str = new StringBuilder(s1);
      
      for(char c: s2.toCharArray()){
        int i = str.indexOf(""+c); // String builder index of check first occurrence of string
        if(i!=-1) str.deleteCharAt(i);
      }
      if(str.length()!=0 || s1.length()!=s2.length()) System.out.println("not ana");
      else System.out.println("ana");


// Using Hash map of array
	  String s1 = "silent";
      String s2 = "listent";
      
      boolean isAna = true;
      
      int [] map1 = new int[26];
      int [] map2 = new int[26];
      
      for(int c: s1.toCharArray()){
        map1[c-'a']++;
      }
      for(int c: s2.toCharArray()){
        map2[c-'a']++;
      }
      
      for(int i=0; i<26; i++){
        if(map1[i]!=map2[i]) isAna = false ; 
        break;
      } 
      if(isAna && s1.length()==s2.length()) System.out.println("ana");
      else System.out.println("Not ana");
  

```
```java
// using HashMap<>
String s1 = "silent";
        String s2 = "listen";

        if (s1.length() != s2.length()) {
            System.out.println("not ana");
            return;
        }
        Map<Character, Integer> map = new HashMap<>();
        for (char c : s1.toCharArray()) map.put(c, map.getOrDefault(c, 0) + 1);
        for (char c : s2.toCharArray()) map.put(c, map.getOrDefault(c, 0) - 1);

        for (int v : map.values()) {
            if (v != 0) {
                System.out.println("not ana");
                return;
            }
        }
        System.out.println("is ana");
```
