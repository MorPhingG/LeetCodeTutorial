# [172]Factorial Trailing Zeroes

Given an integer n, return the number of trailing zeroes in n!.

Note: Your solution should be in logarithmic time complexity.

## 思路
只有5和2能产生末尾的0，在因子中，5的数量一定比2少，故统计因子5的个数就可以了。每5个数出现一次5，故将n反复除以5，求得每次5的个数加起来即为总共的5个个数。


## Code

### Python
```
class Solution(object):
    def trailingZeroes(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n <= 0:
            return 0
        sum = 0
        while n>=5:
            sum += n/5
            n = n/5
        return sum
        ```
Runtime: 32ms

### Java

```
public class Solution {
    public int trailingZeroes(int n) {
        if(n<0)
        return -1;
        int sum5=0;
        while(n>0)
        {
            sum5+=n/5;
            n/=5;
        }
        return sum5;
    }
}
```