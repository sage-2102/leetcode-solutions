# 58. Length of Last Word
  
<br>**Problem:** https://leetcode.com/problems/length-of-last-word/<br>

**Difficulty:** Easy<br>
**Topics:** String<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-10-09 20:09 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.3 MB (beats 54.85079999999998%)


<!-- leetgit:submissionId=2167373097 codeHash=58572a037c1835eb092dc9ade97d3acc5768e48573fb2e44d492380d43fd66d8 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
class Solution:
    def lengthOfLastWord(self, s: str) -> int:
        #split the sentence into words
        w = s.split()
        return len(w[-1])
```
