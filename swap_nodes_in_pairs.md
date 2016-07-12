# [24]Swap Nodes in Pairs

Given a linked list, swap every two adjacent nodes and return its head.

For example,
Given 1->2->3->4, you should return the list as 2->1->4->3.

Your algorithm should use only constant space. You may not modify the values in the list, only nodes itself can be changed.

## Code

### Python

```class Solution(object):
    def swapPairs(self, head):
        if head == None:
            return head
        start = ListNode(0)
        start.next = head
        node = start
        while node.next != None:
            if node.next.next != None:
                first = node.next
                second = node.next.next
                temp = second.next
                node.next = second
                second.next = first
                first.next = temp
                node = node.next.next
            else:
                return start.next
        return start.next
        ```



