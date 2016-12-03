# [118]Pascal's Triangle

Given numRows, generate the first numRows of Pascal's triangle.

For example, given numRows = 5,
Return

[
     [1],
    [1,1],
   [1,2,1],
  [1,3,3,1],
 [1,4,6,4,1]
]

## 思路
边缘的1直接插入，而中间的元素由上一行两个相加获得。


## Code

### Python
```
class Solution(object):
    def generate(self, numRows):
        if numRows == 0:
            return []
        if numRows == 1:
            return [[1]]
        result = [[] for i in range(numRows)]
        result[0] = [1]
        for i in range(1, numRows):
            for j in range(i+1):
                if j == 0 or j == i:
                    result[i].append(1)
                else:
                    result[i].append(result[i-1][j-1]+result[i-1][j])
        return result
        ```




