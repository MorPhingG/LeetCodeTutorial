# [268]Miss Number

Given an array containing n distinct numbers taken from 0, 1, 2, ..., n, find the one that is missing from the array.

For example,
Given nums = [0, 1, 3] return 2.

Note:
Your algorithm should run in linear runtime complexity. Could you implement it using only constant extra space complexity?

## 思路

直接用求和公式求和然后减去数列总和即可得到丢失的数


## Code


### Java

```
public class Solution {
    public int missingNumber(int[] nums) {
        int num=0;
        int sum=0;
        if(nums.length==0 || nums==null)
        return -1;
        for (int i=0;i<nums.length;i++)
        {
            sum=sum+nums[i];
        }
        return (nums.length+1)*nums.length/2-sum;
    }
}```