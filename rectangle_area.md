# [223]Rectangle Area

Find the total area covered by two rectilinear rectangles in a 2D plane.

Each rectangle is defined by its bottom left corner and top right corner as shown in the figure.

Rectangle Area
Assume that the total area is never beyond the maximum possible value of int.

## 思路
两矩形重叠的区域的边长可用两右侧最小减左侧最大获得，另外小于0时应取0

## Code

### Python
```
class Solution(object):
    def computeArea(self, A, B, C, D, E, F, G, H):
        """
        :type A: int
        :type B: int
        :type C: int
        :type D: int
        :type E: int
        :type F: int
        :type G: int
        :type H: int
        :rtype: int
        """
        return (C-A)*(D-B)+(G-E)*(H-F) - max(min(C,G)-max(A,E),0)*max(min(D,H)-max(B,F),0)
        ```



