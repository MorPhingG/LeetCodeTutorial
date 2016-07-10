# [19]Remove Nth Node From End of List


## Code


### Python

```
class Solution(object):
    def removeNthFromEnd(self, head, n):
        if head == None:
            return []
        start = ListNode(0)
        start.next = head
        node1 = start
        node2 = start
        num = 0
        while num < n:
            node1 = node1.next
            n -= 1
        while node1.next != None:
            node1 = node1.next
            node2 = node2.next
        node2.next = node2.next.next
        return start.next
        ```



