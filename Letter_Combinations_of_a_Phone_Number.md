```
class Solution(object):
    def letterCombinations(self, digits):
        """
        :type digits: str
        :rtype: List[str]
        """
        if len(digits) == 0:
            return []
        dictionary = {
            '2':['a','b','c'],
            '3':['d','e','f'],
            '4':['g','h','i'],
            '5':['j','k','l'],
            '6':['m','n','o'],
            '7':['p','q','r','s'],
            '8':['t','u','v'],
            '9':['w','x','y','z']
        }
        output = ['']
        for digit in digits:
            output = output*len(dictionary[digit])
            output.sort()
            for i in range(len(output)):
                output[i] = output[i]+dictionary[digit][i%len(dictionary[digit])]
        return output
```
