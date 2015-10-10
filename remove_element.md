# [27]Remove Element

Given an array and a value, remove all instances of that value in place and return the new length.

The order of elements can be changed. It doesn't matter what you leave beyond the new length.

## 思路
对比每个元素和删除值，相同则删除


## Code


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