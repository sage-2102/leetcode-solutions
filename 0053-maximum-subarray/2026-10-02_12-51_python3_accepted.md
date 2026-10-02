# 53. Maximum Subarray
  
<br>**Problem:** https://leetcode.com/problems/maximum-subarray/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Divide and Conquer, Dynamic Programming<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-02 12:51 local time

**Runtime:** 26 ms (beats 86.083%)
**Memory:** 31.3 MB (beats 75.42930000000001%)


<!-- leetgit:submissionId=2159905739 codeHash=50b6c0e8c135c8248aa53d92bb07f0db5073ef8f2e7f96a54f6249182c9399f7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def maxSubArray(self, nums: list[int]) -> int:
        maxSub = nums[0]
        curSum = 0

        for n in nums:
            if curSum < 0:
               curSum = 0
            curSum += n
            maxSub = max(maxSub,curSum)
        return maxSub
```
