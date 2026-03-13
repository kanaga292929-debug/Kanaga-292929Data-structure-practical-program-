class Solution:
    def commonElements(self, arr1, arr2, arr3):
        i, j, k = 0, 0, 0
        res = []
        
        while i < len(arr1) and j < len(arr2) and k < len(arr3):
            # If all three are equal
            if arr1[i] == arr2[j] == arr3[k]:
                # Add only if it's not a duplicate in our result
                if not res or res[-1] != arr1[i]:
                    res.append(arr1[i])
                i += 1
                j += 1
                k += 1
            
            # Move the pointer of the smallest element
            elif arr1[i] < arr2[j]:
                i += 1
            elif arr2[j] < arr3[k]:
                j += 1
            else:
                k += 1
        
        # If no common elements found, return [-1]
        return res if res else [-1]
# Kanaga-292929Data-structure-practical-program-
Kanagavalli data structures 
