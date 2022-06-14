'''
class Solution(object):
    def isValidSudoku(self, board):
        """
        :type board: List[List[str]]
        :rtype: bool
        """
        for i in range(9):
            if(len(set([x for x in board[i] if board[i].count(x)>1]))>1):
                return False
            if(len(set([x for x in [list(y) for y in zip(*board)][i] if [list(z) for z in zip(*board)][i].count(x)>1]))>1):
                return False
        for j in range(3):
            for k in range(3):
                lst = [item[j*3:(j+1)*3] for item in board[k*3:(k+1)*3]]
                l = [item for sublist in lst for item in sublist]
                if(len(set([x for x in l if l.count(x)>1]))>1):
                    return False
        return True
'''
