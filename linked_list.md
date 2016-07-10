# Linked List

Easy:
1:很多时候在head前面加一个start节点比较好，因为满足了链表只有一个head节点并需要删除的情况
2:删除下一节点通常只需要node.next = node.next.next就行，如果是删除当前节点的话，可以将下一节点赋值到当前节点，node.val = node.next.val，之后再进行删除
3:循环删除多个节点时，要注意当前循环删除节点后不要再执行节点位移了，否则相当于直接移了两次