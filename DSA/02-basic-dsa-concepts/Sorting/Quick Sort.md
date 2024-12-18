```java
import java.util.*;

public class MyClass {
  public static void main(String args[]) {
   int []arr = {12,3,3,34,123,1,12,2,13};
   System.out.println(Arrays.toString(arr));
   quickSort(arr, 0, arr.length-1);
   System.out.println(Arrays.toString(arr));
  }
  
  public static void quickSort(int[]arr, int low, int high){
      if(low>=high) return;
      int p = partition(arr, low, high);
      quickSort(arr, low, p-1);
      quickSort(arr,p+1, high);
  }
  
  public static int partition(int[]arr, int low, int high){
      int pivot = arr[low];
      int l = low;
      int r = high;
      while(l<r){
          while(arr[l]<=pivot && l<=high-1){
              l++;
          }
          while(arr[r]>=pivot && r>=low+1){
              r--;
          }
          if(l<r) swap(arr, l, r);
      }
      swap(arr , low, r);
      return r;
  }
  
  public static void swap(int [] arr, int a, int b){
     int temp = arr[a];
     arr[a] = arr[b];
     arr[b] = temp;
  }
  
}
```