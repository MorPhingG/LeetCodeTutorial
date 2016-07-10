# [19]Remove Nth Node From End of List

Given a linked list, remove the nth node from the end of list and return its head.

For example,

   Given linked list: 1->2->3->4->5, and n = 2.

   After removing the second node from the end, the linked list becomes 1->2->3->5.
Note:
Given n will always be valid.
Try to do this in one pass.

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



