# 792. Binary Search
  
<br>**Problem:** https://leetcode.com/problems/binary-search/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Binary Search<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 01:04 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 20.6 MB (beats 10.034900000000015%)


<!-- leetgit:submissionId=2166708093 codeHash=27b04e533b64946b4783f6b361fd7cf4651149765cab84ed92c8d91a071d654c notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def search(self, nums: list[int], target: int) -> int:
       l,r = 0,len(nums)-1

       while l<=r:
          m = (l+r)//2
          if nums[m]>target:
            r = m-1
          elif nums[m]<target:
            l = m+1
          else :
            return m
       return -1
```
