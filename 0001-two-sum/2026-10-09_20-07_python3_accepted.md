# 1. Two Sum
  
<br>**Problem:** https://leetcode.com/problems/two-sum/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 20:07 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 20.4 MB (beats 59.76279999999996%)


<!-- leetgit:submissionId=2167371553 codeHash=e7d9a48732b1932ee2383bda35bb0d1638b4dffddd282cb7a2025cd2c67dda92 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        seen={}
        for i in range (len(nums)):
            complement = target- nums[i]

            if complement in seen :
               return[seen[complement],i]

            seen [nums[i]] = i
```
