# Subarray and Subsequence
> **Question**    
> Write a program where you need to print all the subarrays and all the subsequences of an array, based on the user input.       

<pre>
Input  : The first line consists of size and then array elements. The second line of the input has a number, that is either 1 or 2. 
If you get a 1, then print all the subarrays of the input array, if you get 2, then print all the subsequences of the input array. 
If you get any number other than 1 or 2, output “INVALID CHOICE”.
4 1 2 3 4
1 - print subarrays
2 - print subsequences
4 - INVALID CHOICE
</pre>

### Implementation
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for(int i=0; i<n; i++) {
            arr[i] = sc.nextInt();
        }
        int option = sc.nextInt();

        if(option == 1) {
            printSubArray(arr, n);
        } else if(option == 2) {
            printSubsequence(arr, n);
        } else {
            System.out.println("INVALID CHOICE");
        }
    }
    
    public static void printSubArray(int[] arr, int n) {
        for(int length=1; length<=n; length++) {
            for(int i=0; i<=n-length; i++) {
                for(int index=i; index<i+length; index++) {
                    System.out.print(arr[index]+" ");
                } 
                System.out.println();
            }
        }
    }
    
    public static void printSubsequence(int[] arr, int n) {
        int total = (int)Math.pow(2,n);
        for(int i=0; i<total; i++) {
            List<Integer> list = new ArrayList();
            int temp = i;
            for(int j=0; j<n; j++) {
                int rem = temp%2;
                temp = temp/2;
                if(rem == 1) list.add(arr[j]);
            }
            if(list.size() > 0) System.out.println(list);
        }
    }
}
```
---
