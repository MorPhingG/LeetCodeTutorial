# [219]Contains Duplicate II

Given an array of integers and an integer k, find out whether there are two distinct indices i and j in the array such that nums[i] = nums[j] and the difference between i and j is at most k.

## Code

### Python

```class Solution(object):
    def containsNearbyDuplicate(self, nums, k):
        numsDict = {}
        length = len(nums)
        for i in range(length):
            if numsDict.__contains__(nums[i]) and i - numsDict[nums[i]] <= k:
                return True
            else:
                numsDict[nums[i]] = i
        return False
        ```



