# [257]Binary Tree Paths


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



