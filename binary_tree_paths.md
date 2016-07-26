# [257]Binary Tree Paths

Given a binary tree, return all root-to-leaf paths.

For example, given the following binary tree:

   1
 /   \
2     3
 \
  5
All root-to-leaf paths are:

["1->2->5", "1->3"]

## 思路
难以理解，日后再战

## Code

### Python

```class Solution:
    def binaryTreePaths(self, root):
        if root == None:
            return []
        return [str(root.val) + "->" + path
                for kid in (root.left, root.right) if kid
                for path in self.binaryTreePaths(kid)] or [str(root.val)]
                ```



