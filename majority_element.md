# [169]Majority Element

Given an array of size n, find the majority element. The majority element is the element that appears more than ⌊ n/2 ⌋ times.

You may assume that the array is non-empty and the majority element always exist in the array.

## Code

### Python

```class Solution(object):
    def majorityElement(self, nums):
        numsDict = {}
        length = len(nums)
        for key in nums:
            if numsDict.__contains__(key):
                numsDict[key] += 1
            else:
                numsDict[key] = 1
            if numsDict[key] > length/2:
                return key
                ```



