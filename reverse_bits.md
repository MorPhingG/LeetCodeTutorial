# [190]Reverse Bits

Reverse bits of a given 32 bits unsigned integer.

For example, given input 43261596 (represented in binary as 00000010100101000001111010011100), return 964176192 (represented in binary as 00111001011110000010100101000000).

## 思路
不断移位，记住不要用乘除，不知道为什么


## Code


### Java

```
public class Solution {
    // you need treat n as an unsigned value
    public int reverseBits(int n) {
        int num=0;
        for (int i=0;i<32;i++)
        {
            num=num<<1 | n&1;
            n>>>=1;
        }
        return num;
    }
}```