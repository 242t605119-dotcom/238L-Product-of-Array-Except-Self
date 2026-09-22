# LeetCode 238 - Product of Array Except Self

## Problem

Given an integer array `nums`, return an array `answer` such that:

```text
answer[i] = product of all nums[j] where j != i
```

The solution must run in `O(n)` time and should not use division.

## Example

### Input

```text id="y5j2pv"
nums = [1,2,3,4]
```

### Output

```text id="qj8v1k"
[24,12,8,6]
```

## Approach

For every position, we need the product of all elements before it and all elements after it.

We calculate these using two passes:

* First pass calculates the prefix product.
* Second pass calculates the suffix product and multiplies it with the prefix product.

This avoids using division.

## Algorithm

1. Create a result array filled with `1`.
2. Traverse from left to right and store the product of elements before each index.
3. Traverse from right to left.
4. Maintain a suffix product.
5. Multiply the suffix product with the corresponding result value.
6. Return the result array.

## Complexity

* Time Complexity: `O(n)`
* Space Complexity: `O(1)` extra space

The output array is not counted as extra space.

## Language

Python

## LeetCode

Problem: 238 - Product of Array Except Self

## Author

**T.Nandhini**
