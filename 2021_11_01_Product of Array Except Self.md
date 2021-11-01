
        

       class Solution:
        def productExceptSelf(self, nums: List[int]) -> List[int]:
       
       sum = 1
        answer = []
        zero = 0
        
        for i in range(len(nums)) :
            if(nums[i] != 0) :
                sum *= nums[i]
            else :
                zero += 1
                if(zero >= 2) :
                    sum *= 0
        for i in range(len(nums)) :
            if(nums[i] != 0) :
                if(zero == 0) :
                    answer.append(sum//(nums[i]))
                else :
                    answer.append(0)
            else :
                answer.append(sum)
        return answer


​            