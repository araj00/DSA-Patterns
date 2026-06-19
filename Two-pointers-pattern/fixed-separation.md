# Fixed Separation Pattern

## Observations

1. [Remove Nth node from the linked list](https://leetcode.com/problems/remove-nth-node-from-end-of-list/description/) - Remove Nth node from the end of the linked list 
2. [Delete the middle node of the linked list](https://leetcode.com/problems/delete-the-middle-node-of-a-linked-list/description/) - Remove the middle node of the linked list.

Each questions mentioned above, follows some patterns which are:-

1. Remove the Nth node from end of the linked list, need to maintain Nth distance from the end.
2. Remove the middle node of the linked list. Maintain a separate distance between nodes such that at the end, fast pointer comes to end then slow pointer should be at middle of the node.

Keywords to observe before <u>*applying fixed-separation*</u> is a fixed separation to find the position with reference to a point(usually from end).

---

## What Is Fixed-Separation Pattern ?

It is a technique about using two markers (fast and slow pointers) to maintain a fixed separation to find the position in an array or linked list.

![alt text](/assets/Fixed_Separation_Pattern.png)

## Its function and edge-cases

### How it works
```javascript
- Set up two pointers: Both at the head.
- Advance the fast pointer: Move it N steps ahead (for “Nth from end” problems).If you’re finding the middle, move fast pointer two steps for every one step of slow pointer.
- Move both pointers together: Keep going until the fast pointer reaches the end.
```

### Handling edge cases

```javascript
- Before proceeding, always take care of head of the linked list as per the given question condition so we can have correct output.
- Always look for when fast pointer comes to end before slow pointer objective is end i.e finding the position of the index or node in the list i.e what if the linked list is one node only. 
- Always check for null pointers to avoid crashes i.e what if the linked list is empty.
```

## Properties :-

1. **Efficiency**:- Time Complexity O(n). You only walk through the list once, like reading a book cover to cover.

2. **Space Complexity** - Space Complexity O(1). No extra memory, just two pointers.