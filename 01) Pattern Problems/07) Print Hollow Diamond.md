# Print Hollow Diamond
> Question -> Write a program to print the following pattern:     
> Input: 5      
> Output:   
<pre>
*	*	*		*	*	*	
*	*				*	*	
*						*	
*	*				*	*	
*	*	*		*	*	*   
</pre>

### Implementation
```java
public static void printPattern(int n) {
    for(int i=0; i<n; i++) {
        if(i<=n/2) {
            for(int space=0; space<(n/2-i+1); space++) {
                System.out.print("*\t");
            }
            for(int star=0; star<(2*i+1); star++) {
                System.out.print("\t");
            }
            for(int space=0; space<(n/2-i+1); space++) {
                System.out.print("*\t");
            }
        } else {
            for(int space=0; space<(i-n/2+1); space++) {
                System.out.print("*\t");
            }
            for(int star=0; star<(2*(n-i)-1); star++) {
                System.out.print("\t");
            }
            for(int space=0; space<(i-n/2+1); space++) {
                System.out.print("*\t");
            }
        }
        System.out.println();
    }
}
```
---
