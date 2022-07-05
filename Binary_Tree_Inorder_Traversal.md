```
# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution(object):
    def inorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        # two similar solutions
        if root == None:
            return []
        output = [root]
        while not all(isinstance(x, int) for x in output):
            for i in output:
                if i != None and type(i)!=int:
                    index = output.index(i)
                    output[index] = i.val
                    output.insert(index, i.left)
                    output.insert(index+2, i.right)
                    output = [x for x in output if x != None]
        return output

        if root == None:
            return []
        output = [root]
        while not all(isinstance(x, int) for x in output):
            for i in range(len(output)):
                if output[i] != None and type(output[i])!=int:
                    output.insert(i, output[i].left)
                    output.insert(i+2, output[i+1].right)
                    output[i+1] = output[i+1].val
                    output = [x for x in output if x != None]
        return output    
```        
