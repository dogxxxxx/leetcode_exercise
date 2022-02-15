```
class Solution(object):
    def maxArea(self, height):
        """
        :type height: List[int]
        :rtype: int
        """
        ans = 0
        for i in range(len(height)):
            for j in range(i+1, len(height)):
                con = (j-i)*(min(height[i], height[j]))
                if con > ans:
                    ans = con
        return ans
        
        # to be faster
```
