# Plus One Pattern

## Observations

1. [Multiply string](https://leetcode.com/problems/multiply-strings/description/) - Multiply the integer in two strings handling the carry over.
2. [Add to array form of integer](https://leetcode.com/problems/add-to-array-form-of-integer/description/) - Add two integers in given two strings without converting it into integer from string.

Keywords to observe before <u>*applying plus one pattern*</u> is **"simply which involves addition or multiplication which can result into handling carry over. Hence, increasing the length of array/string by one or more".**

It is just an oldschool way of adding two numbers on paper.

## What Is Plus One Pattern ?

It is a pattern of array which simulates the addition of two integers on paper.

![alt text](/assets/Plus_one_Pattern.png)

## Approach

```javascript
1. Use two pointers to iterate over two given strings of integers from rightmost and find longest string out of two. carry_over = 0.
2. Add the current pointers and carry_over and check the sum.
3. If sum >= 10; then replace the digit in longest string at current index of the pointer with value of sum - 10 and put carry_over = 1
4. Else, carry_over = 0 and replace the digit in longest string at current index of pointer with sum.
5. Increment the two pointers to its left index. And repeat step 2 - 4.
6. After the iteration is over depending upon the shortest length of the string, check the value of carry_over.
7. If the value == 1, then increment the value on next left index of longest string.
8. In doing so, keep checking where the sum on left index becomes greater than or equal to 10. If so, then keep incrementing the value on its next left index of longest string until the carry_over != 0.
9. Edge case could be when iteration is complete but we still have a carry_over = 1, then create a new array of length = longest string length + 1. Put 1 at index 0 and copy paste the element from the longest string at the remaining empty index of the new array.
```

## Properties

1. Time Complexity: O(N)
2. Space Complexity: O(1) for average cases, O(N) for the worst case (input is all 9s)