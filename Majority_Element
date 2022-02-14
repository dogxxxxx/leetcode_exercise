```
class Solution(object):
    def majorityElement(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        a = (dict([[x,nums.count(x)] for x in set(nums)]))
        for i in a.items():
            if i[1] > len(nums)/2:
                return i[0]                             
```
