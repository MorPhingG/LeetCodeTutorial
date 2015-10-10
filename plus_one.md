# [66]Plus One

Given a non-negative number represented as an array of digits, plus one to the number.

The digits are stored such that the most significant digit is at the head of the list.

## Code

### Java

```
public class Solution {
    public int[] plusOne(int[] digits) {
        if (digits==null || digits.length == 0)
        return digits;
        int i=digits.length-1;
        while(i>=0)
        {
            if(digits[i]<9)
            {
                digits[i]=digits[i]+1;
                return digits;
            }
            else
            {
                digits[i]=0;
                i--;
            }
        }
        int [] Newdigits = new int[digits.length+1];
        Newdigits[0]=1;
        return Newdigits;
        }
}
```