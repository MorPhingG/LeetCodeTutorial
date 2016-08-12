# [202]Happy Number

Write an algorithm to determine if a number is "happy".

A happy number is a number defined by the following process: Starting with any positive integer, replace the number by the sum of the squares of its digits, and repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle which does not include 1. Those numbers for which this process ends in 1 are happy numbers.

Example: 19 is a happy number

12 + 92 = 82
82 + 22 = 68
62 + 82 = 100
12 + 02 + 02 = 1

## Code

### Python

```class Solution(object):
    def isHappy(self, n):
        def sum(number):
            sum = 0
            while number != 0:
                sum += (number%10)**2
                number = number / 10
            return sum
            
        numDict = {}
        if n == 0:
            return False
        while n != 1:
            if n in numDict:
                return False
            numDict[n] = 1
            n = sum(n)
        return True
        ```



