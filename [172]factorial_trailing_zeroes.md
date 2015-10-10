# [172]Factorial Trailing Zeroes

Given an integer n, return the number of trailing zeroes in n!.

Note: Your solution should be in logarithmic time complexity.

## Code

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