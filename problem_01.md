첫 성공 코드 (  168 ms  )

       class Solution:
        def containsDuplicate(self, nums: List[int]) -> bool:
            result = set(nums)
            # for i in nums :
            #     if i not in result :
            #         result.append(i)
            
            re = (True if sorted(result) != sorted(nums) else False)
        
            return re
    





조금 더 효율적으로 짠 코드  (  116 ms  )
        

        class Solution:
        def containsDuplicate(self, nums: List[int]) -> bool:
            result = set(nums)
        
        if(sorted(result) == sorted(nums)) :
            return 0
        
        else :
            return 1