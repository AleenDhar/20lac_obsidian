---
tags:
  - "#segment_tree"
  - "#DSA"
  - "#easy"
---
# question


without pre-sum : This is not the optimal soln as the max time taken can be O(n)
```python
class NumArray(object):
    def __init__(self, nums):
        self.nums = nums

    def sumRange(self, left, right):
        summ = sum(self.nums[left:right+1])
        return summ
```
Using Pre-sum: we calculate the pre-sum (sum of all the elements appearing before + current number)