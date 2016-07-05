# [349]Intersection of Two Arrays


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



