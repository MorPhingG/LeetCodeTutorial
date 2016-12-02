# [27]Remove Element

Given an array and a value, remove all instances of that value in place and return the new length.

The order of elements can be changed. It doesn't matter what you leave beyond the new length.

Example:
Given input array nums = [3,2,2,3], val = 3

Your function should return length = 2, with the first two elements of nums being 2.

## 思路
对比每个元素和删除值，相同则删除

## Code

### Python
```
class Solution(object):
    def removeElement(self, nums, val):
        """
        :type nums: List[int]
        :type val: int
        :rtype: int
        """
        index = 0
        for i in range(len(nums)):
            if nums[i] != val:
                nums[index] = nums[i]
                index += 1
        return index
        ```
Runtime: 46ms

### Java

```
public class Solution {
    public int removeElement(int[] nums, int val) {
        int length=0;
        for (int i=0;i<nums.length;i++)
        {
            if(nums[i]!=val)
            {
                nums[length]=nums[i];
                length++;
            }
        }
        return length; 
    }
}
```