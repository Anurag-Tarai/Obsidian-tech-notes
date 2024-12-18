```java

import java.util.*;
public class MyClass {
  public static void main(String args[]) {
      int[] arr = {10, 20, 15, 5, 25, 30, 1, 40};
       // Expected Output: [1, 5, 10, 15, 20, 25, 30, 40]

      System.out.println(Arrays.toString(arr));
      mergeSort(arr, 0, arr.length-1);
      System.out.println(Arrays.toString(arr));
  }
  
  // merge sort method
  static void mergeSort(int arr[], int low, int high){
      if(low>=high) return;
      int mid = (low+high)/2;
      mergeSort(arr, low, mid);
      mergeSort(arr, mid+1, high);
      merge(arr, low, mid, high);
  }

	// merge method
  static void merge(int[]arr, int low, int mid,int high){
      List<Integer> list = new ArrayList<>();
      int l = low;
      int r = mid+1;
      while(l<=mid && r<=high){
          if(arr[l]<=arr[r]){
              list.add(arr[l]);
              l++;
          }else{
              list.add(arr[r]);
              r++;
          }
      }
      while(l<=mid){
           list.add(arr[l]);
              l++;
      }
      while(r<=high){
           list.add(arr[r]);
            r++;
      }
      // updating value from low to high in original array
      // We subtract starting from current index to get 0th indexing value of current index, same as we subtract 'a' from other character to get 0th indexing value
      for(int i=low; i<=high; i++){
          arr[i] = list.get(i-low);
      }
  }
}
```