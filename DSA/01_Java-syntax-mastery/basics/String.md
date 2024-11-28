### Substring 
```java
	// to find substring
	String str = "anurag";
	String substr = str.substring(0,3);// "anu"
	// exclude the 3
```


## String Builder
```java
// StringBuilder create
StringBuilder sb = new StringBuilder();
sb.append("Hello");  // Adds "Hello" to the StringBuilder
sb.append(' ');      // Adds a space
sb.append("World");  // Adds "World"
System.out.println(sb);  // Output: "Hello World"

// Empty the sb
sb.setLength(0); // Clears the StringBuilder and assigns an empty string

// To find the length
sb.length();

// Insert
StringBuilder sb = new StringBuilder("HelloWorld");
sb.insert(5, " ");  // Inserts a space at index 5
System.out.println(sb);  // Output: "Hello World"

// Delete
StringBuilder sb = new StringBuilder("Hello World");
sb.delete(5, 6);  // Deletes the space between "Hello" and "World"
System.out.println(sb);  // Output: "HelloWorld"

// DeleteCharAt
StringBuilder sb = new StringBuilder("Hello");
sb.deleteCharAt(0);  // Removes the character at index 0 ("H")
System.out.println(sb);  // Output: "ello"

// Replace
StringBuilder sb = new StringBuilder("Hello World");
sb.replace(6, 11, "Java");  // Replaces "World" with "Java"
System.out.println(sb);  // Output: "Hello Java"

// Reverse
StringBuilder sb = new StringBuilder("Hello");
sb.reverse();  // Reverses the string
System.out.println(sb);  // Output: "olleH"

// IndexOf
StringBuilder sb = new StringBuilder("Hello World");
int index = sb.indexOf("World");  // Finds the index of "World"
System.out.println(index);  // Output: 6

// LastIndexOf
StringBuilder sb = new StringBuilder("Hello Hello");
int lastIndex = sb.lastIndexOf("Hello");  // Finds the last occurrence of "Hello"
System.out.println(lastIndex);  // Output: 6

// Substring
StringBuilder sb = new StringBuilder("Hello World");
String sub = sb.substring(6, 11);  // Extracts "World" from the string
System.out.println(sub);  // Output: "World"

// CharAt
StringBuilder sb = new StringBuilder("Hello");
char ch = sb.charAt(1);  // Gets the character at index 1 ('e')
System.out.println(ch);  // Output: 'e'

// ToString
StringBuilder sb = new StringBuilder("Hello World");
String result = sb.toString();  // Converts the StringBuilder to a String
System.out.println(result);  // Output: "Hello World"

```