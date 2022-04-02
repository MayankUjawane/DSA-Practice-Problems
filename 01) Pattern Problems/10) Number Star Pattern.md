# Number Star Pattern
> Question -> Write a program to print the following pattern:     
> Input: 3      
> Output:   
<pre>
1*2*3*10*11*12
--4*5*8*9
----6*7
</pre>
> Input: 4      
> Output:   
<pre>
1*2*3*4*17*18*19*20
--5*6*7*14*15*16
----8*9*12*13
------10*11
</pre>

### Implementation
```java
public static void printPattern(int n) {
    int leftCounter = 1;
    int rightCounter = n*n + 1;
    for(int i=0; i<n; i++) {
        for(int j=0; j<n; j++) {
            if(j < i) {
                System.out.print("--");
            } else {
                System.out.print(leftCounter+"*");
                leftCounter++;
            }
        }
        for(int j=0; j<n-i; j++) {
            System.out.print(rightCounter+j);
            if(j != n-i-1) System.out.print("*");
        }
        rightCounter -= (n-i-1);
        System.out.println();
    }
}
```
---
