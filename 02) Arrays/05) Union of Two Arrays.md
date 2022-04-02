# Union of Two Arrays
> **Question**    
> Given two arrays a[] and b[] of size n and m respectively. The task is to find union between these two arrays.      
> Union of the two arrays can be defined as the set containing distinct elements from both the arrays. If there are repetitions, 
> then only one occurrence of the element should be printed in union.   
> Examples : 
<pre>
Input  : 5 3
         1 2 3 4 5
         1 2 3
         
Output : 5

Explanation: 1, 2, 3, 4 and 5 are the elements which comes in the union set of both arrays. So count is 5.
</pre>

### Implementation
```java
public static void unionOfArrays(int[] arr1, int[] arr2) {
    Set<Integer> union = new HashSet();
    for(int num : arr1) union.add(num);
    for(int num : arr2) union.add(num);
    System.out.println(union.size());
}
```
---
