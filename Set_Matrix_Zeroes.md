```
class Solution(object):
    def setZeroes(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: None Do not return anything, modify matrix in-place instead.
        """
        m = len(matrix)
        n = len(matrix[0])
        for i in range(m):
            for j in range(n):
                if matrix[i][j] == 0:
                    for indices in range(n):
                        if matrix[i][indices] != 0:
                            matrix[i][indices] =  'a'   
                    for a in matrix:
                        if a[j] != 0:
                            a[j] = 'a'
        print(matrix)
        for i in range(m):
            for j in range(n):
                if type(matrix[i][j]) == str:
                    matrix[i][j] = 0
```
