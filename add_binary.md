# [67]Add Binary

Given two binary strings, return their sum (also a binary string).

For example,
a = "11"
b = "1"
Return "100".

## Code

### Python

```class Solution(object):
    def addBinary(self, a, b):
        aInt = int(a,2)
        bInt = int(b,2)
        sumInt = aInt + bInt
        return bin(sumInt)[2:]
        
```



