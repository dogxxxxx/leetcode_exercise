```
class Solution(object):
    def lengthOfLongestSubstring(self, s):
        """
        :type s: str
        :rtype: int
        """
        def get_substring(i):
            sub = ''
            o = i
            while i<len(s) and s[i] not in sub:
                sub = s[o:i+1]
                i+=1
            return len(sub)
        
        longest = 0
        for i in range(len(s)):
            a = get_substring(i)
            if a > longest:
                longest = a
        return longest
```        
