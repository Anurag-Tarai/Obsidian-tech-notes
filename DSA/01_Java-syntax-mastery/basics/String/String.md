1. **`length()`**  
    Returns the length of the string.
```java
String str = "Hello";
System.out.println(str.length()); // Output: 5
```

2. **`charAt(int index)`**  
    Returns the character at the specified index.
```java
String str = "Hello";
System.out.println(str.charAt(1)); // Output: e
```    

3. **`substring(int beginIndex, int endIndex)`**  
    Returns a substring from `beginIndex` to `endIndex` (exclusive).
```java
String str = "Hello";
System.out.println(str.substring(1, 4)); // Output: ell
```
    
4. **`equals(Object obj)`**  
    Compares two strings for equality.
```java
String str1 = "Hello";
String str2 = "Hello";
System.out.println(str1.equals(str2)); // Output: true
```
    
5. **`equalsIgnoreCase(String anotherString)`**  
    Compares two strings, ignoring case differences.
```java
String str1 = "Hello";
String str2 = "hello";
System.out.println(str1.equalsIgnoreCase(str2)); // Output: true
```
    
6. **`contains(CharSequence sequence)`**  
    Returns `true` if the string contains the specified sequence.
```java
String str = "Hello";
System.out.println(str.contains("ell")); // Output: true
```
    
7. **`indexOf(int ch)`**  
    Returns the index of the first occurrence of the specified character.
```java
String str = "Hello";
System.out.println(str.indexOf('l')); // Output: 2
```
    
8. **`replace(CharSequence target, CharSequence replacement)`**  
    Replaces all occurrences of the target sequence with the replacement sequence.
```java
String str = "Hello";
System.out.println(str.replace("l", "L")); // Output: HeLLo
```
    
9. **`toLowerCase()`**  
    Converts all characters of the string to lowercase.
```java
String str = "HELLO";
System.out.println(str.toLowerCase()); // Output: hello
```

10. **`toUpperCase()`**  
    Converts all characters of the string to uppercase.
```java
String str = "hello";
System.out.println(str.toUpperCase()); // Output: HELLO
```
    
11. **`trim()`**  
    Removes any leading and trailing whitespace.
```java
String str = "  Hello  ";
System.out.println(str.trim()); // Output: Hello
```
    
12. **`split(String regex)`**  
    Splits the string into an array of substrings based on the given delimiter.
```java
String str = "Hello,World";
String[] parts = str.split(",");
System.out.println(parts[0]); // Output: Hello
```
### Replace
```java
String str = "Hello";
System.out.println(str.replace('l', 'p')); // Output: Heppo
System.out.println(str.replace("Hello", "Hi")); // Output: Hi
```
### Replace All (regular expression)
```java
String str ="hello! anurag.";
System.out.println(str.replace("[ !.]",""));// helloanurag
```

##### replace() Vs replaceAll()
```java
	String str ="hello! anurag.";
    System.out.println(str.replace(" ", "-"));// hello!-anurag.
    System.out.println(str.replaceAll("[ !.]", "-"));// hello--anurag-
```
