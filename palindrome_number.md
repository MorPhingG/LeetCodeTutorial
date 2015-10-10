# [9]Palindrome Number

Determine whether an integer is a palindrome. Do this without extra space.

## Code

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