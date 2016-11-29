# [204]Count Primes

Description:

Count the number of prime numbers less than a non-negative number, n.


## 思路
合数都是两个数相乘得到的，故我们可以用迭代乘法找出所有合数，剩下的就是质数了。


## Code

### Python
```
class Solution(object):
    def countPrimes(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n <= 2:
            return 0
        trueTable = [True]*n
        trueTable[0:2] = [False]*2
        for i in range(2, int(n**0.5)+1):
            if trueTable[i] == False:
                continue
            for j in range(i, int((n-1)/i)+1):
                trueTable[i*j] = False
        return sum(trueTable)
        ```

Runtime: 996ms

```
class Solution(object):
    def countPrimes(self, n):
        """
        :type n: int
        :rtype: int
        """
        if n <= 2:
            return 0
        trueTable = [True]*n
        trueTable[0:2] = [False]*2
        for i in range(2, int(n**0.5)+1):
            if trueTable[i] == True:
                trueTable[i*2:n:i] = [False]*((n-1-i*2)/i+1)
        return sum(trueTable)
        ```

Runtime: 275ms


### Java

```
public class Solution {
    public int countPrimes(int n) {
        int sum=0;
        boolean c[] = new boolean[n];
        for (int i=2;i*i<n;i++)
        {
            if(!c[i])
            {
                for (int j=i;j*i<n;j++)
                {
                    c[j*i] = true;
                }
            }
        }
        for (int i=2; i<n;i++)
        {
            if(!c[i])
            sum++;
        }
        return sum;
    }
}```