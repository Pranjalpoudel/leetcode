
class Solution(object):
    def mergeTwoLists(self, list1, list2):
        result = []
        i, j = 0, 0
        
        while i < len(list1) and j < len(list2):
            if list1[i] <= list2[j]:
                result.append(list1[i])
                i += 1
            else:
                result.append(list2[j])
                j += 1
        
        while i < len(list1):
            result.append(list1[i])
            i += 1
        
        while j < len(list2):
            result.append(list2[j])
            j += 1
        
        return result           
l1 = [1,2,3]
l2 = [1,4,5]
obj = Solution()
print(obj.mergeTwoLists(l1,l2))
