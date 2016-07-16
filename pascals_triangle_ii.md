# [119]Pascal's Triangle II

Given an index k, return the kth row of the Pascal's triangle.

For example, given k = 3,
Return [1,3,3,1].

Note:
Could you optimize your algorithm to use only O(k) extra space?

## Code

### Python

```class Solution(object):
    def getRow(self, rowIndex):
        row = [1]
        for i in range(rowIndex):
            row = [u+v for u,v in zip(row+[0], [0]+row)]
        return row
        ```





