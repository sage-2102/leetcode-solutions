# 88. Merge Sorted Array
  
<br>**Problem:** https://leetcode.com/problems/merge-sorted-array/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Two Pointers, Sorting<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-12 20:20 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 40.05209999999999%)


<!-- leetgit:submissionId=2170283650 codeHash=8f09e47a4e5e8309858e5dcc845e8715d512e8f641450734e62e4c9393f6df8d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def merge(self, nums1: list[int], m: int, nums2: list[int], n: int) -> None:
        last = m + n - 1

        while m > 0 and n > 0:
            if nums1[m-1] > nums2[n-1]:
                nums1[last] = nums1[m-1]
                m -= 1
            else:
                nums1[last] = nums2[n-1]
                n -= 1
            last -= 1

        while n > 0:
            nums1[last] = nums2[n-1]
            n,last = n-1,last-1
        
```
