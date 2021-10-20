첫 실행 코드

    class Solution:
        def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
            prev = None
            curr = head
            
    
    		while(curr != None) :
            	temp = curr.next    
            
            	curr.next = prev
            	prev = curr
            	curr = temp
        	return prev





스택을 활용한 실행 코드



       class Solution:
        def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
            if head == None :
                return head
       
       	stack = []
        
        curr = head
        
        while curr.next != None :
            stack.append(curr)
            curr = curr.next
            
        first = curr
        
        while stack :
            curr.next = stack.pop()
            curr = curr.next
            
        curr.next = None
        
        return first

