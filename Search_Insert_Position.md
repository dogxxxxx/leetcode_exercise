```
class Solution(object):
    def searchInsert(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: int
        """
        if target > nums[len(nums)]:
            return len(nums)
        if target > nums[len(nums)-1]:
            return len(nums)
        while target not in nums:
            target = target + 1
        return nums.index(target)
```
