# [141]Linked List Cycle

Given a linked list, determine if it has a cycle in it.

## 思路
两个点，一快一慢，有环总能追上

## Code

### Python

```class Solution(object):
    def hasCycle(self, head):
        if head == None:
            return False
        fast = head
        slow = head
        while fast != None and fast.next != None:
            fast = fast.next.next
            slow = slow.next
            if fast == slow:
                return True
        return False
        ```






