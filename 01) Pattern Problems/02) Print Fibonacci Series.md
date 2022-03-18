# Print Fibonacci Series
> Question -> Write a program to print the following pattern:     
> Input: 5      
> Output:   
<pre>
0        
1        1        
2        3        5        
8        13       21        34        
55       89       144       233       377   
</pre>

### Implementation
```java
public static void printPattern(int n) {
    int a = 1, b = 2;
    for(int i=0; i<n; i++) {
        for(int j=0; j<=i; j++) {
            if(i<=1) {
                System.out.print(i+"\t");
            } else {
                System.out.print(b+"\t");
                int temp = b;
                b += a;
                a = temp;
            }
        }
        System.out.println();
    }
}
```
---
