
```
class Solution(object):
    def twoSum(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        ans=[]
        for a in range(len(nums)):
            if ((target-nums[a]) in nums):
                b = nums.index(target-nums[a])
                if a!=b:
                    ans = [a,b]
                    return ans
        return ans
```
