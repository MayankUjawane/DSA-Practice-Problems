# Reverse Array
> Question -> Given an array (or string), the task is to reverse the array/string.     
> Examples : 
<pre>
Input  : arr[] = {1, 2, 3}
Output : arr[] = {3, 2, 1}
</pre>
<pre>
Input :  arr[] = {4, 5, 1, 2}
Output : arr[] = {2, 1, 5, 4}
</pre>


### Implementation
```java
public static void reverse(int[] arr) {
    int left = 0;
    int right = arr.length-1;
    while(left < right) {
        int temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;
        left++;
        right--;
    }
}
```
---
