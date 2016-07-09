# [83]Remove Duplicates from Sorted List

Given a sorted linked list, delete all duplicates such that each element appear only once.

For example,
Given 1->1->2, return 1->2.
Given 1->1->2->3->3, return 1->2->3.

## Code


### Python

```class Solution(object):
    def deleteDuplicates(self, head):
        if head == None:
            return []
        node = head
        while node != None:
            while(node.next != None and node.val == node.next.val):
                node.next = node.next.next
            node = node.next
        return head
        ```



