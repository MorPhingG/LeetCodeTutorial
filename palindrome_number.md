# [9]Palindrome Number

Determine whether an integer is a palindrome. Do this without extra space.

## 思路
因为不能使用额外的空间，所以转换为字符串的方法在这里就不适用了。一个好的解答是依次比较最高位和最低位是否相等，如果比完所有位发现都满足条件的话，该数即为回文数。

## Code

### Python
```
class Solution(object):
    def isPalindrome(self, x):
        """
        :type x: int
        :rtype: bool
        """
        if x < 0:
            return False
        div = 1
        while x / div >= 10:
            div *= 10
        while x > 0:
            start = x / div
            end = x % 10
            if start != end:
                return False
            x = x % div / 10
            div = div / 100
        return True
        ```
Runtime: 242ms

### Java

```
public class Solution {
    public boolean isPalindrome(int x) {
        int sum = 0;
        int x1 = x;
        if(x<0)
        return false;
        while(x>0)
        {
            sum = sum*10+x%10;
            x = x/10;
        }
        if(x1 == sum)
        return true;
        else return false;
        
    }
}
```