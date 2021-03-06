# [102]Binary Tree Level Order Traversal

Given a binary tree, return the level order traversal of its nodes' values. (ie, from left to right, level by level).

For example:
Given binary tree [3,9,20,null,null,15,7],
    3
   / \
  9  20
    /  \
   15   7
return its level order traversal as:
[
  [3],
  [9,20],
  [15,7]
]

## 思路
迭代，每次都记录当前层的树，根据该层得到下一层。

## Code

### Python
```
class Solution(object):
    def levelOrder(self, root):
        current_level, result = [root], []
        while current_level and root:
            result.append([leaf.val for leaf in current_level])
            current_level = [next for leave in current_level for next in (leave.left, leave.right) if next]
        return result
        ```



