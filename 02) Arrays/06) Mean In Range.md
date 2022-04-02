# Mean In Range
> **Question**    
> Given an array of n integers and q queries. Write a program to find floor value of mean in range l to r for each query in a new line.         
     
**Example** : 
<pre>
Input  : Arr[] = {1, 2, 3, 4, 5}      
         Q = 3        
         queries[] = {0, 2, 1, 3, 0, 4}
         
Output : 2 3 3

Explanation: Here we can see that the array of integers is [1, 2, 3, 4, 5].
             Query 1: L = 0 and R = 2
                      Sum = 6
                      Integer Count = 3
                      So, Mean is 2
             Query 2: L = 1 and R = 3
                      Sum = 9
                      Integer Count = 3
                      So, Mean is 3
             Query 3: L = 0 and R = 4
                      Sum = 15
                      Integer Count = 5
                      So, the Mean is 3. 
             So, In the end, the function will return the array [2, 3, 3] as an answer.
</pre>

### Implementation
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        int[] arr = {1,2,3,4,5};
        int Q = 3;
        int[] queries = {0, 2, 1, 3, 0, 4}; 
        int[] ans = new int[Q];
        int index = 0;
        for(int i=0; i<queries.length; i+=2) {
            int start = queries[i];
            int end = queries[i+1];
            int val = meanInRange(arr, start, end);
            ans[index++] = val;
        }
        System.out.println(Arrays.toString(ans));
    }
    public static int meanInRange(int[] arr, int start, int end) {
        int sum = 0;
        int count = 0;
        for(int i=start; i<=end; i++) {
            sum += arr[i];
            count++;
        }
        return sum/count;
    }
}
```
---
