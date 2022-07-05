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
class Solution(object):
    def longestPalindrome(self, s):
        """
        :type s: str
        :rtype: str
        """
        def start_end_indices(i, j):
            while 0<=i<=j<len(s) and s[i]==s[j]:
                i -= 1
                j += 1
            return s[i+1:j]
        longest = s[0:1]
        for i in range(len(s)):
            odd = start_end_indices(i, i)
            even = start_end_indices(i, i+1)
            if len(odd)>len(even) and len(odd)>len(longest):
                longest = odd
            elif len(even)>len(odd) and len(even)>len(longest):
                longest = even
        return longest
```        
