# [231]Power of Two

Given an integer, write a function to determine if it is a power of two.

## Code

### 

```
public class Solution {
    public boolean isPowerOfTwo(int n) {
        int b = n & n-1;
        if(n>0 && b==0)
        return true;
        else 
        return false;
    }
}
```