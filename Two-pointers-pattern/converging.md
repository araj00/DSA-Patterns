# Converging Pattern

## Observations

1. [Boats to save people](https://leetcode.com/problems/boats-to-save-people/description/) - Find the minimum number of boats required to carry every person; given a weight limit that a boat can carry of at most 2 persons.  
2. [3 Sum closest](https://leetcode.com/problems/3sum-closest/description/) - Find three integers in an array whose sum is closest to a given target number and return that sum.
3. [2 Sum](https://leetcode.com/problems/two-sum/description/) - Find two indices in an array such that the numbers at those indices add up to a specific target.
4. [3 Sum](https://leetcode.com/problems/3sum/description/) - Find all unique triplets in an array that sum up to exactly zero.
5. [4 Sum](https://leetcode.com/problems/4sum/description/) - Find all unique quadruplets in an array that sum up to a specific target number.

Each questions mentioned above, follows a single pattern directly or indirectly which are:-

1. Find those pairs that can be accommodated on a single boat without overload.
2. Find that 3 numbers which have the closest sum to a given value. 
3. Find those pairs whose sum is a given target, avoiding duplicates
4. Find those triplets whose sum is zero, with no duplicates
5. Find those quadruplets whose sum is a given target, avoiding duplicates.

Points to observe before <u style="color: cadetblue">*applying converging pattern*</u> are **key-pairs, target, and adding up to the target**.

Whenever the questions indicate finding pairs, it could be double, triplets or quadruplets which will be based upon some target that those values add up to.

Converging pattern can be one of the solution.

---


## What Is Converging Pattern ?

Converging pattern is a technique about using two markers (pointers) to scan a sorted array from both ends toward the center.

![alt text](/assets/Converging_Pattern.png)

## Its function and edge-cases

<u style="color: cadetblue">**Conditions for converging pattern**</u> :- A given array should be in sorted array.

### How it works
```javascript
- Left Pointer: Starts at the beginning (smallest value).
- Right Pointer: Starts at the end (largest value).
- At each step, you check the sum (or another condition) of the values at both pointers.
- If the sum is too small, move the left pointer right (to a larger value).
- If the sum is too big, move the right pointer left (to a smaller value).
- If the sum matches the target, you've found a solution!
```

### Handling edge case of duplicacy pairs

```javascript
- After finding your solution and shifting the pointers inward, check for the previous value and current value of each pointer.
- If the values are same as previous value then iterate over the next value from both ends. This avoid the duplicacy in the solution.
- In case of left_pointer == right_pointer and it satisfies the target then consider it.  
```

## Properties

1. **Efficiency**

- Instead of checking every pair (which would be O(n²) time), you only scan the array once—O(n) time.
- Think of it like reading a book from both ends at once, meeting in the middle, instead of reading every page twice.

2. **Space Complexity**

- Usually O(1) extra space, since you’re just moving pointers around in the existing array.

3. Mathematical Foundation:

- The sorted order guarantees that moving pointers inwards will always bring you closer to (or further from) the target in a predictable way.
- This predictability is what makes the method so powerful.

---

## Beyond Pairs:-

- For problems like "3Sum," you can fix one pointer and use two more to find pairs, extending the idea to triplets. Same with 4 sum, fix 2 pointers, so that instead of O(n4), it will use O(n3).