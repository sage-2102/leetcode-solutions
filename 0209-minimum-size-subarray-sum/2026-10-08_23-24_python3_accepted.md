# 209. Minimum Size Subarray Sum
  
<br>**Problem:** https://leetcode.com/problems/minimum-size-subarray-sum/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Binary Search, Sliding Window, Prefix Sum<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-08 23:24 local time

**Runtime:** 20 ms (beats 31.443200000000036%)
**Memory:** 30.6 MB (beats 42.946400000000004%)


<!-- leetgit:submissionId=2166620409 codeHash=9bce8abf46799e466bd6dc222ae537a4af071635e94582ebd2d41bccdf8f7468 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def minSubArrayLen(self, target: int, nums: list[int]) -> int:
       l,total = 0,0
       res = float("inf")

       for r in range (len(nums)):
            total += nums[r]
            while total >= target:
                res = min(r-l+1,res)
                total -= nums[l]
                l += 1

       return 0 if res == float("inf") else res
```
