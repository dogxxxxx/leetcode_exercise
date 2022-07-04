class Solution(object):
    def isValid(self, s):
        """
        :type s: str
        :rtype: bool
        """
        openb = ['(', '{', '[']
        dic = {')':'(', '}':'{', ']':'['}
        reduced = []
        if len(s)%2 == 1:
            return False
        for word in s:
            if word in openb:
                reduced.append(word)
            elif len(reduced) != 0 and dic[word] == reduced[-1]:
                del reduced[-1]
            else:
                return False
        if len(reduced) != 0:
            return False
        return True
