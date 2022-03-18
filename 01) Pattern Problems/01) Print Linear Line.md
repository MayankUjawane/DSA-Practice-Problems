# Print Linear Line
> Question -> Write a program to print the following pattern:
> Input: 3
> Output:   
<pre>
                *                        

        *                                

* 
</pre>

### Implementation
```java
public static void printPattern(int n) {
    for(int i=1; i<=n; i++) {
        for(int space=n-i; space>0; space--) {
            System.out.print("\t");
        }
        System.out.println("*");
        System.out.println();
    }
}
```
---
