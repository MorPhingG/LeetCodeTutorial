# [50]Pow(x, n)

Implement pow(x, n).

## Code

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