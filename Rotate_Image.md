```
class Solution(object):
    def rotate(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: None Do not return anything, modify matrix in-place instead.
        """
        matrix[:] = list(zip(*matrix))
        for i in range(len(matrix)):
            matrix[i] = list(matrix[i])
            matrix[i].reverse()
```            
