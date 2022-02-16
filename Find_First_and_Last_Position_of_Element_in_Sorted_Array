```
class Solution(object):
    def searchRange(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: List[int]
        """
        if target not in nums:
            return [-1,-1]
        
        a = nums.index(target)
        nums.sort(reverse=True)
        b = len(nums)-1-nums.index(target)
        return[a,b]
```

