```
# slow solution
class Solution(object):
    def longestPalindrome(self, s):
        """
        :type s: str
        :rtype: str
        """
        a = s[::-1]
        for i in range(len(s)-1, -1, -1):
            for j in range(len(s)-i):
                if s[j:i+j+1] == a[len(s)-i-j-1:len(s)-j]:
                    return s[j:i+j+1]

# fast solution

```
