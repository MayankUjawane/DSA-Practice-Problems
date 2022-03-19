# Print Number Diamond
> Question -> Write a program to print the following pattern:     
> Input: 5      
> Output:   
<pre>
		1	
	2	3	2	
3	4	5	4	3	
	2	3	2	
		1	  
</pre>

### Implementation
```java
public static void printPattern(int n) {
    for(int i=1; i<=(n/2 + 1); i++) {
        for(int space=0; space<=n/2-i; space++) {
            System.out.print("\t");
        }
        int num=0;
        for(; num<i; num++) {
            System.out.print((num+i) + "\t");
        }
        num += (i-2);
        for(; num>=i; num--) {
            System.out.print((num) + "\t");
        }
        System.out.println();
    }
    for(int i=n/2; i>=1; i--) {
        for(int space=0; space<=(n/2-i); space++) {
            System.out.print("\t");
        }
        int num=0;
        for(; num<i; num++) {
            System.out.print((num+i) + "\t");
        }
        num += (i-2);
        for(; num>=i; num--) {
            System.out.print((num) + "\t");
        }
        System.out.println();
    }    
}
```
---  
