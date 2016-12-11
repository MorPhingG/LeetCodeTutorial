# \[152\]Maximum Product Subarray

Find the contiguous subarray within an array \(containing at least one number\) which has the largest product.

For example, given the array`[2,3,-2,4]`,  
the contiguous subarray`[2,3]`has the largest product =`6`.

## 思路

动态规划， 每次迭代存一个最大值和最小值。

## Code

### Python

```
class Solution(object):
    def maxProduct(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        minTemp = nums[0]
        maxTemp = nums[0]
        Max = nums[0]
        for i in range(1, len(nums)):
            minTemp, maxTemp = min(nums[i], minTemp*nums[i], maxTemp*nums[i]), max(nums[i], maxTemp*nums[i], minTemp*nums[i])
            Max = max(maxTemp, Max)
        return Max
```

Runtime: 49ms

