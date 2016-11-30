# [8]String to Integer (atoi)

Implement atoi to convert a string to an integer.

Hint: Carefully consider all possible input cases. If you want a challenge, please do not see below and ask yourself what are the possible input cases.

Notes: It is intended for this problem to be specified vaguely (ie, no given input specs). You are responsible to gather all the input requirements up front.

## 思路
要考虑几种特殊的情况，包括空格正负号，溢出，其他字符。

## Code

### Python
```
class Solution(object):
    def myAtoi(self, str):
        """
        :type str: str
        :rtype: int
        """
        sign = 1
        result = 0
        flag = 0
        for c in str:
            if '0' <= c <= '9':
                flag = 1
                result = result*10+int(c)
            elif c == ' ' and flag == 0:
                sign = 1
            elif c == '-' and flag == 0:
                flag = 1
                sign = -1
            elif c == '+' and flag == 0:
                flag = 1
                sign = 1
            else:
                break
        result = sign*result
        if result > 2147483647:
            return 2147483647
        if result < -2147483648:
            return -2147483648
        return result
        ```
Runtime: 75ms





