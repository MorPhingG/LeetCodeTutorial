# [387]First Unique Character in a String

Given a string, find the first non-repeating character in it and return it's index. If it doesn't exist, return -1.

Examples:

s = "leetcode"
return 0.

s = "loveleetcode",
return 2.

## Code

### Python
```
class Solution(object):
    def firstUniqChar(self, s):
        for char in s:
            if s.find(char) == s.rfind(char):
                return s.find(char)
        return -1
```




