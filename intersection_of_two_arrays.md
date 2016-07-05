# [349]Intersection of Two Arrays

Given two arrays, write a function to compute their intersection.

Example:
Given nums1 = [1, 2, 2, 1], nums2 = [2, 2], return [2].

Note:
Each element in the result must be unique.
The result can be in any order.

## Code

### Java

### Python
Solution1:
```class Solution(object):
    def intersection(self, nums1, nums2):
        result = []
        for num in set(nums1):
            if num in nums2:
                result.append(num)
        return result
        ```
Solution2:
```class Solution(object):
    def intersection(self, nums1, nums2):
        return [num for num in set(nums1) if num in nums2]
        ```



