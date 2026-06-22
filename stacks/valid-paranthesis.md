# Valid Paranthesis Pattern

## Observations

1. [Valid Paranthesis](https://leetcode.com/problems/valid-parentheses/description/) - State whether the given input is a valid paranthesis true or not.
2. [Minimum number of swaps to make the string balanced](https://leetcode.com/problems/minimum-number-of-swaps-to-make-the-string-balanced/description/) - Minimum number of swaps to make the string balanced and valid.
3. [Minimum remove to make valid paranthesis](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/description/) - Make a valid paranthesis in a string by minimum removal of it.

Keywords to observe before <u>*applying valid paranthesis pattern*</u> are **make a valid paranthesis through removal, swapping**.

## What Is Valid Paranthesis Pattern ?

It is a pattern in which stack data structure gets used to make the validation on balanced paranthesis in the string.


![alt text](/assets/Valid_paranthesis_Pattern.png)

## Approach

```javascript
1. Initialise an empty stack.
2. Put the element on the top of the stack.
3. Before pushing it on the stack, check with the top element.
4. If it makes the valid pair with opening and closing bracket. Then pop that.
5. Otherwise, push that on top stack.
6. After processing all elements on to the stack, take a call to calculate the output like for valid paranthesis, check if the length of the stack is empty or not, in swapping string question look for the poping up the paranthesis after swapping as there could be chance after swapping that it becomes balanced or valid paranthesis.
```