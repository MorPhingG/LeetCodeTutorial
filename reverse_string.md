# [344]Reverse String

Write a function that takes a string as input and returns the string reversed.

Example:
Given s = "hello", return "olleh".

## Code

### Java
```public class Solution {
    public String reverseString(String s) {
        char[] sArray = s.toCharArray();
        int left = 0, right = s.length()-1;
        while(left < right){
            char temp = sArray[left];
            sArray[left] = sArray[right];
            sArray[right] = temp;
            left++;
            right--;
        }
        return new String(sArray);
    }
}
```




