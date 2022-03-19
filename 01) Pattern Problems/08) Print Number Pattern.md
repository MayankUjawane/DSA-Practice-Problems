# Print Number Pattern
> Question -> Write a program to print the following pattern:     
> Input: 7      
> Output:   
<pre>
1												1	
1	2										2	1	
1	2	3								3	2	1	
1	2	3	4						4	3	2	1	
1	2	3	4	5				5	4	3	2	1	
1	2	3	4	5	6		6	5	4	3	2	1	
1	2	3	4	5	6	7	6	5	4	3	2	1	 
</pre>

### Implementation
```java
public static void printPattern(int n) {
  int space = 2*n-1;
    for(int i=1; i<=n; i++) {
        space -= 2;
        for(int num=1; num<=i; num++) {
            System.out.print(num+"\t");
        }
        for(int s=space; s>0; s--) {
            System.out.print("\t");
        }

        int num;
        if(space < 0) {
            num = i-1;
        } else {
            num = i;
        }
        for( ; num>0; num--) {
            System.out.print(num+"\t");
        }
        System.out.println();
    }
}
```
---
