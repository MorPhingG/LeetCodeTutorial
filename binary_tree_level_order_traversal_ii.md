# [107]Binary Tree Level Order Traversal II

Given a binary tree, return the bottom-up level order traversal of its nodes' values. (ie, from left to right, level by level from leaf to root).

For example:
Given binary tree [3,9,20,null,null,15,7],
    3
   / \
  9  20
    /  \
   15   7
return its bottom-up level order traversal as:
[
  [15,7],
  [9,20],
  [3]
]

## 思路
先得到从上往下的结果，再反转。

## Code

### Python
```
class Solution(object):
    def levelOrderBottom(self, root):
        result, current_level = [], [root]
        while current_level and root:
            result.append([leave.val for leave in current_level])
            current_level = [next for leaf in current_level for next in (leaf.left, leaf.right) if next]
        n = 0
        length = len(result)
        while n<length/2:
            result[n], result[length-n-1] = result[length-n-1], result[n]
            n = n+1  
        return result
        ```



