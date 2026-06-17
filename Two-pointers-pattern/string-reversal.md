# String Reversal

## Observations

1. [Reverse vowels of a string](https://leetcode.com/problems/reverse-vowels-of-a-string/description/) - Reverse only the vowels in the string
2. [Reverse the string](https://leetcode.com/problems/reverse-string/description/) - Reverse the characters in the string
3. [Reverse words in a string](https://leetcode.com/problems/reverse-words-in-a-string/description/) - Reverse the word in a string (not characters but words).[<sup>1</sup>](#questions-to-think)

Each question revolve around word "reverse".

Keywords to observe before *<u style="color: cadetblue">applying string reversal</u>* :- **"Reversing the element"**, **"Reverse the specified element like vowels or consonant"**


## What Is String Reversal Pattern ?

<span style="color: green">String Reversal pattern</span> is a technique about using <span style="color: red">two markers (pointers) to iterate characters from both sides and replace it with each other (in-place modification, if your language allows) in a string.</span>

![alt text](/assets/String_Reversal_Pattern.png)

## Its function and edge-cases

### How it works
```javascript
- Place one pointer (left) at the beginning and another (right) at the end.
- While left is less than right, swap the characters at these positions.
- Move left forward and right backward.
- Repeat until the pointers meet or cross.
```

### Handling edge cases

```javascript
- For Empty String, check if the length is 0; then return
- For Selective Reversal, be careful with conditions—e.g., only swap vowels, or reverse every k characters.
```

## Properties

1. **Efficiency** - Each character is visited at most once, so the time taken is proportional to the length of the string—**O(n)**, where n is the number of characters. Think of reading a book from both ends at the same time; you finish in half the time compared to reading from just one end.
2. **Space Complexity** - Since we’re modifying in place, we use only a constant amount of extra space **—O(1)**. No matter how long the string is, we only need a few variables for the pointers.
3. **Mathematical Foundation** - The pattern leverages the **symmetry of reversal—swapping** the i-th and (n-1-i)-th elements. This ensures each pair is handled exactly once.


## Questions to think
1. What if your programming language allows in place modification then how will you reverse the word in a string? Think about your text editor, how does it handle the insertion of character in a mid document? There are some algorithms. Search for it.