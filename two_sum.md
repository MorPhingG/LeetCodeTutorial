# [1]Two Sum

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution.

Example:
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

## 思路
遍历，把需要找的值放入字典。

## Code

### Python
```
class Solution(object):
    def twoSum(self, nums, target):
        length = len(nums)
        dict_nums = {}
        for i in range(length):
            if nums[i] in dict_nums:
                return [dict_nums[nums[i]], i]
            else:
                dict_nums[target-nums[i]] = i
                ```





