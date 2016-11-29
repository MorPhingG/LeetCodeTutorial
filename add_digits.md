# [258]Add Digits

Given a non-negative integer num, repeatedly add all its digits until the result has only one digit.

For example:

Given num = 38, the process is like: 3 + 8 = 11, 1 + 1 = 2. Since 2 has only one digit, return it.


## 思路
可发现规律：输入每增加一，结果就增加一。当输入为10时，结果减9变为1.

## Code

### Python:
```class Solution(object):
    def addDigits(self, num):
        """
        :type num: int
        :rtype: int
        """
        return 0 if num == 0 else (num-1)%9+1
        ```


### Java:
```
public class Solution {
    public int addDigits(int num) {
        return (num-1)%9+1;
    }
}```