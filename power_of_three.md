# [326]Power of Three

Given an integer, write a function to determine if it is a power of three.

## Code

### Python
```class Solution(object):
    def isPowerOfThree(self, n):
        if n <= 0:
            return False
        rem = 0
        while n > 1 and rem == 0:
            rem = n % 3
            n = n / 3
            if (n < 1 or rem != 0):
                return False
        return True
        ```



