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
   
   
## Code

### Go

```func titleToNumber(s string) int {
	result := 1
	length := len(s)
	result = result + int(s[0]-'A')
	for i := 1; i < length; i++ {
		result = result*26 + int(s[i]-'A') + 1
	}
	return int(result)
}
```



