# Best Time to Buy and Sell Stock
> **Question**    
> You are given an array, prices where prices[i] is the price of a given stock on the ith day.
> You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.
> Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0. 

**Examples** : 
<pre>
Input  : prices = [7,1,5,3,6,4]
Output : 5
Explanation : Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
              Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
</pre>
<pre>
Input  : prices = [7,6,4,3,1]
Output : 0
</pre>

### Implementation
```java
public static int maxProfit(int[] prices) {
    int ans = 0;
    int min = prices[0];
    for(int price: prices) {
        if(price < min) {
            min = price;
            continue;
        }
        if((price-min) > ans) {
            ans = (price-min);
        }
    }
    return ans;
}
```
---
