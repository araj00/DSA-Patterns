# Expanding From Centre Pattern

## Observations

1. [Palindromic Substring](https://leetcode.com/problems/palindromic-substrings/description/) - Find the palindromic substring in a string.
2. [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/) - Find the longest palindromic substring

Keywords to observe before <u>*applying expanding from centre*</u> are **Palindrome + substring**

---

## What Is Expanding From Centre Pattern ?

It is a technique about using two pointers to find varities of palindromic substring in a string.

![alt text](/assets/Expanding_From_Centre_Pattern.png)

## Its function and edge-cases

### How it works
```javascript
- Identify all possible centres:- For a string of length n, there are n single-character centers (for odd-length palindromes) and n-1 pairs of adjacent characters (for even-length palindromes)
- For counting palindromic substrings, increment a counter each time you find one.
- For finding the longest palindrome, keep track of the maximum length and starting index.
```

### Handling edge cases

```javascript
- Single-character strings are always palindromes.
- Empty strings have zero palindromic substrings.
```

## Properties :-

1. **Efficiency** - For a string of length n, there are 2n-1 possible centers (n single characters + n-1 between characters). For each center, in the worst case, we expand up to n/2 steps. So, the total is O(n²).

2. **Space Complexity** - Typically O(1) extra space (unless you store all substrings), since we only use pointers and counters.

3. **Function** : The symmetry of palindromes means that checking characters equidistant from the center is sufficient.