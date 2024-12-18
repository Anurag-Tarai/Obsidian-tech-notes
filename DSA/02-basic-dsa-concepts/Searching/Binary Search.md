```java
public class MyClass {
  public static void main(String args[]) {
    int[] arr = {2,4,5,6,7,8};
    int k = 8;
    int i = binarySearch(arr, 0, arr.length-1, k);
    System.out.println(i);
  }
  
  public static int binarySearch(int[]arr, int l, int r, int k){
      if(l>r) return -1;
      int mid = (l+r)/2;
      if(arr[mid]==k) return mid;
      else if(arr[mid]<k) return binarySearch(arr, mid+1, r, k);
      else return binarySearch(arr,0,mid-1,k);
    //   return -1;
  }
}
```