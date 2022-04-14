# Count Inversions
> **Question**    
> Given an array of integers. Find the Inversion Count in the array.          
> **Inversion Count**: For an array, inversion count indicates how far (or close) the array is from being sorted. 
> If the array is already sorted then the inversion count is 0. If an array is sorted in the reverse order then the inversion count is the maximum.      
> Formally, two elements a[i] and a[j] form an inversion if a[i] > a[j] and i < j.     

**Examples** : 
<pre>
Input  : N = 5, arr[] = {2, 4, 1, 3, 5}
Output : 3
Explanation: The sequence (2, 4, 1, 3, 5) has three inversions (2, 1), (4, 1), (4, 3).
</pre>
<pre>
Input  : N = 5, arr[] = {2, 3, 4, 5, 6}
Output : 0
</pre>

### Implementation
```java
public class Main {
    public static void main(String[] args) {
        int[] arr = {2, 3, 4, 5, 6};
        System.out.println(bubbleSort(arr));
    }
    public static int bubbleSort(int[] arr) {
        int n = arr.length;
        int inversions = 0;
        for(int i=0; i<n-1; i++) {
            boolean swapHappened = false;
            for(int j=0; j<n-1-i; j++) {
                if(arr[j] > arr[j+1]) {
                    swap(arr, j, j+1);
                    swapHappened = true;
                    inversions++;
                }
            }
            if(swapHappened == false) break;
        }
        return inversions;
    }
    public static void swap(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```
---
