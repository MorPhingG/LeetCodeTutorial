# [234]Palindrome Linked List

Given a singly linked list, determine if it is a palindrome.

Follow up:
Could you do it in O(n) time and O(1) space?

## 思路
先把链表分成两半，将后半部分反转，然后判断这两部分是否相同。

## Code

### Python

```
class Solution(object):
    def isPalindrome(self, head):
        if head == None or head.next == None:
            return True
        fast = head
        slow = head
        while fast != None and fast.next != None:
            fast = fast.next.next
            slow = slow.next
        if fast:
            slow = slow.next
        second = slow.next
        slow.next = None
        while second != None:            
            temp = second.next
            second.next = slow
            slow = second
            second = temp
        while slow != None:
            if head.val != slow.val:
                return False
            else:
                head = head.next
                slow = slow.next
        return True
        ```



