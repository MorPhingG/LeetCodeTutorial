# [217]Contains Duplicate

Given an array of integers, find if the array contains any duplicates. Your function should return true if any value appears at least twice in the array, and it should return false if every element is distinct.

## 思路
一种方法是比列表和集合的长度，还一种是用字典。

## Code

### Python
Solution1:
```
class Solution(object):
    def containsDuplicate(self, nums):
        numsDict = {}
        for key in nums:
            if numsDict.__contains__(key):
                return True
            else:
                numsDict[key] = 1
        return False
        ```
        
Solution2:
```
class Solution(object):
    def containsDuplicate(self, nums):
        return not len(set(nums)) == len(nums)
        ```




