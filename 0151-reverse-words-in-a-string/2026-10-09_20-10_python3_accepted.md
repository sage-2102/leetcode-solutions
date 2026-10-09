# 151. Reverse Words in a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-words-in-a-string/<br>

**Difficulty:** Medium<br>
**Topics:** Two Pointers, String<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 20:10 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.2 MB (beats 80.31259999999999%)


<!-- leetgit:submissionId=2167374509 codeHash=97955e6988a6aa130360bd35d1082680c877576c9284a86ae3b326aaca055385 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def reverseWords(self, s: str) -> str:
        return " ".join(reversed(s.strip().split()))
```
