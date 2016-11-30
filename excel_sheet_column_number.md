# [171]Excel Sheet Column Number

Related to question Excel Sheet Column Title

Given a column title as appear in an Excel sheet, return its corresponding column number.

For example:

    A -> 1
    B -> 2
    C -> 3
    ...
    Z -> 26
    AA -> 27
    AB -> 28 
   
## 思路
把问题当作26进制转10进制来做。
   
## Code

### Python
```
class Solution(object):
    def titleToNumber(self, s):
        """
        :type s: str
        :rtype: int
        """
        num = 0
        i = 0
        length = len(s)
        while i < length:
            num += 26**(len(s)-i-1)*(ord(s[i])-64)
            i += 1
        return num
        ```
Runtime: 36ms


### Go

```
func titleToNumber(s string) int {
	result := 1
	length := len(s)
	result = result + int(s[0]-'A')
	for i := 1; i < length; i++ {
		result = result*26 + int(s[i]-'A') + 1
	}
	return int(result)
}
```



