# [400]Nth Digit

Find the nth digit of the infinite integer sequence 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, ...

Note:
n is positive and will fit within the range of a 32-bit signed integer (n < 231).

Example 1:

Input:
3

Output:
3
Example 2:

Input:
11

Output:
0

Explanation:
The 11th digit of the sequence 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, ... is a 0, which is part of the number 10.

## 思路
直白的迭代

## Code

### Python
```
class Solution(object):
    def findNthDigit(self, n):
        """
        :type n: int
        :rtype: int
        """
        b = 1
        while n>b*9*10**(b-1):
            n -= b*9*10**(b-1)
            b += 1
        num = (n-1) / b
        rem = (n-1) % b
        return int(str(10**(b-1)+num)[rem])
        ```
Runtime: 32ms





