# Rain Water Trapping
> **Question**    
> Given an array arr[] of N non-negative integers representing the height of blocks. If width of each block is 1, compute how much water 
> can be trapped between the blocks during the rainy season.          

**Examples** : 
<pre>
Input  : N = 6
         arr[] = {3,0,0,2,0,4}
         
Output : 10
</pre>
<pre>
Input  : N = 4
         arr[] = {7,4,0,9}

Output : 10
</pre>

### Implementation
```java
public static int maxWater(int[] arr) {
    int n = arr.length;
    
    int[] prefixHeight = new int[n];
    int maxHeight = 0;
    for(int i=0; i<n; i++) {
        int height = arr[i];
        if(height > maxHeight) maxHeight = height;
        prefixHeight[i] = maxHeight;
    }
    
    int[] suffixHeight = new int[n];
    maxHeight = 0;
    for(int i=n-1; i>=0; i--) {
        int height = arr[i];
        if(height > maxHeight) maxHeight = height;
        suffixHeight[i] = maxHeight;
    }

    int maxWater = 0;
    for(int i=0; i<n; i++) {
        int height = Math.min(prefixHeight[i],suffixHeight[i]);
        int currHeight = arr[i];
        maxWater += height-currHeight; 
    }
    return maxWater;
}
```
---
