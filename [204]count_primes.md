# [204]Count Primes

Description:

Count the number of prime numbers less than a non-negative number, n.



## Java


### Code

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