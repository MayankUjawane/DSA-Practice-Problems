# Minimum and Maximum of an Array
> Question -> Write a function to return the minimum element and maximum element in an array. Your program should make the minimum number of comparisons.     
> Example : 
<pre>
Input :  arr[] = {4, 5, 1, 2}
Output : 1 5
</pre>

### Implementation
```java
public static void minAndMaxOfArray(int[] arr) {
    int min = arr[0];
    int max = arr[0];
    for(int num : arr) {
        if(num > max) max = num;
        if(num < min) min = num;
    }
    System.out.println(min+" "+max);
}
```
---
