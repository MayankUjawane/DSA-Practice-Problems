# Maximum Sum Subarray
> **Question**    
> Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.
> A subarray is a contiguous part of an array.         

**Examples** : 
<pre>
Input  : nums = [-2,1,-3,4,-1,2,1,-5,4]
Output : 6
Explanation: [4,-1,2,1] has the largest sum = 6
</pre>
<pre>
Input  : nums = [5,4,-1,7,8]
Output : 23
</pre>

### Implementation
```java
public static int maxSubarray(int[] arr) {
    int sum = 0;
    int max = Integer.MIN_VALUE;
    for(int num : arr) {
        sum += num;
        if(sum > max) max = sum;
        if(sum < 0) sum = 0;
    }
    return max;
}
```
---
