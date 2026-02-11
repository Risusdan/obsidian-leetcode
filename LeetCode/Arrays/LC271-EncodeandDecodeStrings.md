---
leetcode_number: 271
title: Encode and Decode Strings
difficulty: Medium
topic: Arrays
status: 🔴
date_attempted: 2026/2/11
date_solved:
time_complexity:
space_complexity:
---

# LC271 - Encode and Decode Strings

Encoding a list of strings into one single string and then decoding it back to the original list.

## Problem Link

- [LeetCode 271](https://leetcode.com/problems/encode-and-decode-strings/)

## Solution (Python)

You encode each string by adding its length in a fixed-width format, like 4 digits, followed by the string itself. This avoids delimiter conflicts because no special characters are needed. For example, to encode ["hello", "world"], you might produce "0005hello0005world". Then, decoding reads the first 4 digits ("0005"), extracts "hello", and moves on to the next. This ensures accurate decoding without delimiter issues.

```python

```

## Solution (C++) — Optional

```cpp

```

## Complexity Analysis

- **Time:**
- **Space:**

## Key Takeaways

-

## Related Problems

- [[]]

## Phase

- [[Phase2-CorePatterns]]
