# [7]Reverse Integer

Reverse digits of an integer.

Example1: x = 123, return 321
Example2: x = -123, return -321

## Code

### Java
```
public class Solution {
    public int reverse(int x) {
        long sum = 0;
        while (x>0)
        {
            sum = sum*10 + x%10;
            x = x/10;
            if(x == 0)
                if(sum>java.lang.Integer.MAX_VALUE)
                return 0;
                else 
                return (int)sum;
        }
        while (x<0)
        {
            sum = sum*10 - x%10;
            x = x/10;
            if(x == 0)
                if(sum>java.lang.Integer.MAX_VALUE)
                return 0;
                else
                return (int)-sum;
        }
        return x;
    }
}```

