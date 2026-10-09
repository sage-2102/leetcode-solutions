# 26. Remove Duplicates from Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 20:07 local time

**Runtime:** 83 ms (beats 5.0034000000000045%)
**Memory:** 20.5 MB (beats 80.05960000000002%)


<!-- leetgit:submissionId=2167372121 codeHash=518d3aaee5301b8c96df365f29f3355eefe3040f86ae86ee0a4d561845605568 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        i=0
        j=1

        while i<len(nums)and j<len(nums):
            if nums[i]==nums[j]:
                nums.remove(nums[i])
            else:
                i+=1
                j+=1
        return len(nums)
```
