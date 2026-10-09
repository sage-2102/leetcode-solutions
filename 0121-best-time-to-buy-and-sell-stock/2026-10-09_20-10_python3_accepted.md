# 121. Best Time to Buy and Sell Stock
  
<br>**Problem:** https://leetcode.com/problems/best-time-to-buy-and-sell-stock/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 20:10 local time

**Runtime:** 78 ms (beats 9.54460000000005%)
**Memory:** 28.7 MB (beats 43.27069999999996%)


<!-- leetgit:submissionId=2167374001 codeHash=aa2ed5266ba845e349bd9923be6ef15508102561f0f7d8f4c6b86ceb23059425 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxProfit(self, prices: list[int]) -> int:
       l,r = 0,1
       maxP = 0

       while r<len(prices):
            if prices[l] < prices[r]:
               profit = prices[r]-prices[l]
               maxP = max(maxP,profit) 
            else:
                l = r
               
               
            r += 1
       return maxP           
```
