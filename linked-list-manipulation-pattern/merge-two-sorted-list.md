# Merge-Two Sorted List Pattern

## Observations

1. [Merge Two sorted list](https://leetcode.com/problems/merge-two-sorted-lists/description/) - Merge the two sorted lists.
2. [Merge K sorted lists](https://leetcode.com/problems/merge-k-sorted-lists/description/) - Given K sorted linked lists, merge them in sorted order


Point to observe before <u>*applying merge-two sorted list pattern*</u> is just **merge n sorted linked list as simple as that**.

## What Is Merge-Two Sorted List Pattern ?

It is a pattern to merge the given n number of lists with O(1) auxillary space.

## Approaches

1. Merge Sort Approach

```javascript
1. Store all the elements from given linked lists into a new linked list.
2. Sort them using merge sort and return the new linked list.
```

2. Iterative Approach

```javascript
1. Use two pointers to point to the head of two linked lists out of given n linked lists.
2. Compare the two pointers value, using head.next of each pointer.
3. Init a new dummy node to create the merge linked list.
4. If pointer1.next.value >= pointer2.next.value then dummy.next = pointer2.next.value && pointer2.next = pointer.next.next else dummy.next=pointer1.next.value && pointer1.next.next. Make sure to check if pointer1/pointer2.next.next value exists before changing the pointers' head value.
5. dummy = dummy.next
6. If any of two linked lists are empty then return all the elements from other linked list as it is by connecting them to dummy.next.
7. End.
```

![alt text](/assets/Merge_2_Linked_Lists_Pattern.png)