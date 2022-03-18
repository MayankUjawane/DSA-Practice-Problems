# Print Plus of String
> Question -> Given a string, print it inside a matrix in such a way that a ‘plus’ is formed.     
> Input: TOP      
> Output:   
<pre>
X    T    X
T    O    P
X    P    X
</pre>
> Input: FEVER    
> Output:
<pre>
X    X    F    X    X
X    X    E    X    X
F    E    V    E    R
X    X    E    X    X
X    X    R    X    X
</pre>

### Implementation
```java
public static void printPattern(String s) {
    int n = s.length();
    int half = n/2;
    for(int i=0; i<n; i++) {
        if(i == half) {
            for(int j=0; j<n; j++) {
                System.out.print(s.charAt(j)+"\t");
            }
        } else {
            for(int j=0; j<n; j++) {
                if(j == half) {
                    System.out.print(s.charAt(i)+"\t");
                } else {
                    System.out.print("X\t");
                }
            }
        }
        System.out.println();
    }
}
```
---
