```
        ans = list()
        for i in range(len(nums)):
            for j in range(len(nums)):
                if -1*(nums[i]+nums[j]) in nums:
                    k = nums.index(-1*(nums[i]+nums[j]))
                    if (i!=j) & (j!=k) & (i!=k):
                        a = sorted([nums[i], nums[j], nums[k]])
                        if a not in ans:
                            ans.append(a)
        return ans
        
        # to be faster, or try another way to solve it
```        
