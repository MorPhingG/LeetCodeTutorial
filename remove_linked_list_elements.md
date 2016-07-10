# [203]Remove Linked List Elements

Remove all elements from a linked list of integers that have value val.

Example
Given: 1 --> 2 --> 6 --> 3 --> 4 --> 5 --> 6, val = 6
Return: 1 --> 2 --> 3 --> 4 --> 5

## 思路

当循环删节点时，要注意不要同时发生删除和右移

## Code

### Python

```
class Solution(object):
    def removeElements(self, head, val):
        if head == None:
            return []
        start = ListNode(0)
        start.next = head
        node = start
        while node.next != None:
            if node.next.val == val:
                node.next = node.next.next
            else:
                node = node.next
        return start.next
        ```



