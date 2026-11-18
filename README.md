# Why Hash Maps Can Turn an O(n²) Solution into O(n)

When solving array problems, a brute-force approach is often the first solution that comes to mind. But sometimes, we can improve it significantly by using a hash map.

Let's understand this with the Two Sum problem.

## Problem

Given an array of integers `nums` and an integer `target`, return the indices of two numbers such that their sum equals the target.

You may assume that exactly one **[solution exists]**(https://www.thecreativeunit.com/) , and you cannot use the same element twice.

## Brute-Force Approach

We can check every possible pair of numbers using two nested loops.

```python
class Solution:
    def twoSum(self, nums, target):
        n = len(nums)

        for i in range(n):
            for j in range(i + 1, n):
                if nums[i] + nums[j] == target:
                    return [i, j]
