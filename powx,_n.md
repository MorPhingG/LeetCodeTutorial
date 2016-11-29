# [50]Pow(x, n)

Implement pow(x, n).

## 思路
二分法


## Code

### Python
```
class Solution(object):
    def myPow(self, x, n):
        """
        :type x: float
        :type n: int
        :rtype: float
        """
        if n == 0:
            return 1.0
        if n < 0:
            return 1/self.myPow(x, -n)
        half = self.myPow(x, n/2)
        if n%2 == 0:
            return half*half
        else:
            return half*half*x
            ```
Runtime: 45ms

### Java 

```
public class Solution {
    public double myPow(double x, int n) {
        if(n == 0) return 1.0;
        double half;
        half = myPow(x,n/2);
        if(n%2 == 0)
        {
            return half*half;
            
        }
        else if(n>0) 
        {
            return half*half*x;
        }
        else
        {
            return half*half/x;
        }
    }
}
```