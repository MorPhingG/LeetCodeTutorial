# [206]Reverse Linked List

Reverse a singly linked list.

## Code

### Python

```
class Solution(object):
    def reverseList(self, head):
        if head == None or head.next == None:
            return head
        node1 = head
        node2 = head.next
        node1.next = None
        while node2 != None:
            temp = node2.next
            node2.next = node1
            node1 = node2
            node2 = temp
        return node1
        ```



