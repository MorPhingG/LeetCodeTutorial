# [21]Merge Two Sorted Lists

Merge two sorted linked lists and return it as a new list. The new list should be made by splicing together the nodes of the first two lists.

## Code

### Python

```class Solution(object):
    def mergeTwoLists(self, l1, l2):
        if l1 == None:
            return l2
        if l2 == None:
            return l1
        node1 = l1
        node2 = l2
        if node1.val <= node2.val:
            newNode = ListNode(node1.val)
            node1 = node1.next
        else:
            newNode = ListNode(node2.val)
            node2 = node2.next
        head = newNode
        while node1 != None and node2 != None:
            if node1.val <= node2.val:
                newNode.next = node1
                node1 = node1.next
            else:
                newNode.next = node2
                node2 = node2.next
            newNode = newNode.next
        if node1 == None:
            newNode.next = node2
        else:
            newNode.next = node1
        return head
        ```



