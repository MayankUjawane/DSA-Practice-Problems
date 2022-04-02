# Rotate Array By One Position
> Question -> Given an array, rotate the array by one position in clock-wise direction.     
> Examples : 
<pre>
Input  : arr[] = {1, 2, 3, 4, 5}
Output : arr[] = {5, 1, 2, 3, 4}
</pre>

### Implementation
```java
public static void rotateArrayByOne(int[] arr) {
    int start = 0;
    int end = arr.length-1;
    reverse(arr, start, end-1);
    reverse(arr, start, end);
}
public static void reverse(int[] arr, int start, int end) {
    while(start < end) {
        int temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
}
```
---
