# In-place Array Modification Pattern

## Observations

1. [Remove Element](https://leetcode.com/problems/remove-element/description/) - Remove the given element from the array.
2. [Remove duplicates from the element](https://leetcode.com/problems/remove-duplicates-from-sorted-array-ii/description/) - Remove the duplicates from the element such that at most 2 duplicates of a unique number can be preserved.
3. [Sort colors](https://leetcode.com/problems/sort-colors/description/) - Sort the 3 colors (Dutch Problem [<sup>1</sup>](#references) )

Each questions mentioned above, follows some patterns which are:-

1. Remove the elements from the array (By this, it just means that you have to move the unnecessary elements to the last so that required elements are at front).
2. Remove the duplicate from the array (same as above but with a twist that at most twice duplicate of a unique number can be preserved, rest of them are removed or can say put at last). 
3. Sort the elements (But, we sure that number of unique elements should be just 2-4 otherwise <u>use sorting algorithm</u>)

Points to observe before <u>*applying in-place modification*</u> are:-
1. **move element, remove the element.**
2. **remove duplicates.**
3. **sort the elements(2-4 unique element).**
4. **swap the elements with true one**.

Note: <u>All of the above questions, just imply one thing if the elements are not at its specified place then just swap it with its true one. So, just before solving anything like this, ask are you going to swap the elements in the array. 

If it is then in-place array might be a great solution.</u>

---


## What Is In-place Array Modification Pattern ?

It is a technique about using two markers (fast and slow pointers) to iterate over elements from starting and making sure that fast pointers are ahead or together of slow pointers and when fast pointers find its keeper and swap it with the slow pointers.

![alt text](/assets/In_Place_Array_Pattern.png)

## Its function and edge-cases

### How it works
```javascript
- Start both pointers at the beginning.
- Move the fast pointer through each element.
- When the fast pointer finds a "keeper" (e.g., non-zero, unique, even), copy or swap it to the position marked by the slow pointer.
- Advance the slow pointer only when you place a valid element.
```

### Handling edge cases

```javascript
All elements are equal - If that is the case then fast pointer will come out of the loop and function returns
```

## Properties :-

1. **Efficiency**

- O(n) time: each element is checked once.
- Just one pass iteration

2. **Space Complexity**

- O(1) space: only pointers used.

3. **Function** : The fast pointer scouts for valid elements; the slow pointer places them

---

# References :-

1. [Dutch Flag problem](https://neetcode.io/solutions/sort-colors)