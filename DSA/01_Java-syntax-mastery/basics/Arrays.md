## Copy Array to another 
```java
way 1--------
int[] array1 = {1, 2, 3, 4, 5};
int[] array2 = new int[array1.length];

for (int i = 0; i < array1.length; i++) {
    array2[i] = array1[i];
}

way 2--------
int[] array1 = {1, 2, 3, 4, 5};
int[] array2 = Arrays.copyOf(array1, array1.length);
```