# [453]Minimum Moves to Equal Array Elements

Given a non-empty integer array of size n, find the minimum number of moves required to make all array elements equal, where a move is incrementing n - 1 elements by 1.

Example:

Input:
[1,2,3]

Output:
3

Explanation:
Only three moves are needed (remember each move increments two elements):

[1,2,3]  =>  [2,3,3]  =>  [3,4,3]  =>  [4,4,4]

## 思路
设想最开始的列表里所有值都相同且为最小值，每有一个值加1，我们的输出就需要加1，故只要求每个值相比最小值增加了多少即可。

## Code

### Python
```
class Solution(object):
    def minMoves(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        m = min(nums)
        return sum(x-m for x in nums)
        ```



