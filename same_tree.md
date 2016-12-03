# [100]Same Tree

Given two binary trees, write a function to check if they are equal or not.

Two binary trees are considered equal if they are structurally identical and the nodes have the same value.

## 思路
迭代，依次判断每个子树看两棵树是否相同。

## Code

### Java
```
public class Solution {
    public boolean isSameTree(TreeNode p, TreeNode q) {
        if((p==null) && (q==null))
            return true;
        if((p==null) || (q==null))
            return false;
        if((p.val==q.val) && isSameTree(p.left, q.left) && isSameTree(p.right, q.right))
            return true;
        else
            return false;
    }
}```



