# Fast and Slow Pointer (Hare-Tortoise Problem)

## Observations

1. [Linked list cycle](https://leetcode.com/problems/linked-list-cycle/description/) - Detect a cycle in a linked list
2. [Happy Number](https://leetcode.com/problems/happy-number/description/) - Find whether the given number is a happy number i.e sum of square of every digits in a number produces the same input number or not after some repeting steps. Basically, detecting a loop or cycle.
3. [Find the duplicate number](https://leetcode.com/problems/find-the-duplicate-number/description/) - Find the single duplicate number in a given array of numbers.

Keywords to observe before *<u>applying fast and slow pointer</u>* :- **"finding a duplicate"**, **"Cycle or loop detection"**


## What Is Fast and Slow Pointer Pattern ?

Fast and Slow pointer is a technique about finding detection cycle or loop using two markers (pointers) which iterate over the given input array with two different speeds, usually double speed to one another. If there is a cycle detection then they will meet at same point or index otherwise fast pointer will exit out of the array.

![alt text](/assets/Fast_and_Slow_Pointer_Pattern.png)

## Its function and edge-cases

### How it works
```javascript
- Two Pointers: You use two variables (pointers), often called slow and fast.
- Different Speeds: The slow pointer moves one step at a time, while the fast pointer moves two steps at a time.
- Meeting Point: If there's a cycle, the fast pointer will eventually "lap" the slow pointer, and both will point to the same place.
- No Cycle: If there's no cycle, the fast pointer will reach the end (null or out of bounds) before the slow pointer.
```

### Handling edge cases

```javascript
- Empty Structure: If the list or array is empty, there's no cycle.
- Single Element: Usually, no cycle unless it points to itself.
- Self-Loop: If the first element points to itself, the pointers will meet immediately.

```

## Properties

1. Time Complexity: Usually O(N), where N is the number of elements. Both pointers traverse the structure, but since the fast pointer moves twice as fast, the number of steps is still proportional to N.
2. Space Complexity: O(1), because you only use two pointers, no extra data structures.
3. Mathematical Foundation - The pattern works because, in a cycle, the distance between the two pointers reduces by one at each step (since fast moves two steps and slow one). Eventually, the gap closes, and they meet.