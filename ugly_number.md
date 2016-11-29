# [263]Ugly Number

Write a program to check whether a given number is an ugly number.

Ugly numbers are positive numbers whose prime factors only include 2, 3, 5. For example, 6, 8 are ugly while 14 is not ugly since it includes another prime factor 7.

Note that 1 is typically treated as an ugly number.

## 思路
判断一个数的基本因子是否只包括2，3，5，只需将数不断除以2，3，5即可。

## Code

### Python
```
class Solution(object):
    def isUgly(self, num):
        """
        :type num: int
        :rtype: bool
        """
        while num >= 2:
            if num % 5 == 0:
                num = num/5
            elif num % 3 == 0:
                num = num/3
            elif num % 2 == 0:
                num = num/2
            else:
                return False
        return num == 1
        ```
Runtime: 52ms

### Java
```
public class Solution {
    public boolean isUgly(int num) {
        while(num>=2)
        {
            if(num%2==0)
            num = num/2;
            else if(num%3==0)
            num = num/3;
            else if(num%5==0)
            num = num/5;
            else return false;
        }
        if(num==1)
        return true;
        else return false;
    }
}
```



