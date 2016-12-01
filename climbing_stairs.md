# [70]Climbing Stairs

You are climbing a stair case. It takes n steps to reach to the top.

Each time you can either climb 1 or 2 steps. In how many distinct ways can you climb to the top?

## 思路
f(n) = f(n-1)+f(n-2)

## Code

### Python

```
memory = {}
memory[0] = 0
memory[1] = 1
memory[2] = 2
class Solution(object):
    def climbStairs(self, n):
        if n in memory:
            return memory[n]
        first = self.climbStairs(n-1)
        memory[n-1] = first
        second = self.climbStairs(n-2)
        memory[n-2] = second
        return first + second
```



