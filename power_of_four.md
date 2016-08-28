# [342]Power of Four

Given an integer (signed 32 bits), write a function to check whether it is a power of 4.

Example:
Given num = 16, return true. Given num = 5, return false.

## Code

### Python
```
class Solution(object):
    def isPowerOfFour(self, num):
        if num <= 0:
            return False
        rem = 0
        while num > 1 and rem == 0:
            rem = num % 4
            num = num / 4
            if (num < 1 or rem != 0):
                return False
        return True
```



