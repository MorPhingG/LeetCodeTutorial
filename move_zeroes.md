# Move Zeroes

Given an array nums, write a function to move all 0's to the end of it while maintaining the relative order of the non-zero elements.

For example, given nums = [0, 1, 0, 3, 12], after calling your function, nums should be [1, 3, 12, 0, 0].

Note:
1:You must do this in-place without making a copy of the array.
2:Minimize the total number of operations.

## 思路
用多个指针指向数组中的元素，然后遍历

## Code

## Python
```
class Solution(object):
    def moveZeroes(self, nums):
        """
        :type nums: List[int]
        :rtype: void Do not return anything, modify nums in-place instead.
        """
        index = 0
        for i in range(len(nums)):
            if nums[i] != 0:
                nums[i], nums[index] = 0, nums[i]
                index += 1
                ```
Runtime: 89ms

### Java
```
public class Solution {
    public void moveZeroes(int[] nums) {
        int point1=0;
        int point2=1;
        int temp=0;
        while(point2<nums.length)
        {
            if(nums[point1]!=0)
            {
                point1++;
            }
            else if (nums[point2]!=0)
            {
                temp=nums[point1];
                nums[point1]=nums[point2];
                nums[point2]=temp;
                point1++;
            }
            point2++;
        }
    }
}```