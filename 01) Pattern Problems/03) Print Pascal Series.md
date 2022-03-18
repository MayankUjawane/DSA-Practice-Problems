#  Print Pascal Series
> Question -> Write a program to print the following pattern:       
> Input: 5    
> Output:          
<pre>
1        
1        1        
1        2        1        
1        3        3        1        
1        4        6        4        1   
</pre>

### Implementation
```java
public static void printPattern(int n) {
    int count = 0;
    List<Integer> prev = new ArrayList();

    for(int i=0; i<n; i++) {
        List<Integer> curr = new ArrayList();
        System.out.print("1\t");
        curr.add(1);

        for(int j=0; i>1 && j<i-1; j++) {
            int val = prev.get(j) + prev.get(j+1);
            System.out.print(val+"\t");
            curr.add(val);
        }

        if(i != 0) {
            System.out.print("1");
            curr.add(1);
        }
        prev = curr;
        System.out.println();
    }
}
```
---
