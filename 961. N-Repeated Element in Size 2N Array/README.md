# Problem

URL: [https://leetcode.com/problems/n-repeated-element-in-size-2n-array/](https://leetcode.com/problems/n-repeated-element-in-size-2n-array/) 

In a array `A` of size `2N`, there are `N+1` unique elements, and exactly one of these elements is repeated N times.

Return the element repeated `N` times.

**Example 1:**

    Input: [1,2,3,3]
    Output: 3

**Example 2:**

    Input: [2,1,2,5,3,2]
    Output: 2

**Example 3:**

    Input: [5,1,5,2,5,3,5,4]
    Output: 5

---

# Solution

    class Solution:
        def repeatedNTimes(self, A):
            """
            :type A: List[int]
            :rtype: int
            """
            seen_number = set()
            for num in A:
                if num not in seen_number:
                    seen_number.add(num)
                else:
                    return num
                    
    d = [1,2,2,5,3,2]
    a = Solution()
    print(a.repeatedNTimes(d))

    class Solution:
        def repeatedNTimes(self, A):
            """
            :type A: List[int]
            :rtype: int
            """
            N = len(A)/2
            buf = []
            for i in range(0,len(A)):
                if(A.count(A[i]) == N):
                    return A[i]
    
    d = [1,2,2,5,3,2]
    a = Solution()
    print(a.repeatedNTimes(d))
