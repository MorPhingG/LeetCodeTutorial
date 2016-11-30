# [326]Power of Three

Given an integer, write a function to determine if it is a power of three.

## 思路
因为当位数确定时，3的幂只有2到3种可能.故只需判断该整数是否等于那三个数即可。

## Code

### Python
```
class Solution(object):
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
        
 ```
 class Solution(object):
    def isPowerOfThree(self, n):
        """
        :type n: int
        :rtype: bool
        """
        pow = 2*(len(str(n))-1)
        if 3**pow == n or 3**(pow+1) == n or 3**(pow+2) == n:
            return True
        else:
            return False
            ```
  Runtime: 238ms



