```
class Solution(object):
    def climbStairs(self, n):
        """
        :type n: int
        :rtype: int
        """
        def factorial(a):
            fact = 1
            for i in range(1, 1+a):
                fact = fact*i
            return fact
        result = 0
        b = n
        for i in range(-((-n-1)//2)):
            result = result + factorial(n-i)/(factorial(i)*factorial(b))
            b = b - 2
        return result
```
