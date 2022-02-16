```
class Solution(object):
    def nextPermutation(self, nums):
        """
        :type nums: List[int]
        :rtype: None Do not return anything, modify nums in-place instead.
        """
        if len(set(nums)) == 1:
            return nums
        
        a = len(nums)-1
        
        while nums[a] <= nums[a-1]: # 找出不是降冪的數字
            a = a-1
        
        b = a - 1 # make the index of number to change constant
        
        c = len(nums) - 1
        while nums[b]>=nums[c]: # 找出要換的數字
            c = c-1
                
        r = nums[c]
        nums[c] = nums[b]
        nums[b] = r
        # sort nums[b] to nums[len(nums)]
        nums[b+1:] = sorted(nums[b+1:])
        return nums

        # Runtime = 72%
        # Memory Usage = 72%
```
