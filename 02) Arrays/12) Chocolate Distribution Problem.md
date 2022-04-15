# Chocolate Distribution Problem
> **Question**    
> Given an array A[ ] of positive integers of size N, where each value represents the number of chocolates in a packet. Each packet can have a variable number of chocolates. There are M students, the task is to distribute chocolate packets among M students such that :
> 1. Each student gets exactly one packet.
> 2. The difference between maximum number of chocolates given to a student and minimum number of chocolates given to a student is minimum.


**Examples** : 
<pre>
Input  : N = 8, M = 5
         A = {3, 4, 1, 9, 56, 7, 9, 12}
Output : 6
Explanation : The minimum difference between maximum chocolates and minimum chocolates is 9 - 3 = 6 by choosing following M packets :
              {3, 4, 9, 7, 9}.
</pre>
<pre>
Input  : N = 7, M = 3
         A = {7, 3, 2, 4, 9, 12, 56}
Output : 2
Explanation : The minimum difference between maximum chocolates and minimum chocolates is 4 - 2 = 2 by choosing following M packets :
              {3, 2, 4}.
</pre>

### Implementation
```java
public static int maxProfit(int[] arr, int m, int n) {
    // if there are no chocolates or number of students is 0
    if(m == 0 || n == 0) return 0;

    // Number of students cannot be more than number of packets
    if(n < m) return -1;

    Arrays.sort(arr);
    int minDiff = Integer.MAX_VALUE;
    for(int i=0; i<n-m; i++) {
        int min = arr[i];
        int max = arr[i+m-1];
        minDiff = Math.min(minDiff, max-min);
    }
    return minDiff;
}
```
---
