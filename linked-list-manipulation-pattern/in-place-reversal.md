# In-place Reversal Pattern

## Observations

1. [Reverse the linked list](https://leetcode.com/problems/reverse-linked-list-ii/) - Reverse the linked list inside a given range positions.
2. [Remove duplicates from sorted list](https://leetcode.com/problems/remove-duplicates-from-sorted-list-ii/description/) - Remove all the duplicates from the given linked list.

Each questions mentioned above, follows a pattern which involves just <u>*a linked list*</u> and tell you to reverse the list or remove the duplicates from the sorted linked list. Indirectly, it says to in-place reversal using insertion or deletion by keeping track of current, prev and next node. As insertion and deletion is just of O(1) time complexity.

Keywords to observe before <u>*applying in-place reversal pattern*</u> are **reverse the linked list, remove duplicated from the sorted linked list**.

## What Is In-place Reversal Pattern ?

It is a pattern to reverse a linked list without using extra space.

## Approaches

1. Stack Approach

```javascript
1. Use a stack to store the linked list elements.
2. Pop each element of the stack one by one, to replace the existing linked list.
3. Once the stack is empty, return the new linked list using its head.
```

2. Recursion Approach

```javascript
1. Store the head address in a temp value.
2. Start the recursion on first node by replacing next address to null.
3. Use recursion, to change the existing node next address with previous one.
4. Once, come to an end replace the head next address with that node.
```

3. In-place reversal.

```javascript
1. Start on the head or from where it is mentioned in the question.
2. Use prev, current and next variable to store the prev, current and next node value.
3. Once you have prev, current and next variable value, replace the current value, next address with the prev one while changing the head address to current value. Don't consider head value in any of the variable.
4. Once you find the next variable value to null, return the reversed linked list.
```
**Note:- In-place reversal pattern is just a insertion and deletion thing in a linked list as this method is just O(1) time complexity.**
