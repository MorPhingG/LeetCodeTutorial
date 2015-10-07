# [13]Roman to Integer

Given a roman numeral, convert it to an integer.

Input is guaranteed to be within the range from 1 to 3999.


## Code


### Java

```
public class Solution {
    public int romanToInt(String s) {
        int sum = 0;
        int number = 0;
        int number1 = 0;
        for (int i=0;i<s.length();i++)
        {
            number1 = number;
            switch(s.charAt(i))
            {
                case 'I':number = 1;break;
                case 'V':number = 5;break;
                case 'X':number = 10;break;
                case 'L':number = 50;break;
                case 'C':number = 100;break;
                case 'D':number = 500;break;
                case 'M':number = 1000;
            }
            sum = sum+number;
            if(number>number1)
            sum = sum-2*number1;
        }
        return sum;
    }
}```

