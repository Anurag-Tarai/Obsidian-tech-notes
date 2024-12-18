```java
int[] array1 = {1, 2, 3}; 
int[] array2 = {4, 5, 6};
```
1. **Swapping References**: Use a temporary variable to swap the references, allowing one array to point to the other's data.
	- arrays **do not need to be the same**

```java
int[] temp = array1;
array1 = array2;
array2 = temp;
```
    
2. **Swapping Contents**: Manually iterate and exchange elements when both arrays have the same length.
	- Arrays length should be same
```java
for (int i = 0; i < array1.length; i++) {
    int temp = array1[i];
    array1[i] = array2[i];
    array2[i] = temp;
}
```
### Key Points:

- Reference swap is efficient but changes only the reference addresses.
- Content swap modifies the actual data inside the arrays.