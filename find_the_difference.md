# [389]Find the Difference

Given two strings s and t which consist of only lowercase letters.

String t is generated by random shuffling string s and then add one more letter at a random position.

Find the letter that was added in t.

Example:

Input:
s = "abcd"
t = "abcde"

Output:
e

Explanation:
'e' is the letter that was added.

## Code

### Python
```class Solution(object):
    def findTheDifference(self, s, t):
        """
        :type s: str
        :type t: str
        :rtype: str
        """
        if s == None:
            return t[0]
        Dict = {}
        for char in s:
            if char in Dict:
                Dict[char] += 1
            else:
                Dict[char] = 1
        for char in t:
            if char in Dict:
                if Dict[char] == 0:
                    return char
                else:
                    Dict[char] -= 1
            else:
                return char
        return False
        ```



