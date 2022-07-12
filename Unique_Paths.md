```
class Solution(object):
    def uniquePaths(self, m, n):
        """
        :type m: int
        :type n: int
        :rtype: int
        """
        def fac(a):
            fact = 1
            for i in range(1,a+1):
                fact = fact*i
            return fact
        return fac(m+n-2)/(fac(m-1)*fac(n-1))
```
