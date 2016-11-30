# [168]Excel Sheet Column Title

Given a positive integer, return its corresponding column title as appear in an Excel sheet.

For example:

    1 -> A
    2 -> B
    3 -> C
    ...
    26 -> Z
    27 -> AA
    28 -> AB 
    
## 思路
迭代，相当于十进制转二十六进制。

## Code

### Python
```
class Solution(object):
    def convertToTitle(self, n):
        """
        :type n: int
        :rtype: str
        """
        s = ''
        while n > 0:
            s += chr((n-1)%26+65)
            n = (n-1)/26
        return s[::-1]
        ```
Runtime: 32ms





