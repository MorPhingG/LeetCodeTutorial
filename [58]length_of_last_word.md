# [58]Length of last word

Given a string s consists of upper/lower-case alphabets and empty space characters ' ', return the length of last word in the string.

If the last word does not exist, return 0.

Note: A word is defined as a character sequence consists of non-space characters only.

For example, 
Given s = "Hello World",
return 5.


## 思路
从字符串的最后往前搜索， 先确定单词结尾的位置，再确定开头的位置，
然后求出长度



## Code


### Java
```
public class Solution {
    public int lengthOfLastWord(String s) {
        if(s==null || s.length()==0)
        return 0;
        int flag=0;
        int end=0;
        for (int i=s.length()-1;i>=0;i--)
        {
            if(s.charAt(i)!=' ' && flag==0)
            {
                flag=1;
                end=i;
            }
            if(s.charAt(i)==' ' && flag==1)
            return end-i;
        }
        if(flag==0)
        return 0;
        else
        return end+1;
    }
}```


